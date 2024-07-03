Name: Energy Efficiency EACs using pre and post measurements

Developer: C3

Revision Date: 2024-06-20

 

**Glossary**

Asset: An energy device or energy system within a measurement boundary acted upon by an intervention that results in a change in energy consumption relative to a baseline.

Site: A uniquely identifiable geographical location of an Asset

Pre: Denotes the time prior to the intervention that will change energy consumption

Post: Denotes the time after the intervention that will change energy consumption.

 

**Summary**

The purpose of this methodology is to estimate the energy and related carbon impact of energy efficiency projects in commercial buildings. Specifically, the methodology looks to measure the number of hourly useful EACs, avoided emissions, and the generated grid emissions from changing electricity consumption.

The applicable interventions will be listed in the Measure Upgrades section.

**Measure Upgrades**

1\. LED Lighting and / or Lighting Controls (including dimming)

** **

**Project Stakeholders**

Provide contact information for relevant stakeholders which may include Asset Owner.

|                   |                 |
| ----------------- | --------------- |
| **Field**         | **Description** |
| Organization Name |                 |
| Contact Name      |                 |
| Contact Title     |                 |
| Email             |                 |
| Phone             |                 |
| Mailing Address   |                 |
| Mailing Address 2 |                 |
| City              |                 |
| State             |                 |
| Zip Code          |                 |

 

**Asset Location**

|            |             |          |           |         |         |
| ---------- | ----------- | -------- | --------- | ------- | ------- |
| **Site #** | **Address** | **City** | **State** | **Lat** | **Lon** |
| 1          |             |          |           |         |         |
| 2          |             |          |           |         |         |
| 3          |             |          |           |         |         |
| 4          |             |          |           |         |         |
| 5          |             |          |           |         |         |
| 6          |             |          |           |         |         |

 

**Project Dates**

Provide information about the project dates including: Project Start Date, Project End Date, and Project Duration.

** **

**Measure 1. LED Lighting – Energy Saving Calculation**

_Pre-intervention Details_

Data shall be collected by a project developer to indicate the Quantity of Fixtures, Location of Fixture, Fixture Wattage, Hours of Use and other attributes affecting baseline energy use. Data will be gathered from an on-site audit to verify the existing lighting systems and be documented in a line-by-line audit.  At a minimum, each line of the audit will contain the number of fixtures with unique combinations of the following attributes as determined from the source(s) indicated:

|                                                |             |                                                                                                    |
| ---------------------------------------------- | ----------- | -------------------------------------------------------------------------------------------------- |
| **Attribute**                                  | **Units**   | **Source**                                                                                         |
| Location (Building/Room)                       | Descriptive | Field observation, site map                                                                        |
| Baseline Fixture Type (type/lamps per fixture) | Descriptive | Field observation                                                                                  |
| Baseline Fixture Wattage                       | Watts       | Manufacturer’s Specifications, Table of Standard Wattages (see Attachment 1), or spot measurements |
| Baseline Hours of Operation                    | hrs/year    | Field observation, facility manager interviews or data logging                                     |

 

Optional data may also be provided which includes Fixture Description, Model #, and Manufacturer. Where available, floor plans and reflected ceiling plans may be gathered to support the line-by-line audit, but the expectation is the line-by-line audit shall provide sufficient detail of fixture location and details to reasonably replicate or validate the contents should a third party review the project.

_Post-intervention Details_

For each line of the pre-intervention line-by-line audit above, the following data shall be detailed to provide the post-intervention project specifications of the proposed case.

|                                                |             |                                          |
| ---------------------------------------------- | ----------- | ---------------------------------------- |
| **Attribute**                                  | **Units**   | **Source**                               |
| Proposed Fixture Quantity                      | Number      | Proposed project specifications          |
| Proposed Fixture Type                          | Descriptive | Proposed project specifications          |
| Proposed Fixture/Retrofit Manufacturer & Model | Descriptive | Proposed project specifications          |
| Proposed Fixture Wattage                       | Watts       | Proposed project specifications          |
| Proposed Controls, if applicable               | Descriptive | Proposed project specifications          |
| Proposed Hours of Operation                    | hrs/year    | Equal to existing, unless controls added |

 

Proposed fixture specifications shall align with the proposed scope of work and be supported by manufacturer’s product-specific data sheets (“cutsheets”).

_Energy Saving Calculation_

The combination of the pre and post intervention details will collectively form a comprehensive line by line audit to serve as the basis for calculated energy savings. For each line in the audit, the following will be calculated in a spreadsheet:

_Baseline Annual Electricity (kWh/yr)  = Baseline Fixture Quantity \* Baseline Fixture Wattage \* (1 kW / 1000 W) \* Baseline Hours of Operation_

_Proposed Annual Electricity (kWh/yr)  = Proposed Fixture Quantity \* Proposed Fixture Wattage \* (1 kW / 1000 W) \* Proposed Hours of Operation_

_Saved Annual Electricity (kWh/yr)  = Baseline Annual Electricity – Proposed Annual Electricity_

The Saved Annual Electricity for each line will then be summed to determine the total project savings. This calculation will be updated upon installation of the project to reflect the as-built conditions and energy savings.

**Measurement and Verification**

To further validate the energy savings levels and to ensure persistence of savings over the anticipated lifetime of the intervention, measurement and verification will be performed. For each project a site-specific measurement and verification plan will be developed. At a minimum each plan will include:

<!--[if !supportLists]-->·         <!--[endif]-->Selection of representative circuits to isolate lighting loads being retrofit

<!--[if !supportLists]-->·         <!--[endif]-->Installation of meters to record amperage or power in no more than 15-minute intervals

<!--[if !supportLists]-->·         <!--[endif]-->Storage of the interval data for analysis on a centralized server

<!--[if !supportLists]-->·         <!--[endif]-->Performing calculations of energy savings and reporting results in a web-based or API based platform

<!--[if !supportLists]-->·         <!--[endif]-->A fixture sampling plan that achieves a 10% precision at 90% confidence covering fixtures retrofit, assuming a Coefficient of Variation of 0.5 as calculated below

First determine the initial sample size; n = <!--[if gte msEquation 12]><m:oMath><m:f><m:fPr><span
   style='font-family:"Cambria Math",serif;mso-ascii-font-family:"Cambria Math";
   mso-hansi-font-family:"Cambria Math";font-style:italic;mso-bidi-font-style:
   normal'><m:ctrlPr></m:ctrlPr></span></m:fPr><m:num><m:sSup><m:sSupPr><span
     style='font-family:"Cambria Math",serif;mso-ascii-font-family:"Cambria Math";
     mso-hansi-font-family:"Cambria Math";font-style:italic;mso-bidi-font-style:
     normal'><m:ctrlPr></m:ctrlPr></span></m:sSupPr><m:e><i style='mso-bidi-font-style:
     normal'><span style='font-family:"Cambria Math",serif'><m:r>Z</m:r></span></i></m:e><m:sup><i
     style='mso-bidi-font-style:normal'><span style='font-family:"Cambria Math",serif'><m:r>2</m:r></span></i></m:sup></m:sSup><m:sSup><m:sSupPr><span
     style='font-family:"Cambria Math",serif;mso-ascii-font-family:"Cambria Math";
     mso-hansi-font-family:"Cambria Math";font-style:italic;mso-bidi-font-style:
     normal'><m:ctrlPr></m:ctrlPr></span></m:sSupPr><m:e><i style='mso-bidi-font-style:
     normal'><span style='font-family:"Cambria Math",serif'><m:r>CV</m:r></span></i></m:e><m:sup><i
     style='mso-bidi-font-style:normal'><span style='font-family:"Cambria Math",serif'><m:r>2</m:r></span></i></m:sup></m:sSup></m:num><m:den><m:sSup><m:sSupPr><span
     style='font-family:"Cambria Math",serif;mso-ascii-font-family:"Cambria Math";
     mso-hansi-font-family:"Cambria Math";font-style:italic;mso-bidi-font-style:
     normal'><m:ctrlPr></m:ctrlPr></span></m:sSupPr><m:e><i style='mso-bidi-font-style:
     normal'><span style='font-family:"Cambria Math",serif'><m:r>P</m:r></span></i></m:e><m:sup><i
     style='mso-bidi-font-style:normal'><span style='font-family:"Cambria Math",serif'><m:r>2</m:r></span></i></m:sup></m:sSup></m:den></m:f></m:oMath><![endif]--><!--[if !msEquation]--><!--[if gte vml 1]><v:shapetype
 id="_x0000_t75" coordsize="21600,21600" o:spt="75" o:preferrelative="t"
 path="m@4@5l@4@11@9@11@9@5xe" filled="f" stroked="f">
 <v:stroke joinstyle="miter"/>
 <v:formulas>
  <v:f eqn="if lineDrawn pixelLineWidth 0"/>
  <v:f eqn="sum @0 1 0"/>
  <v:f eqn="sum 0 0 @1"/>
  <v:f eqn="prod @2 1 2"/>
  <v:f eqn="prod @3 21600 pixelWidth"/>
  <v:f eqn="prod @3 21600 pixelHeight"/>
  <v:f eqn="sum @0 0 1"/>
  <v:f eqn="prod @6 1 2"/>
  <v:f eqn="prod @7 21600 pixelWidth"/>
  <v:f eqn="sum @8 21600 0"/>
  <v:f eqn="prod @7 21600 pixelHeight"/>
  <v:f eqn="sum @10 21600 0"/>
 </v:formulas>
 <v:path o:extrusionok="f" gradientshapeok="t" o:connecttype="rect"/>
 <o:lock v:ext="edit" aspectratio="t"/>
</v:shapetype><v:shape id="_x0000_i1025" type="#_x0000_t75" style='width:24pt;
 height:21.75pt'>
 <v:imagedata src="file:///C:/Users/weins/AppData/Local/Temp/msohtmlclip1/01/clip_image001.png"
  o:title="" chromakey="white"/>
</v:shape><![endif]--><!--[if !vml]-->![](file:///C:/Users/weins/AppData/Local/Temp/msohtmlclip1/01/clip_image002.png)<!--[endif]--><!--[endif]--> 

where; n = initial sample size\
Z = The z-statistic for the desired level of confidence. Equal to 1.645 for a confidence level of 90%\
CV =assumed coefficient of variation (0.5)\
P = desired precision (10%)

and then determine the adjusted sample size based on the population; n\* = <!--[if gte msEquation 12]><m:oMath><m:f><m:fPr><span
   style='font-family:"Cambria Math",serif;mso-ascii-font-family:"Cambria Math";
   mso-hansi-font-family:"Cambria Math"'><m:ctrlPr></m:ctrlPr></span></m:fPr><m:num><span
   style='font-family:"Cambria Math",serif;mso-bidi-font-family:"Cambria Math"'><m:r><m:rPr><m:scr
      m:val="roman"/><m:sty m:val="p"/></m:rPr>Nn</m:r></span></m:num><m:den><span
   style='font-family:"Cambria Math",serif;mso-bidi-font-family:"Cambria Math"'><m:r><m:rPr><m:scr
      m:val="roman"/><m:sty m:val="p"/></m:rPr>N+n</m:r></span></m:den></m:f></m:oMath><![endif]--><!--[if !msEquation]--><!--[if gte vml 1]><v:shape
 id="_x0000_i1025" type="#_x0000_t75" style='width:17.25pt;height:20.25pt'>
 <v:imagedata src="file:///C:/Users/weins/AppData/Local/Temp/msohtmlclip1/01/clip_image003.png"
  o:title="" chromakey="white"/>
</v:shape><![endif]--><!--[if !vml]-->![](file:///C:/Users/weins/AppData/Local/Temp/msohtmlclip1/01/clip_image004.png)<!--[endif]--><!--[endif]-->

where; n\* = adjusted sample size (actual minimum sample fixtures)\
n = initial sample size (calculated above)\
N = population size (total fixtures)

Resulting in the following minimum sample sizes based on total fixtures to achieve a 10% precision at 90% confidence:

|                                         |                                           |
| --------------------------------------- | ----------------------------------------- |
| **Total Fixture Quantity Retrofit (N)** | **Minimum Sample Fixture Quantity (n\*)** |
| 3                                       |                          3                |
| 5                                       |                          5                |
| 10                                      |                          9                |
| 25                                      |                        19                 |
| 50                                      |                        29                 |
| 100                                     |                        41                 |
| 250                                     |                        54                 |
| 500                                     |                        60                 |
| 1000                                    |                        64                 |
| 2500                                    |                        66                 |
| 5000                                    |                        67                 |
| ≥7500                                   |                        68                 |

 

Where baseline data logging is conducted, the same circuits will be monitored post retrofit for side-by-side comparison.  In such cases, the difference between measured post energy consumption to baseline energy consumption will be used to verify the true reduction;

_Saved Annual Electricity (kWh/yr) = Measured Baseline Annual Electricity – Measured Proposed Annual Electricity_

Where

_Measured Baseline Annual Electricity = ∑ Measured Baseline Circuit kW x Measurement Interval (minutes) / 60 minutes per hour _**and**

_Measured Proposed Annual Electricity = ∑ Measured Proposed Circuit kW x Measurement Interval (minutes) / 60 minutes per hour __if power_ is measured

_Or_

_Measured Baseline Annual Electricity = ∑ Measured Baseline Circuit Amperage x Baseline Circuit Voltage / 1000 W per kW x Measurement Interval (minutes) / 60 minutes per hour _**and**

_Measured Proposed Annual Electricity = ∑ Measured Baseline Circuit Amperage x Baseline Circuit Voltage / 1000 W per kW x Measurement Interval (minutes) / 60 minutes per hour __if current_ is measured__

Measurements will be taken for a full year during the Proposed period, and optimally for a full year in the Baseline period.  However, if the baseline monitoring period is not one full year, the Baseline Period Electricity will be extrapolated to annual consumption;

_Measured Baseline Annual Electricity = Measured Baseline Period Electricity / Days in Monitoring Period x 365 days_

Where _Measured Baseline Period Electricity_ is calculated in the same manner as Annual Electricity noted above.

The total of the _Saved Annual Electricity_ above will be the final annual savings where 100% of the lighting intervention is metered.  If a representative sampling has been done, the savings will be extrapolated using the Calculated savings from the line-by-line audit used for the Energy Savings Calculation;

_ Total Saved Annual Electricity = Sample Saved Annual Electricity / Sample Calculated Annual Electricity Savings \* Total Calculated Saved Annual Electricity_

If only post retrofit data logging is available, the data will be validated against the Proposed Annual Electricity, and compared to the calculated Baseline Annual Electricity_ _for the same fixtures monitored to verify savings;

_Saved Annual Electricity = Baseline Calculated Fixture Demand (kW) \* Annual Hours of Operation (hrs/yr) - Measured Proposed Annual Electricity (kWh/yr)_

Where_ Measured Proposed Annual Electricity _is determined as described above and _Baseline Calculated Fixture Demand_ and _Annual Hours of Operation_ are from the line-by-line audit used for the as-built Energy Savings Calculation.
