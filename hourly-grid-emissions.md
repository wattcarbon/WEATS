## **Calculating Hourly Emissions**


### **Overview of locational emissions methodology.**

1.1. Model intuition.

1.1.1. A site receives electricity from the grid to which it is interconnected. The source of this electricity comes from a variety of power plants that are dispatched according to contracts and bidding mechanisms established by the balancing authority. The site operator can choose to consume or not consume electricity during a particular period of time, but does not have control over the source of electricity provided by the grid operator.

1.2. Foundations in literature. Modeling does not strictly adhere to these methods, but draws from them for inspiration.

1.2.1. World Resources Institute GHG Emissions Scope 2 Emissions Protocol.

1.2.2. Energy Tag.

1.2.3. 24/7 Carbon Free Energy Compact.

1.3. Annual emissions are calculated for the 365 days immediately prior to the reporting period end date, provided the data sufficiency criteria are met.

1.4. Follow the process outlined below and detailed in subsequent sections:

1.4.1. Select and qualify sites and assets. Emissions should be calculated on a site-level basis, but may be aggregated across sites in a subsequent process.

1.4.2. Use hourly emissions factors from matched balancing authority.

1.4.3. Align timestamps of site-level energy consumption to equivalent timestamps of power systems data.

1.4.4. Compute all hourly emissions values by multiplying hourly consumption by the associated grid emissions value.

1.4.5. Sum each hourly value.

1.4.6. Aggregate across sites.


### **2. Portfolio aggregation.**

2.1. In accordance with existing standards, all qualifying sites should be selected for inclusion in the aggregated portfolio.

2.1.1. In cases where some site consumption is associated with an owner and other consumption is associated with a tenant (thus becoming a Scope 3 emission), it is reasonable to subdivide the emissions from a single site into multiple (exclusive) aggregations.

2.1.2. If some sites that would be included in a portfolio lack the quality of data of other sites, all sites should be included, but the data limitations should be called out (see methods for estimating hourly consumption using data models).

2.2. Constraints and qualification.

2.2.1. Energy attribute purchases may be included in a portfolio aggregation. Non-energy attribute purchases should be accounted for elsewhere.


### **3. Use Hourly Emissions factors from matching balancing authority.**

3.1. Basic structure applies to analysis using both actual and modeled energy consumption.

3.1.1. Carbon emissions: weighted average of operational emissions from each fuel dispatched during a particular time period on a grid.

3.1.2. Produced electricity mix: The aggregate amount of electricity dispatched onto a grid from power plants within a particular balancing authority. This number does not include imports or exports to/from neighboring balancing authorities.

3.1.3. Consumed electricity mix: The aggregate amount of electricity consumed within a grid including power dispatched from power plants within the grid and any imported power from neighboring grids and excluding any power exported to neighboring grids.

3.2. When calculating emissions for a site, the emissions factor of the Consumed electricity mix should be used.

3.2.1. If calculating negative emissions from distributed generation, the Consumed electricity mix should be used.

3.2.1. If calculating negative emissions from generation that is managed by the balancing authority, Produced electricity mix should be used.

3.3. Equation: Annual emissions = sum of hourly energy use multiplied by emissions factor.


### **4. Align timestamps.**

4.1. All time series data should be consistently formatted such that a time stamp indicates the beginning of a known length of time (e.g., 7:00 AM indicates the period between 7:00 and 8:00 AM).

4.2. Time series data should be upsampled to create a consistent hourly time-series for both consumption and power systems data.

4.3. If any data is in local time, it should be converted to UTC prior to computing hourly emissions.

4.4. Upon calculating hourly emissions, time stamps should be converted to the local time of the site prior to aggregation with other sites.

4.4.1. All aggregation should be done in the local time zone. For example, if there are two sites, one a site in Eastern Standard Time and the other a site in Pacific Standard time, they should have their noon (local time) carbon emissions aggregated.


### **5. Compute all Hourly Emissions.**

5.1. For each hour, multiply the site consumption value by the appropriate emissions factor.

5.1.1. Missing consumption grid emissions values should be filled in with average of non-missing values for the preceding and subsequent interval.

5.1.2. If hourly grid emissions factors are calculated by averaging higher frequency data, no more than 50% of high-frequency values should be missing.

5.1.3. Missing consumption values should be filled in with average of non-missing values for the preceding and subsequent interval.

5.1.4. Data is considered missing if it is clearly marked by the data provider as NULL, NaN, or similar.


### **6. Annual Aggregation.**

6.1. The product of each hour’s carbon emissions calculation should be summed for the reporting time period (typically annually).

6.2. If data sufficiency requirements have been met (see 2.2), total emissions should be normalized to a full year (8,760 hours) for reporting purposes.

6.2.1. Sum the total emissions of each hourly value. Divide by the number of valid hours in the dataset. Multiply by 8760.
