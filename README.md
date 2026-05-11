<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Playfair+Display&size=38&pause=1000&color=E63946&center=true&vCenter=true&width=600&lines=%F0%9F%8D%95+Pizza+Sales+Analysis;Powered+by+Advanced+SQL" alt="Typing SVG" />

<p>
  <em>Transforming raw pizza sales data into crisp, actionable business intelligence — one query at a time.</em>
</p>

<p>
  <img src="https://img.shields.io/badge/Database-MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Tool-MySQL%20Workbench-F29111?style=for-the-badge&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Queries-13%20Business%20Insights-E63946?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Completed-2DC653?style=for-the-badge" />
</p>

<p>
  <a href="https://github.com/pritwrk-ux/Pizza_sale--Sql/blob/main/Pizza_sales_analysis.sql">
    <img src="https://img.shields.io/badge/View%20SQL%20File-%23121011?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://www.linkedin.com/posts/pritam-verma-02721531a_check-out-the-full-presentation-below-ugcPost-7459199657945063424-biNC?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFDVat8BUD5mR-4LbLCOagR_seydBq0rFDo" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn%20Showcase-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="https://pritamverma83599-ux.github.io/Pizza_sale--Sql/" target="_blank">
    <img src="https://img.shields.io/badge/Live%20Dashboard-View%20Now-E63946?style=for-the-badge&logo=googlechrome&logoColor=white" />
  </a>
</p>

</div>

---

## 📖 Project Overview

> **Goal:** Analyze a real-world pizza sales dataset to uncover revenue patterns, customer preferences, and product performance using advanced SQL techniques — enabling smarter, data-driven business decisions.

This project covers **13 business logic queries** spanning revenue analysis, demand forecasting, and category-level leaderboards — structured across four key analytical pillars.

---

## 🌐 Interactive Project Dashboard

> Explore the full visual analysis, animated charts, and interactive SQL query results — live in your browser.

<div align="center">

<a href="https://pritamverma83599-ux.github.io/Pizza_sale--Sql/" target="_blank">
  <img src="https://img.shields.io/badge/🚀%20View%20Live%20Project%20Dashboard-Click%20Here-E63946?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Live Demo" />
</a>

</div>

**What's inside the dashboard:**
- 📊 Animated category revenue bar charts
- 🏆 Top 5 pizza leaderboard with rankings
- ⏰ Peak demand window visualizations
- 🗄️ Full schema diagram with PK / FK relationships
- 💻 Syntax-highlighted SQL query viewer (3 switchable tabs)
- 📐 Pizza size preference breakdown

---

## 🗄️ Dataset Schema

```
┌──────────────┐       ┌───────────────┐       ┌──────────────────┐       ┌──────────────┐
│   orders     │       │ order_details │       │    pizzas        │       │ pizza_types  │
│──────────────│       │───────────────│       │──────────────────│       │──────────────│
│ order_id  PK │──────<│ order_id   FK │>──────│ pizza_id      PK │>──────│ pizza_type_id│
│ date         │       │ pizza_id   FK │       │ pizza_type_id FK │       │ name         │
│ time         │       │ quantity      │       │ size             │       │ category     │
└──────────────┘       └───────────────┘       │ price            │       │ ingredients  │
                                               └──────────────────┘       └──────────────┘
```

**Relationships:** `orders` ─ 1:N ─► `order_details` ─ N:1 ─► `pizzas` ─ N:1 ─► `pizza_types`

---

## 🛠️ Tech Stack & SQL Concepts Used

| Concept | Application |
|---|---|
| ⚡ **Advanced JOINs** | Linking orders → order_details → pizzas → pizza_types across 4 tables |
| 📊 **CTEs & Subqueries** | Layered data flows for multi-step calculations |
| 📈 **Window Functions** | `RANK() OVER`, `SUM() OVER` for rankings & rolling revenue |
| 🧹 **Aggregation & Filtering** | `GROUP BY`, `HAVING`, `ORDER BY` for targeted summaries |
| 🔢 **Date & Time Functions** | Extracting hours and dates for peak-demand analysis |

---

## 📊 Business Challenges & SQL Solutions

<details>
<summary><b>📌 Module 1 — Revenue & Pricing Analysis</b></summary>

<br>

| # | Business Question | SQL Approach |
|---|---|---|
| 1 | What is the **total revenue** generated? | `SUM(price * quantity)` across all orders |
| 2 | Which is the **highest-priced pizza**? | `ORDER BY price DESC LIMIT 1` |
| 3 | What is the **average order value**? | Total revenue ÷ total distinct orders |

**Outcome:** Established a revenue baseline of **$817,860** and identified the premium product tier (The Greek Pizza at $35.95).

</details>

<details>
<summary><b>📌 Module 2 — Customer & Order Trends</b></summary>

<br>

| # | Business Question | SQL Approach |
|---|---|---|
| 4 | What is the **total number of orders** placed? | `COUNT(DISTINCT order_id)` |
| 5 | Which **pizza size** do customers prefer most? | `GROUP BY size ORDER BY COUNT DESC` |
| 6 | What are the **peak ordering hours**? | `HOUR(time)` extracted and grouped |

**Outcome:** Pinpointed lunch (12–1 PM) and dinner (6–8 PM) as the highest-demand windows. **Large** is the most ordered size.

</details>

<details>
<summary><b>📌 Module 3 — Top Performer Rankings</b></summary>

<br>

| # | Business Question | SQL Approach |
|---|---|---|
| 7 | What are the **Top 5 pizzas** by quantity sold? | `SUM(quantity) GROUP BY pizza_id LIMIT 5` |
| 8 | How are sales **distributed by category**? | `GROUP BY category` with percentage share |
| 9 | Which category **generates the most revenue**? | Revenue aggregated per category |

**Outcome:** Classic category dominates revenue at **26.91%** of total sales.

</details>

<details>
<summary><b>📌 Module 4 — Advanced Business Intelligence</b></summary>

<br>

| # | Business Question | SQL Approach |
|---|---|---|
| 10 | How has **revenue grown** cumulatively over time? | `SUM(revenue) OVER (ORDER BY date)` rolling window |
| 11 | What is the **average daily order volume**? | CTE → avg of daily order counts |
| 12 | Who are the **Top 3 pizzas within each category**? | `RANK() OVER (PARTITION BY category)` |
| 13 | What % of revenue does each **category contribute**? | Subquery for total ÷ category revenue |

**Outcome:** Rolling revenue curves reveal sustained growth with clear seasonal dips — opportunities for targeted promotions.

</details>

---

## 💡 Key Business Insights

```
╔══════════════════════════════════════════════════════════════════╗
║                     EXECUTIVE SUMMARY                           ║
╠══════════════════════════════════════════════════════════════════╣
║                                                                  ║
║  🏆  TOP 5 REVENUE LEADERS                                       ║
║      1. Classic Deluxe Pizza                                     ║
║      2. Barbecue Chicken Pizza                                   ║
║      3. Hawaiian Pizza                                           ║
║      4. Pepperoni Pizza                                          ║
║      5. Thai Chicken Pizza                                       ║
║                                                                  ║
║  ⏰  PEAK DEMAND WINDOWS                                         ║
║      Lunch  → 12:00 PM – 1:00 PM                                 ║
║      Dinner → 6:00 PM – 8:00 PM                                  ║
║                                                                  ║
║  📦  CATEGORY REVENUE SHARE                                      ║
║      Classic    ████████████████░░░░  26.91%  ← Leader          ║
║      Supreme    ████████████████░░░░  25.46%                    ║
║      Chicken    ███████████████░░░░░  23.96%                    ║
║      Veggie     ██████████████░░░░░░  23.68%                    ║
║                                                                  ║
║  📐  PREFERRED SIZE                                              ║
║      Large (L) is the most ordered size across all categories    ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

---

## 📂 Repository Structure

```
Pizza_sale--Sql/
│
├── 📄 Pizza_sales_analysis.sql    ← All 13 business logic queries
├── 📄 index.html                  ← Interactive live dashboard (GitHub Pages)
└── 📄 README.md                   ← Project documentation & insights
```

---

## 🚀 How to Run

```sql
-- Step 1: Clone the repository
git clone https://github.com/pritamverma83599-ux/Pizza_sale--Sql.git

-- Step 2: Open MySQL Workbench and connect to your local server

-- Step 3: Import the dataset tables (orders, order_details, pizzas, pizza_types)

-- Step 4: Open and execute Pizza_sales_analysis.sql
-- Each query is labelled with its business question for easy navigation
```

> **To activate the Live Dashboard:** Rename `pizza_sales_project.html` to `index.html`, push it to the root of your repo, then go to `Settings → Pages → Deploy from branch (main / root)`.

---

## 🔗 Professional Showcase

<div align="center">

📊 Full data visualizations and presentation slides available on LinkedIn:

<a href="https://www.linkedin.com/posts/pritam-verma-02721531a_check-out-the-full-presentation-below-ugcPost-7459199657945063424-biNC?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFDVat8BUD5mR-4LbLCOagR_seydBq0rFDo" target="_blank">
  <img src="https://img.shields.io/badge/View%20Full%20Presentation%20on%20LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Post" />
</a>

</div>

---

<div align="center">

**📬 Let's Connect**

If you found this project useful, consider starring ⭐ the repository and following for more data projects!

<a href="https://github.com/pritamverma83599-ux">
  <img src="https://img.shields.io/badge/GitHub-pritamverma83599--ux-181717?style=for-the-badge&logo=github" />
</a>
&nbsp;
<a href="https://www.linkedin.com/in/pritam-verma-02721531a" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-Pritam%20Verma-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
</a>

<br><br>

<sub>Crafted with ❤️ and a lot of SQL by <a href="https://github.com/pritamverma83599-ux"><b>Pritam Verma</b></a></sub>

</div>
