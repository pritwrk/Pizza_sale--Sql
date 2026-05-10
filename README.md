<div align="center">

<img src="[https://readme-typing-svg.demolab.com?font=Playfair+Display&size=38&pause=1000&color=E63946&center=true&vCenter=true&width=600&lines=%F0%9F%8D%95+Pizza+Sales+Analysis;Powered+by+Advanced+SQL](https://readme-typing-svg.demolab.com?font=Playfair+Display&size=38&pause=1000&color=E63946&center=true&vCenter=true&width=600&lines=%F0%9F%8D%95+Pizza+Sales+Analysis;Powered+by+Advanced+SQL)" alt="Typing SVG" />

<p>
  <em>Transforming raw pizza sales data into crisp, actionable business intelligence — one query at a time.</em>
</p>

<p>
  <img src="[https://img.shields.io/badge/Database-MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white](https://img.shields.io/badge/Database-MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)" />
  <img src="[https://img.shields.io/badge/Tool-MySQL%20Workbench-F29111?style=for-the-badge&logo=mysql&logoColor=white](https://img.shields.io/badge/Tool-MySQL%20Workbench-F29111?style=for-the-badge&logo=mysql&logoColor=white)" />
  <img src="[https://img.shields.io/badge/Queries-13%20Business%20Insights-E63946?style=for-the-badge](https://img.shields.io/badge/Queries-13%20Business%20Insights-E63946?style=for-the-badge)" />
  <img src="[https://img.shields.io/badge/Status-Completed-2DC653?style=for-the-badge](https://img.shields.io/badge/Status-Completed-2DC653?style=for-the-badge)" />
</p>

<p>
  <a href="[https://github.com/pritamverma83599-ux/Pizza_sale--Sql/blob/main/Pizza_sales_analysis.sql](https://github.com/pritamverma83599-ux/Pizza_sale--Sql/blob/main/Pizza_sales_analysis.sql)">
    <img src="[https://img.shields.io/badge/View%20SQL%20File-%23121011?style=for-the-badge&logo=github&logoColor=white](https://img.shields.io/badge/View%20SQL%20File-%23121011?style=for-the-badge&logo=github&logoColor=white)" />
  </a>
  <a href="[https://www.linkedin.com/posts/pritam-verma-02721531a_pizzahut-sales-activity-7442049581372268544-5s11](https://www.linkedin.com/posts/pritam-verma-02721531a_pizzahut-sales-activity-7442049581372268544-5s11)">
    <img src="[https://img.shields.io/badge/LinkedIn%20Showcase-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white](https://img.shields.io/badge/LinkedIn%20Showcase-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)" />
  </a>
</p>

</div>

---

## 📖 Project Overview

> **Goal:** Analyze a real-world pizza sales dataset to uncover revenue patterns, customer preferences, and product performance using advanced SQL techniques.

---

## 🌐 Interactive Project Dashboard
> **Live Demo:** Explore the visual analysis and interactive query results directly in your browser.

<a href="[https://pritamverma83599-ux.github.io/Pizza_sale--Sql/](https://pritamverma83599-ux.github.io/Pizza_sale--Sql/)" target="_blank">
  <img src="[https://img.shields.io/badge/View_Live_Project-Click_Here-E63946?style=for-the-badge&logo=googlechrome&logoColor=white](https://img.shields.io/badge/View_Live_Project-Click_Here-E63946?style=for-the-badge&logo=googlechrome&logoColor=white)" alt="Live Demo" />
</a>

---

## 🗄️ Dataset Schema

┌──────────────┐       ┌───────────────┐       ┌──────────────────┐       ┌──────────────┐
│   orders     │       │ order_details │       │    pizzas        │       │ pizza_types  │
│──────────────│       │───────────────│       │──────────────────│       │──────────────│
│ order_id  PK │──────<│ order_id   FK │>──────│ pizza_id      PK │>──────│ pizza_type_id│
│ date         │       │ pizza_id   FK │       │ pizza_type_id FK │       │ name         │
│ time         │       │ quantity      │       │ size             │       │ category     │
└──────────────┘       └───────────────┘       │ price            │       │ ingredients  │
└──────────────────┘       └──────────────┘


---

## 🛠️ Tech Stack & SQL Concepts Used

| Concept | Application |
|---|---|
| ⚡ **Advanced JOINs** | Linking 4 relational tables |
| 📊 **CTEs & Subqueries** | Layered data flows |
| 📈 **Window Functions** | `RANK()`, `SUM() OVER` for rolling revenue |
| 🔢 **Date/Time** | Extracting peak-demand windows |

---

## 📊 Business Challenges & SQL Solutions

<details>
<summary><b>📌 Module 1 — Revenue & Pricing Analysis</b></summary>
Total Revenue, Highest-priced pizza, and Average Order Value analysis.
</details>

<details>
<summary><b>📌 Module 2 — Customer & Order Trends</b></summary>
Order volume, Size preferences, and Peak ordering hours.
</details>

<details>
<summary><b>📌 Module 3 — Top Performer Rankings</b></summary>
Top 5 pizzas by quantity and Revenue distribution by category.
</details>

---

## 💡 Key Business Insights

```text
╔══════════════════════════════════════════════════════════════════╗
║                     EXECUTIVE SUMMARY                            ║
╠══════════════════════════════════════════════════════════════════╣
║                                                                  ║
║   TOP 5 REVENUE LEADERS                                          ║
║   1. Classic Deluxe Pizza                                        ║
║   2. Barbecue Chicken Pizza                                      ║
║   3. Hawaiian Pizza                                              ║
║   4. Pepperoni Pizza                                             ║
║   5. Thai Chicken Pizza                                          ║
║                                                                  ║
║   PEAK DEMAND WINDOWS                                            ║
║   Lunch  -> 12:00 PM - 1:00 PM                                   ║
║   Dinner -> 6:00 PM - 8:00 PM                                    ║
║                                                                  ║
║   CATEGORY REVENUE SHARE                                         ║
║   Classic    ████████████████░░░░  26.91%  [Leader]              ║
║   Supreme    ████████████████░░░░  25.46%                        ║
║   Chicken    ███████████████░░░░░  23.96%                        ║
║   Veggie     ██████████████░░░░░░  23.68%                        ║
║                                                                  ║
║   PREFERRED SIZE                                                 ║
║   Large (L) is the most ordered size across all categories       ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
