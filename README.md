# Humanitarian Incidents in Africa by the Overseas Security Advisory Council at the Department of State
This is the data repository for the Humanitarian Incidents in Africa operated and updated by the Overseas Security Advisory Council at the Department of State.

<b> Visual Dashboard (desktop): </b> https://humanitarianincidentdashboard.com

<b>Provided by Overseas Security Advisory Council:</b>
https://osac.gov/

<b> About the Data:</b> This dashboard uses data from the Armed Conflict & Location Event Data Project (ACLED) and the Aid Worker Security Database (AWSD). This data is publicly available and open source in nature. It does not include incidents not reported in the media or to either organization directly. The number of incidents involving or against humanitarian workers abroad is likely much larger than the sum of this portrayed dataset. For additional resources regarding incidents affecting the humantarian community abroad, please see the resources listed at the bottom of this slider. A repository of the data used is found on GitHub here, published at the end of every day. The dashboard itself updates four (4) times a day.

Note: Location and fatality data may not be exact. Event location data at the lat/long level and fatality counts may differ by account or source. This dashboard relies on information input by ACLED and AWSD and should not be viewed as an authoritative source on specific event location or fatality information.

<b> Data attributions: </b> <em> "Humanitarian Outcomes, Aid Worker Security Database, https://aidworkersecurity.org/"  / “Armed Conflict Location & Event Data Project (ACLED); https://www.acleddata.com/" </em> 

Please do not use, reproduce, or otherwise share without attribution to the original datasources and <em> "Overseas Security Advisory Council (OSAC), Humanitarian Incidents in Africa Dashboard, https://osac.gov" </em>

<b> Methodology:</b> Both the ACLED and AWSD datasets have been combined, filtered, and manipulated using Python to illustrate only events relevant to the humantiarian community. The data manipulation workflow is published below in general terms for transparency:

1. Data from the ACLED was imported and then filtered using the following key words to determine relevancy to humanitarian workers: 'humanitarian (notes/actor2/assoc_actor_2), aid work (notes/actor2/assoc_actor_2)'. The following key phrase omitted entries: 'humanitarian source, humanitarian funds, humanitarian preparedness, humanitarian map' and 'peaceful (sub_event_type). This process was double checked for accuracy and precision.

2. ACLED data was grouped using the inter codes as found in ACLED's  ACLED's External/State Forces was combined with ACLED's State Forces tag, an unknown tag was created that filtered if the actor name was "unknown" or "unidentified." Lastly, a new group was created - Violent Islamist Extremist Groups - from ACLED's inter2 (Political Milita) tag based on these key words for actor1: 'boko', 'katiba', 'islamic state', 'isis', 'jnim', 'iswap', 'isgs', 'al-qa', 'al qa', 'al-sha', 'al sha', 'islamist', 'veo', 'violent extremist', 'ansaroul', 'ansarul', 'ansar', 'al-mo', 'al mo', 'mujao', 'aqim'.

3. Data from the AWSD was imported and then grouped using the ACLED inter code groupings and the values from the previously filtered ACLED dataset. Several incorrect latitude/longitude pairs were manually corrected.

4. These two datasets were then combined. Duplicates were identified if more than one data entry shared all of the following values: event date, country, year, admin1, fatalities. This process was double checked for accuracy and precision.

5. Additional administrative and data cleaning (renaming columns, etc.) techniques were used to finalize the data before uploading to the dashboard.

<b> Resources: </b> 

- [Overseas Security Advisory Council (OSAC)](https://www.osac.gov)
- [GitHub Repository of Data Files](https://www.github.com/ZieglerAE/OSACHumanitarianDashboard)
- [Armed Conflict Location & Event Data Project](https://www.acleddata.com)
- [Aid Worker Security Database](https://www.aidworkersecurity.org)
- [ReliefWeb](https://www.reliefweb.int)
- [Humanitarian Data Exchange](https://data.humdata.org/)


<b>Contact Us: </b>

* Email: osacAF@state.gov

