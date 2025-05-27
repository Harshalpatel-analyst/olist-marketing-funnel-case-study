# Marketing Funnel Analysis with Google Sheets

## 📋 Project Overview

This repository contains a detailed case study of **Marketing Funnel Analysis** performed on a dataset provided by [Olist](https://www.olist.com), Brazil’s largest department store marketplace. The analysis focuses on understanding the flow of Marketing Qualified Leads (MQLs) through the sales funnel, from initial contact to closed deals, using Google Sheets.

### 🔍 Primary Goal

* Demonstrate how to perform common analyses on a marketing funnel.

### 🎯 Secondary Goal

* Practice and showcase advanced Google Sheets skills: formulas, pivot tables, and charts.

---

## 📊 Dataset Description

The project leverages two linked datasets:

1. **MQL Dataset**

   * Contains information on 8,000 randomly sampled Marketing Qualified Leads (MQLs) who requested contact from June 1, 2017, to June 1, 2018.
   * Features include `lead_id`, `seller_id`, `lead_origin`, `lead_type`, `business_segment`, `date_contacted`, and anonymized behavior profiles.

2. **Closed Deals Dataset**

   * Captures outcomes of MQLs that progressed to the sales stage where deals were either won or lost.
   * Contains `seller_id`, `date_closed`, and `deal_status` ("Won" or "Lost").

These datasets can also be joined with the Brazilian E-Commerce Public Dataset by Olist via `seller_id` to enrich the analysis with order and revenue information.

---

## 📈 Key Analysis Questions & Findings

| Question                                              | Finding                                      |
| ----------------------------------------------------- | -------------------------------------------- |
| Which Lead Origin generates the most leads?           | Paid Search & Organic Search                 |
| Which Lead Origin generated the most closed deals?    | Paid Search & Organic Search                 |
| Average time from first contact to closed deal (days) | \~49 days                                    |
| Month-over-Month lead generation trend                | Leads doubled from 2017 to 2018              |
| Lead Type with highest closed deals                   | Online Medium                                |
| Business Segment with highest closed deals            | Home Decor, Health & Beauty, Car Accessories |

---

## 🛠 Analysis Workflow

All analysis was performed in Google Sheets. The core steps are:

1. **Data Preparation**

   * Imported both CSV files (`mql_data.csv`, `closed_deals.csv`) into separate tabs.
   * Performed a **JOIN** (VLOOKUP) to link closed-deal outcomes to MQL records by `seller_id`.

2. **Pivot Tables & Charts**

   * **Lead Origin Analysis**

     * Created a pivot table summarizing total MQLs and won deals by `lead_origin`.
     * Added a combo chart (bars + line) to compare volumes and conversion rates.

   * **Monthly Trends**

     * Built a pivot table with `month_contacted` as rows and count of MQLs as values, broken down by `lead_origin`.
     * Added a stacked bar chart to visualize MoM volumes by origin.
     * Created another pivot to calculate average `days_to_close` by month and visualized it with a line chart.

   * **Lead Type & Business Segment**

     * Generated pivot tables for `lead_type` and `business_segment` against count of closed deals.
     * Added bar charts to highlight top-performing categories.

3. **Recommendations**

   * Based on the findings, defined an **Ideal Customer Profile (ICP)** and proposed targeted marketing strategies for high-value segments.

---


## 🤝 Acknowledgments

* **Olist** for providing the anonymized marketing funnel data.
* **Data School** community for inspiration on analytical techniques.



