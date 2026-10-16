# Play Store Data Analysis | Power BI

Explore app categories, installation volume, ratings and review activity through a five-page Power BI report.

**Author:** Swapnil Sudhakar Pathare  
**Tool:** Microsoft Power BI Desktop  
**Project file:** `4 project (1).pbix`

[Read the project report](docs/Play_Store_Data_Analysis.pdf)

![Data overview](screenshots/01-overview.png)

## Project overview

This project presents a visual analysis of a Play Store dataset. It brings together headline metrics, category comparisons, top-app installation shares, rating distributions and review-volume comparisons in a consistent dashboard layout.

The documentation is based on five supplied dashboard screenshots and the supplied Power BI application view. Dataset preparation steps, DAX formulas and raw-data calculations have not been independently verified.

## Questions explored

- Which categories contain the most app records?
- Which categories account for the highest installation volume?
- How are installations distributed among the displayed top 15 apps?
- How are ratings distributed, including missing ratings?
- How do category cost and review contributions compare?
- Where do apps sit when rating is compared with review volume?

## Dashboard KPIs

| Displayed metric | Displayed value | Interpretation |
| --- | ---: | --- |
| Total Installs | 168bn | Rounded dashboard aggregate; not unique users |
| Total Reviews | 5bn | Rounded dashboard aggregate |
| Total Apps | 9,639 | Card value; uniqueness/counting logic unverified |
| Avg Review | 444.15K | Card value; formula and denominator unverified |

These values describe the report as captured. They are not live Google Play totals. Do not recompute one card from another without checking the underlying measures, filters and rounding.

## Dashboard walkthrough

### 1. Data overview

Compares app counts by category using a horizontal bar chart and an area chart.

| Category | Displayed app count |
| --- | ---: |
| FAMILY | 1,972 |
| GAME | 1,144 |
| TOOLS | 843 |
| MEDICAL | 463 |
| BUSINESS | 460 |

FAMILY has the largest displayed app count. This reflects dataset coverage, not proof of the most profitable category. The area chart compares categories; it is not a time series.

### 2. Category installs and ratings

![Category installs](screenshots/02-category-installs.png)

- GAME leads the installs chart at **35.1bn**.
- COMMUNICATION follows at **32.6bn**.
- TOOLS shows **11.5bn** and PHOTOGRAPHY **10.1bn**.
- A combination chart compares category-level average ratings and total installs.

**Display limitation:** the rating axis is formatted in billions, and a category labeled `1.9` is visible. Check number formatting and category values before interpreting that chart.

### 3. Top apps and rating distribution

![Top apps and ratings](screenshots/03-apps-and-ratings.png)

The pie chart presents installations for 15 apps, including Subway Surfers, Google Drive, Instagram and WhatsApp. The largest visible slice is labeled **6bn (11.32%)**. Its percentages refer to the displayed subset, not all dataset installations.

The donut chart groups apps by rating. A **NaN group (15.11%)** is visible and should be treated as missing/invalid pending data validation. Several count labels round to `0K`; exact whole-number labels would make the chart clearer.

### 4. Category cost and review composition

![Cost and reviews](screenshots/04-cost-and-reviews.png)

- FINANCE, FAMILY and LIFESTYLE occupy large areas in the Total App Cost treemap.
- GAME has the largest visible area in the Total Reviews treemap; COMMUNICATION and SOCIAL are also prominent.

The screenshot does not expose exact treemap values. Total App Cost should not be described as revenue: its currency, aggregation and outlier treatment need confirmation. The lower chart is partially cropped in the supplied image.

### 5. Ratings versus reviews

![Ratings and reviews](screenshots/05-ratings-and-reviews.png)

The scatter plot compares average rating with total reviews. High-review observations cluster around ratings of approximately **4.0-4.6**, while many observations have low review totals across the rating range.

This visual alone does not prove correlation or causation. Despite the navigation label “Rating & Review Trends,” the supplied visuals do not show a time axis and cannot establish temporal growth. The screenshots also do not establish sentiment-analysis results.

## Observed data model

| Table | Visible column count | Role indicated by its name |
| --- | ---: | --- |
| Play Store Data | 22 | App-related data |
| User Reviews | 5 | Review-related data |

The supplied application view shows a **limited many-to-many relationship** between these tables. Its join key and filter direction have not been verified. Validate uniqueness and filter behavior before interpreting combined measures; consider a unique app dimension if supported by the source data.

## Repository contents

```text
.
├── README.md
├── 4 project (1).pbix          # Add the original supplied project file
├── docs/
│   └── Play_Store_Data_Analysis.pdf
└── screenshots/
    ├── 01-overview.png
    ├── 02-category-installs.png
    ├── 03-apps-and-ratings.png
    ├── 04-cost-and-reviews.png
    └── 05-ratings-and-reviews.png
```

The documentation bundle contains the PDF, README and screenshots. Add your original PBIX alongside README.md; the PBIX is not included in this bundle.

## How to open

1. Download or clone this repository.
2. Open `4 project (1).pbix` in Power BI Desktop.
3. Explore the five report pages and inspect the active filters.
4. If refreshing, provide the original source datasets and update paths through **File → Options and settings → Data source settings** as needed.
5. Inspect relationships and measure definitions before trusting refreshed totals.

A PDF or screenshot provides a static preview. Use the PBIX in Power BI Desktop for report interactions. Original source datasets may be required for refresh.

## Quality checks and improvements

- Verify app uniqueness, repeated app records and the definitions of the four KPI cards.
- Confirm numeric conversion of installs, reviews, ratings and prices; document any cleaning actually performed.
- Handle missing ratings explicitly instead of leaving `NaN` in the legend.
- Correct rating-axis display units and investigate category values such as `1.9`.
- Test the many-to-many relationship for unexpected filtering or aggregation.
- Replace crowded pie/donut labels with readable counts, tooltips or ranked bars.
- Standardize labels such as “Total Reviews” and “User Feedback.”
- Document dataset provenance, collection period, currency and permitted reuse.

These are recommended next steps, not claims that these changes are already implemented.

## Scope and attribution

Evidence: five user-supplied dashboard screenshots, arranged in report order, and the supplied Power BI application description. Screenshots are preserved as supplied. Raw datasets and DAX definitions were not audited; this report should be read as a portfolio demonstration rather than a current market assessment.

Dataset source and license were not provided in the reviewed material. Add the verified original source and its license before redistributing underlying data. No software or dataset license is asserted by this README.
