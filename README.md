# Personnel_Report
This Power BI report offers a comprehensive overview of personnel qualifications, tracking certification statuses, skill levels, and training progress. Interactive visuals and filters enable quick identification of compliance rates, skill gaps, and training needs across the team, enhancing workforce management

*[DAX Measures](https://github.com/AdamClem/Personnel_Report/tree/main/DAX)*

*[Overlay Pages](https://github.com/AdamClem/Personnel_Report/tree/main/Overlay_Pages)*


# Welcome screen
Provides interface for users to navigate through pages while embedded into a SharePoint online site via the Power BI service.

# Schools
Enables a search to find specific qualifications within the unit that are required for different mission sets
Also identifies if the qualified person or population is already deployed or on hand and ready for a deployment

       DAX - List of Mil Scol

# Professional Military Education
This is a key metric for the leadership at the front line level. Professional military education is required for promotion. Limitations to a member's service are based on their rank
        For example - E5 - 10 years and 2 passes for promotion, E6 - 20 years and 2 passes for promotion
This factor makes it important to ensure members are attending their resident courses to be eligible for promotion
Tool tips are used to judge how long a member has been in service, and also how long they have been in this rank
        Promotions are formed by zones based on when a person was promoted and this will allow leadership to anticipate if a member is likely to be placed in the promotion zone

        DAX - PME_Status
        DAX - PME_Count (by completion)
        DAX - Percentage (by status)

# Insignia Authorized to Wear
Each member of the unit is authorized to wear different insignia on their uniform which denotes the level of experience within the explosive ordnance dispoal field
This is transferred to a members final paperwork when they exit service, if a member does not have the insignia properly documented it could inhibit their ability to find explosive ordnance disposal realated work
There is a specific progresssion to each of the insignias
        Basic - complete Naval Explosive Ordnance Disposal course
        Senior - complete 5 years as a basic badge, 180 days in a deployed environment, and completion of supervisor's course at the advanced training center
        Basic - complete 5 years as a senior badge, 180 days in a deployed environment (as a senior badge), and completion of chief's or officer's course at the advanced training center
Tool tips help to quickly display if and when a member is ready for another progression in badge
Additionally it allows leadership to look at members that have met the total 5 year time, but have not met deployment time

# EOD Pays
There are two incentive pays that are due to each member based on mission and training requirements
Hazardous duty pay - each member must work with explosives during the month
Civilian clothing allowance - upon completion of basic insignia requirements, and every three years thereafter

        DAX - CCA_Due Table
        DAX - New Join CCA
        DAX - Elgibility

# Recall
During periods of destructive weather it is often required to provide support to members living in specific geographic areas
The heatmap is used as a drill down to work through zip code to city/state address

        Heirarchy - Addr State / Zip Code / City and State

# Personnel Tempo
One of the problems that the unit ran into was burnout for members that were highly qualified, and they were completing multiple back to back deployments for extended periods of time
This report helps to identify members of the unit by number of trips as well as the number of days they are deployed
The main table contains a tool tip that denotes the amount of deployed time wihtin the specific insigna level that the member has completed

        DAX - Count_Trips

# Physical Fitness - Physical Fitness Test (PFT) and Combat Fitness Test (CFT)
This is another metric that is constantly looked at, especially during the end of periods (Jun & Dec) to ensure 100% completion
The report will help to denote those who need more attention with a more strenuous physical fitness regimen

        Query Work - Append DIM_CFT to DIM_PFT
        DAX - CFT and PFT by class

# Manpower
Military members constantly flow in and out of units, with peak times occuring in the summertime
Communication to headquarters Marine Corps requires issuance of orders to personnel based on shortfalls of rank
Additionally, the unit will begin to change over the next several years adding new occupational specialties witch changes in the overall number of personnel required

        DAX - RankCountTable

# Features
Overlay pages for helping users go use visualizations for their own individual ends
        # Improvements - Develop parameters that allow a user to select which section they are in, and provide a specific view for thier section

Information links to SharePoint online library that houses specificly sensitive personal data. This document library has protections in place and isolated to maintain compliance with government data loss prevention policies

# Data Schema
<img src="https://github.com/AdamClem/Personnel_Report/blob/main/Data_Schema.png" alt="Snowflake schema for EOD personnel report" width="1000" />
