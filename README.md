# PowerBI-Crisis-Analysis-Spatial-Modeling
Power BI Dashboard investigating the intersection of infrastructure efficiency and public safety in Maji Ndogo. Features custom Shape Maps, Star Schema modeling, and time-series analysis of crime trends vs. water queue metrics.

- Project Overview
This repository contains a comprehensive data audit of the water crisis in Maji Ndogo. The project transitions from raw SQL data to a high-level executive dashboard designed to help government officials prioritize infrastructure projects based on two critical factors: Service Efficiency and Citizen Safety.

- The Technical Challenge
The primary challenge of this project was the spatial visualization of a fictional territory. Since Maji Ndogo does not exist in standard GIS databases, I implemented a custom solution by layering a hand-drawn topographical background (MD_Map.png) with a custom-engineered TopoJSON layer (MD_provinces.json) to create a fully interactive Shape Map.

- Data Architecture
I implemented a Star Schema to manage relationships between disparate datasets:

1, Fact Table 1 (Infrastructure): Md_summary - 60,000+ records of water source visits and queue metrics.

2, Fact Table 2 (Safety): Md_queue_related_crime - 70,000+ records of safety incidents at water points.

3, Dimension Table: Location - The central SQL-derived table that ensures synchronized filtering across all visuals via location_id.

- Key Investigative Findings
The 3,000-Person Plateau: Through scatter plot analysis, I identified that average queue times stabilize once a source serves more than 3,000 people. This suggests a systemic "breaking point" where citizens opt for more dangerous, unmonitored sources (like rivers) due to unmanageable wait times.

The "Hour of Danger": By correlating crime timestamps with queue data, a significant spike in violent crime was identified between 4:00 AM and 7:00 AM.

Gendered Burden: Data confirmed that female citizens bear the brunt of the crisis, making up the majority of victims during the high-risk early morning queuing hours.

- Repository Contents
Maji_Ndogo_Report.pbix: The master Power BI file.

A, /Data: Cleaned CSV files used for the final model.

B, /Shapefiles: The JSON and PNG files used for the custom spatial modeling.

- Skills Demonstrated
1, Advanced Power BI: Custom Shape Maps, Slicers, and Tooltip interactions.

2, Data Modeling: Star Schema implementation and relationship management.

3, Analytical Thinking: Identifying correlations between infrastructure failure and social safety.

This project was completed as part of an advanced data analytics simulation to demonstrate the power of BI in solving complex humanitarian crises.
