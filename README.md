# Play Store App Review Analysis Dashboard

### Explore app performance, category popularity and user ratings with Power BI.

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Power Query](https://img.shields.io/badge/Power_Query-Data_Preparation-217346)
![DAX](https://img.shields.io/badge/DAX-Analytics-753AA6)
![Data Modeling](https://img.shields.io/badge/Data_Modeling-Relationships-326CE5)

**Author:** Swapnil Sudhakar Pathare  
**Data source:** AlmaBetter course materials  
**Project type:** Business Intelligence / Data Analytics

[View Project Report](Play_Store_Data_Analysis.pdf) · [Download Power BI File](Playstore-App-Review-Analysis-Dashboard.pbix)

## Project Overview

This project explores Play Store app data through a five-page Power BI dashboard. It compares app categories, installations, ratings, review activity and app cost to make the dataset easier to understand visually.

Viewers can start with the headline metrics, compare categories, explore popular apps and examine how ratings relate to review volume. The project demonstrates dashboard design, KPI presentation and visual analysis for a data analytics portfolio.

![Play Store dashboard overview](<Playstore_app_review_analysis_images/1. Count_app_by_category.png>)

## Tech Stack

| Technology | Role in the project |
| --- | --- |
| **Power BI Desktop** | Build and explore the multi-page dashboard |
| **Power Query** | Data preparation layer for importing and transforming source data |
| **DAX** | Measures referenced in the report, including Total Installs, Total Reviews, No Of Apps and Avg Review |
| **Data Modeling** | Organize app and user-review tables and their relationships |
| **File formats** | `.pbix` for the Power BI project, `.pdf` for the report, `.png` for dashboard previews and `.md` for documentation |

The archive contains the report project and presentation assets. Original source datasets and their file formats are not included; detailed Power Query steps and DAX formulas are not documented here.

## Data Source

The dataset was provided through my **AlmaBetter course** and used for this learning and portfolio project.

The project model includes two tables:

| Table | Purpose |
| --- | --- |
| **Play Store Data** | App information used to analyze categories, installs, ratings, reviews and app cost |
| **User Reviews** | User-review information associated with apps |

**Acknowledgment:** Thanks to AlmaBetter for the course learning resources and dataset. The original datasets may be needed to refresh the report. Course attribution does not establish permission to redistribute the underlying data.

## Features and Highlights

- **KPI overview:** Summarizes installations, reviews, app count and the displayed average-review metric.
- **Category comparison:** Shows how app counts and installation volume differ across categories.
- **Top-app analysis:** Presents installation shares for the displayed top 15 apps.
- **Rating distribution:** Groups apps by rating to help viewers explore the dataset's rating profile.
- **Treemap comparisons:** Shows relative category contributions to app cost and total reviews.
- **Rating-versus-reviews analysis:** Uses a scatter plot to compare app ratings with review volume.
- **Consistent visual layout:** Uses purple styling, repeated KPI cards and navigation labels across report pages.
- **Accessible project previews:** Includes screenshots and a PDF so viewers can review the work without opening Power BI.

## Dashboard at a Glance

| KPI | Value displayed |
| --- | ---: |
| Total Installs | **168bn** |
| Total Reviews | **5bn** |
| Total Apps | **9,639** |
| Avg Review | **444.15K** |

`bn` means billion; `K` means thousand. These are the rounded values displayed in the dashboard, not live Google Play market totals. Check the underlying measures and filters before using them for further calculations.

## Dashboard Pages

### 1. App Count by Category

Compare the number of apps across categories using a bar chart and an area chart.

**Highlight:** FAMILY has the highest displayed app count at **1,972**, followed by GAME at **1,144** and TOOLS at **843**.

### 2. Category Installs and Average Ratings

Compare the top 10 categories by installations and explore the category-level rating/install comparison.

**Highlight:** GAME leads the displayed installation chart at **35.1bn**, followed by COMMUNICATION at **32.6bn**.

![Category installs and ratings](<Playstore_app_review_analysis_images/2. Avg_rating_and_total_install_by_category.png>)

### 3. Top Apps and Rating Distribution

Explore installation shares for 15 apps and see how apps are distributed across rating groups.

**Highlight:** Featured apps include Subway Surfers, Google Drive, Instagram and WhatsApp. Installation-share percentages refer to the displayed top-app subset.

![Top apps and rating distribution](<Playstore_app_review_analysis_images/3. No_of_apps_by_rating.png>)

### 4. App Cost and Reviews by Category

Use treemaps to compare category contributions to Total App Cost and Total Reviews.

**Highlight:** FINANCE, FAMILY and LIFESTYLE occupy large areas in the cost treemap. GAME has the largest visible area in the reviews treemap.

![App cost and reviews by category](<Playstore_app_review_analysis_images/4. Total_app_cost_and_reviews_by_category.png>)

### 5. Average Rating vs. Total Reviews

Compare app ratings with review volume using a scatter plot.

**Highlight:** High-review observations appear mainly around ratings of **4.0–4.6**. This is a visual observation and does not establish causation.

![Average rating versus total reviews](<Playstore_app_review_analysis_images/5. Avg_rating_and_total_reviews_by_app_and_rating.png>)

## Example: How a Viewer Can Use This Dashboard

**Question: “Which category has more apps, and which attracts more installations?”**

1. Open the overview page and compare app counts: FAMILY leads with **1,972** apps.
2. Move to the category-installation view: GAME leads with **35.1bn** displayed installs.
3. Compare the two findings: the category with the most app records is different from the category with the most installation volume.
4. Explore ratings and reviews for additional context before drawing a business conclusion.

This example shows how the dashboard separates **app availability** from **installation activity**. Neither metric alone establishes profitability.

## Project Files

| File / folder | Contents |
| --- | --- |
| `Playstore-App-Review-Analysis-Dashboard.pbix` | Power BI report project |
| `Play_Store_Data_Analysis.pdf` | Project report and dashboard walkthrough |
| `Playstore_app_review_analysis_images/` | Five dashboard screenshots in report order |
| `README.md` | Project overview, features and usage instructions |

## How to Open the Project

1. Download or clone this repository and extract it if downloaded as a ZIP.
2. Open **`Playstore-App-Review-Analysis-Dashboard.pbix`** in Power BI Desktop.
3. Explore the five report pages using the page tabs.
4. For a quick static preview, open the PDF or the screenshots in this README.
5. To refresh the data, obtain the original course datasets and update the source paths in **Data source settings** as needed.

## Interpretation Notes

- The rating distribution includes a `NaN` group, indicating missing or invalid ratings that need review.
- The category comparison chart displays rating units in billions; correct that formatting before interpreting its rating values.
- App cost is not revenue, and installation totals are not unique users.
- The supplied rating/review visuals compare records rather than change over time. No sentiment-analysis result is claimed here.

## Skills Demonstrated

**Power BI dashboard design · KPI communication · Category comparisons · Data visualization · App performance analysis · Analytical storytelling**

---

Created by **Swapnil Sudhakar Pathare** using a dataset provided through the **AlmaBetter course**.
