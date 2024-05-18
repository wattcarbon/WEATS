## Summary

All EACs from renewables or batteries represent a watt-hour of clean energy production, or in the case of batteries, time-shifted clean energy production. Where electricity has been time-shifted, the EAC represents a watt-hour of emission-neutral generation, estimated by factoring out the emissions rate of the grid during charging and the emissions rate of the grid during discharging. Each EAC is assigned a serial number that is linked to the asset and the time of day. 


## The Basics

Renewable energy production is measured using telemetry within a device (such as an inverter) or via a separate meter that may be located at the point of interconnection with the grid. This data is usually uploaded to a central cloud-hosted database that can be accessed through an API or other automated data transfer. For the purposes of creating EACs, WattCarbon requires this data to be uploaded to the WattCarbon platform for independent authentication of energy production. 


## An Hourly EAC Registry for DERs

WattCarbon operates WEATS, a fully functional Registry for tracking, transacting, and retiring EACs. The Registry is based on the principle of hourly tracking of EACs at the **Asset** level, where Assets are located at **Sites**, and are connected to **Projects**. Initial Registry registration happens at the Site level, where the address is converted to a set of latitude/longitude coordinates. This data layer serves two important purposes. First, it allows the site to be geolocated on the grid for proper attribution of carbon emissions. Second, it allows the Registry to be queried for potential duplicate claims without revealing private or proprietary information. We can expose the Sites endpoint to the public without also exposing the Assets or Projects endpoints.


## Projects 

**Projects** are an important concept because they define both the type of intervention as well as the performance period. We’ve already defined electrification projects and demand response projects. Here we will describe directly metered projects. For example, a directly metered interconnection point may be supporting both a solar and a battery asset and may involve flows of energy in both directions (production and consumption). Whether or not the battery charges solely from the solar panels or jointly from solar and from the grid will matter for the way the methodology is applied.


## Assets

**Assets** are what provide us with the necessary data to calculate EACs. Each asset delivers a time-series of data representing hourly (or more frequent) energy consumption or production. If sub-hourly increments are provided, we aggregate the data to hourly intervals. Electricity is tracked at the watt-hour level of granularity. Each watt-hour that becomes an EAC is assigned its own serial number so that it can be uniquely identified, in perpetuity. All other energy, site, and project attributes are attached to the serial number so that the provenance of the EAC is completely transparent. 


## Carbon Emission Intuition

If 24/7 carbon-free energy is the ultimate goal of clean energy procurement, our intuition is to use the carbon intensity of the grid as the way to prioritize the most valuable clean electrons. An additional solar panel in a solar-saturated state like California will still be helpful, especially as it contributes clean energy to still-dirty shoulder hours, but not nearly as helpful as a solar panel located in a grid that primarily relies upon fossil fuels for generation throughout the day. We recognize that using a grid-wide average emissions intensity, especially in a large balancing authority like MISO, where transmission constraints can be significant, runs the risk of rewarding or penalizing renewable energy development “behind the transmission constraint.” For example, the value of a new wind farm in Minnesota may be overstated because the wind energy cannot get to the dirtier southern portion of the MISO grid. However, our goal is to use the carbon signal as a proxy for what resources would be needed at different times of day for a grid to be self-sufficient, assuming that it can also solve its interconnection bottlenecks. Already we see evidence of success as transmission companies open new routes for energy to be routed to urban areas. To the extent that greater administrative granularity is valuable, we believe that utility-specific “consumed carbon emissions” data are needed. This is especially the case for utilities that are responsible for procuring supply for their customers or who own and operate their own generation supplies.


## Clean energy generation

Clean energy generation from solar, wind, hydro, and other resources can be measured directly. Data from inverters is transferred to WattCarbon to be converted into EACs. All data is converted to watt-hours. Each Watt-hour is assigned a unique ID and becomes an EAC. Other attributes are attached to the EAC. Missing hours do not receive EACs. Outliers or other obviously wrong data (such as overnight solar production) are removed from the dataset.


## Batteries and Time-Shifted Emissions

Batteries present a special tricky case because they can be directly metered, but don’t actually generate electricity. So the charging of the battery must be taken into account in addition to the discharging. Battery charging can come from an attached renewable (or non-renewable) generator or from the grid itself. If it comes from an attached renewable generator, the discharged electricity can be considered “clean”, but the renewable generation must be accounted for so as to not be double-counted. If the battery is charged from the grid, the net emissions must be calculated.


## Combined Solar and Storage

Starting with the case in which batteries are charged from an attached generation system, there are two typical data configurations. First, the battery and renewable generator might share the same meter, so that there is only one Asset from which to derive data. If the battery is never charged from the grid, a net production profile would be used in which each hour’s total production is calculated. If the battery was charged in the morning from the solar panels, solar production in the morning would show up as minimal and then extend into the evening while the battery was discharging. 

The second case is a separately metered, yet still attached, battery and solar system. In this case, the solar EACs must be minted separately and then canceled against the battery charging in the same hour. Only the excess solar EACs would be transferred. The canceled solar EACs are assigned to the battery. Because the battery is less than 100% efficient at converting energy, losses must also be accounted for. Only the energy that is actually dispatched from the battery is assigned a new EAC, with the remainder of the lost EACs retired against the battery’s efficiency losses. 

Even if the systems are connected, it is possible that the battery is charged from the grid. This is observable when there is net negative production (i.e., consumption) or in the case of separately metered systems, when the production of solar EACs is less than the energy fed into the battery to charge it for any given hour. In this case, the emissions of the charging energy must be factored into the accounting to create a “clean” discharge. 


## Stand Alone Storage

Stand-alone batteries, which always charge from the grid, always represent some amount of “embedded” emissions. Accounting for these emissions is central to the validity of an EAC for batteries that are strictly deployed as a grid resource. If a battery is charged during periods of low emissions and discharged during periods of high emissions, a net reduction in emissions is possible. However, the net emissions difference must be large enough to allow for the efficiency losses in the charge/discharge cycle of the battery. Assuming that this condition is met, the battery’s discharge EACs are assigned the net emissions rate. This rate is calculated by looking up the hourly emissions rate for each hour of charging and multiplying that rate by the total amount of electricity consumed by the battery during that hour. That number is subtracted from the avoided discharged emissions using the same methodology. For example, if the battery is charged for one hour at an emissions rate of 100 lbs/mwh and discharged for one hour at a rate of 200 lbs/mwh and the battery gets charged with 10 kWh and discharges 9 kWh, the consumed emissions will be 1 lb and the avoided emissions will be 1.8 lb for a net emissions savings of 0.8 lb.

WattCarbon uses a concept of “carbon debt” to ensure that EACs represent net emissions reductions. As the battery charges from less than 100% clean sources, it accrues carbon in its account. As the battery discharges, it generates EACs that are immediately retired against accumulated carbon debt. Only the discharged electricity in excess of the carbon becomes eligible for transferrable EACs. To avoid the accumulation of debt, a battery account can be paired with a renewable energy account such that the renewable energy EAC output is retired against the battery debt.
