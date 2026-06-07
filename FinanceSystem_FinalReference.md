# Personal Finance Management System
## Complete Project Reference — Final Version

---

## 1. Who Is This For?

This project was built **by one person, for one person — me.**

I am an ERP / Business Intelligence engineering student based in Tunisia. I had a real personal problem: I needed to understand where my money was going, track my income sources, and take control of my financial habits. No existing app felt right, so I decided to build my own.

The project started from a genuine personal need. That makes it better than anything built for an imaginary user.

---

## 2. Why This Project Exists

### The Personal Reason
I needed a tool to:
- See exactly where I was spending money
- Track every income source I had
- Understand my financial behavior over time
- Make better decisions with limited resources

### The Professional Reason
As an ERP/BI student, I wanted a real project that covers what I actually study — not a tutorial clone, not a fake dataset exercise. A real system, built from scratch, that I use every day, that grows with my skills.

### The Long-Term Vision
The project follows a clear three-stage sequence:

1. **Personal use first** — build it, use it daily, fix real problems with my own finances
2. **Portfolio second** — once solid, it demonstrates full-stack + data engineering + BI + ML skills to employers
3. **Product maybe later** — share with friends, grow organically, potentially sell

These three stages are sequential. Not parallel. One at a time.

---

## 3. What This System Is

A **full-stack personal finance decision-support platform** that:
- Collects financial data through a web application (mobile-responsive)
- Synchronizes data across all devices
- Transforms raw transactions into analytical models
- Visualizes insights through dashboards
- Uses machine learning to predict and optimize financial behavior
- Evolves into a complete data engineering pipeline

This is not a simple expense tracker.
It is a complete, data-driven financial management ecosystem built progressively, one phase at a time.

---

## 4. System Architecture Overview

```
[Web App - React (responsive, works on mobile)]
              |
              v
    [Backend API - FastAPI]
              |
              v
   [PostgreSQL - Operational DB]
              |
              v
     [ETL - dbt + Airbyte]
              |
     [Airflow - Orchestration]
              |
              v
  [Data Warehouse - PostgreSQL -> Snowflake]
              |
              v
     [BI - Power BI Dashboards]
              |
        [Kafka - Streaming]
              |
              v
  [ML - scikit-learn + MLflow]
              |
              v
  [Optional - Databricks / Delta Lake / Spark]
```

---

## 5. Stack Philosophy

Every tool chosen follows three rules:
1. **Market demand** — engineers get hired for knowing it
2. **Reliability at scale** — will not break when the system grows
3. **Right tool for the right job** — not the trendiest, the most appropriate

Tools studied in school are kept where they genuinely belong.
Where a better, more in-demand tool exists, it replaces the older one.

---

## 6. Final Technology Stack

### Core Tools - Phase 1

| Layer | Tool | Why |
|---|---|---|
| Frontend Web | React | Most demanded frontend skill worldwide, huge ecosystem |
| Backend API | FastAPI (Python) | Async, lightweight, perfect for data-heavy applications |
| Operational DB | PostgreSQL | Most reliable open-source RDBMS, scales well, widely used |
| DB Client | DBeaver | Universal DB client, works with PostgreSQL, Snowflake, everything |

### Data Engineering Tools - Phase 3+

| Layer | Tool | Why |
|---|---|---|
| ETL Transformations | dbt | Modular SQL transformations, version-controlled, industry standard |
| Data Integration | Airbyte | Modern open-source data integration, replaces Talend/SSIS |
| Orchestration | Apache Airflow | Industry standard for pipeline scheduling and monitoring |
| Data Warehouse (start) | PostgreSQL (star schema) | Free, sufficient for personal scale |
| Data Warehouse (scale) | Snowflake | Cloud-native, elastic, widely used in enterprises |

### Business Intelligence - Phase 4

| Layer | Tool | Why |
|---|---|---|
| BI Platform | Power BI | Most widely used enterprise BI tool, connects to everything |

### Real-Time and Streaming - Phase 5

| Layer | Tool | Why |
|---|---|---|
| Event Streaming | Apache Kafka | Gold standard for real-time pipelines in finance and tech |

### Machine Learning - Phase 6

| Layer | Tool | Why |
|---|---|---|
| Classical ML | scikit-learn | Covers 90% of practical ML tasks cleanly |
| Experiment Tracking | MLflow | Standard for tracking, deploying, and monitoring ML models |

> PyTorch added only if classical ML is genuinely insufficient. Not a priority.

### Advanced Platform - Optional

| Layer | Tool | Why |
|---|---|---|
| Data Lake | Delta Lake (Databricks) | ACID transactions on large-scale storage |
| Processing Engine | Apache Spark | Distributed data transformation at enterprise scale |
| Full Platform | Databricks | Hottest data engineering skill in France and across Europe |

---

## 7. Tools Replaced and Why

| Studied Tool | Replaced By | Reason |
|---|---|---|
| SSIS | dbt + Airbyte | Cloud-native, modern, actively growing market demand |
| Talend | dbt + Airbyte | dbt is the standard for SQL transformations, Airbyte for integration |
| SSAS | Power BI + proper DWH schema | Power BI makes SSAS unnecessary for this scale |
| SSMS | DBeaver | Works with PostgreSQL and every other DB, not tied to SQL Server |
| PgBadger | - | Kept for personal PostgreSQL tuning only, not a headline skill |

> **Important:** The concepts behind these tools are fully transferable. ETL is ETL. Orchestration is orchestration. OLAP is OLAP. Knowing the older tools and moving to better ones is a strength — it means you can work in both legacy and modern environments.

---

## 8. The Flutter Decision

Flutter is not hard. The timing is wrong.

**Why Flutter is skipped for now:**
- It uses Dart — a completely new language on top of everything else being learned
- Phase 1 already introduces React (JavaScript), FastAPI (Python), and PostgreSQL (SQL) simultaneously
- A responsive React web app works perfectly on any phone browser
- Adding Flutter now means learning 4 technologies at once instead of 3
- Momentum matters more than a native mobile feel at this stage

**When Flutter gets added:**
- After Phase 1 is fully working and in daily use
- After React, FastAPI, and PostgreSQL feel comfortable
- When native mobile features (push notifications, offline mode) are genuinely needed

Flutter will still be there in 3 months. Build the web app first.

---

## 9. The Rules for Using AI Coding Tools

AI coding assistants (Cursor, Windsurf, Trae, and others) are allowed and encouraged.
They accelerate development significantly.

But they carry one real risk: reading carefully at first, then vibing too hard, copying without understanding, then hitting a wall that cannot be debugged.

**Three rules. Applied every single time AI generates code:**

1. **Read it line by line** — explain to yourself what each part does, even roughly
2. **Ask the AI to explain** any line or block that is not clear before using it
3. **Never copy a full file blindly** — always know what that file is responsible for

**What AI can write:**
- React form components and table views
- FastAPI CRUD endpoints
- PostgreSQL table creation scripts
- Basic dbt models
- Boilerplate Airflow DAG structure

**What must be written or deeply understood personally:**
- The core data model — what tables exist, what relationships, and why
- Any logic that touches money — calculations, aggregations, totals
- The star schema design — this is the heart of the BI portfolio
- Authentication and session logic

> JavaScript and Python are the most readable languages that exist. AI-generated code in these languages reads almost like English after a few days. No need to memorize syntax — just understand the logic.

---

## 10. Phase-by-Phase Breakdown

---

### Phase 1 - Core Application

**Goal:** A working app that records real financial behavior. Nothing more.

**Tools:**
- React (web frontend — responsive, works on mobile browser)
- FastAPI (backend API)
- PostgreSQL (operational database)
- DBeaver (database client)

**What gets built:**
- User registration and secure login
- Add income transactions — amount, source, date, description, tags
- Add expense transactions — amount, category, date, description, tags
- Default categories: food, coffee, transport, gifts, going out, and more
- View full transaction history

**What does NOT get built in Phase 1:**
- No charts or dashboards
- No real-time sync
- No profiling or onboarding
- No native mobile app
- No data warehouse

**Why it matters:**
Without real data, nothing else works. This phase produces the raw material for every future phase. The goal is an app that gets opened every day and actually used.

**The only rule:** Keep it ruthlessly simple. Working and usable beats perfect and unfinished.

**Phase 1 is done when:** A transaction can be added from a web form, saved to PostgreSQL, and seen in a list. That is it.

---

### Phase 1 v2 - Adaptive Onboarding and User Profiling

**Status:** Planned — built after Phase 1 core has been in daily use for at least 30 days.

**Goal:** Make the app feel personal from minute one by adapting the interface to each user's real life situation.

**What gets built:**
- A simple onboarding screen after registration with profile checkboxes
- Each user selects all that apply to their life situation
- The app loads a matching category set based on their profile
- Categories adapt to who the person actually is

**Profile Options (multi-select — not exclusive):**

| Profile | Auto-loaded Categories |
|---|---|
| Student | Tuition, books, transport, food, going out |
| In a relationship | Dates, gifts, trips, shared expenses |
| Married | Bills, rent, family expenses, groceries |
| Has a salary | Monthly salary tracking, work transport |
| Freelancer | Multiple income sources, client payments |
| Has a family | Children expenses, school fees, healthcare |

**Technical implementation:**
- One extra table in PostgreSQL: user_profile with boolean columns per life situation
- Onboarding: 2-3 screens maximum, checkbox selection
- Backend: profile stored at registration, category set loaded dynamically
- Combining profiles merges their category sets automatically

**Why it matters:**
A student and a married person have completely different financial lives. Showing the same generic interface to both is lazy design. This feature makes the app feel built for the actual person using it.

**Why it waits:**
Phase 1 must stay simple enough to get built and used quickly. Profiling designed after real usage is better than profiling designed from assumptions.

**Impact on future phases:**
User profile becomes a powerful dimension in the data warehouse — enabling ML clustering by life situation, not just by spending category.

---

### Phase 2 - Cross-Platform Synchronization

**Goal:** One transaction added on any device appears everywhere within seconds.

**Tools:**
- FastAPI (REST + WebSockets)
- Kafka (lightweight introduction)
- React Query / polling (web sync)

**What gets built:**
- All devices connected to the same backend
- Near real-time synchronization
- Optional WebSocket layer for instant updates

**Why it matters:**
Multiple devices must feel like one connected tool, not separate apps with separate data.

---

### Phase 3 - Data Modeling and Data Warehouse

**Goal:** Transform raw transactions into an analytics-ready structure.

**Tools:**
- PostgreSQL (star schema data warehouse)
- dbt (SQL transformations)
- Airbyte (data integration)
- Apache Airflow (pipeline orchestration)

**What gets built:**
- Fact table: transactions
- Dimension tables: date, category, income source, user
- ETL pipeline: extract -> clean -> transform -> load
- Airflow DAGs to schedule and monitor all jobs

**Star Schema:**
```
         [Dim: Date]
              |
[Dim: User]-[Fact: Transactions]-[Dim: Category]
              |
     [Dim: Income Source]
```

**Why it matters:**
This is the core of ERP/BI engineering. A properly designed data warehouse makes every analytical query fast, simple, and powerful. This is what BI professionals build in enterprise systems — applied here at personal scale.

---

### Phase 4 - Business Intelligence and Dashboards

**Goal:** Visual insights from analytical data for real decision-making.

**Tools:**
- Power BI (dashboards and reports)
- PostgreSQL / Snowflake (data source)

**What gets built:**
- Spending vs income trends
- Top expense categories
- Monthly and yearly financial behavior
- Income sources breakdown
- Personal financial KPIs

**Example insights this phase unlocks:**
- "I spent 40% of my budget on food this month"
- "My income dropped 20% in Q3"
- "Going out expenses spike every Friday"
- "One income source covers 70% of my total income"

**Why it matters:**
Numbers in a database mean nothing until visualized. This phase turns months of data into clear, actionable financial stories.

---

### Phase 5 - Real-Time Data Pipeline

**Goal:** Dashboards reflect new transactions within seconds.

**Tools:**
- Apache Kafka (event streaming)
- Apache Spark via Databricks (stream processing)
- Apache Airflow (orchestration)
- Snowflake (streaming ingestion target)

**What gets built:**
```
New transaction -> Kafka event -> Spark processes -> Snowflake stores -> Power BI reflects
```

**Why it matters:**
A dashboard showing last week's data is useful. A dashboard showing today's data is powerful.

---

### Phase 6 - Machine Learning and Advanced Analytics

**Goal:** Predict, detect, and recommend based on real historical behavior.

**Tools:**
- scikit-learn (classical ML models)
- MLflow on Databricks (experiment tracking and model deployment)
- FastAPI (serve predictions back to the app)
- dbt + Spark (feature engineering)

**What gets built:**
- Spending anomaly detection — alerts when behavior is unusual
- Monthly expense forecasting — predicts next month's spending
- Behavioral clustering — identifies recurring spending patterns
- Personalized recommendations — suggests where to improve

**Why the data will be real:**
Unlike most ML projects that use borrowed or synthetic datasets, this system generates its own real labeled data from day one. The ML work is genuine, not simulated.

---

### Optional Phase - Databricks Data Engineering Platform

**Goal:** Enterprise-grade data processing for portfolio and career positioning.

**Tools:**
- Databricks (full platform)
- Delta Lake (data lake with ACID transactions)
- Apache Spark (distributed processing)
- MLflow (end-to-end ML lifecycle)
- Airflow + Databricks Jobs (hybrid orchestration)

**Why it matters for career:**
Databricks is among the most requested data engineering skills in France and across Europe. A working Databricks project in a portfolio puts you ahead of most candidates.

---

## 11. What to Ignore Until Later

These tools are in the long-term plan but must be completely ignored during Phase 1 and Phase 2.

| Tool | When to actually touch it |
|---|---|
| Kafka | Phase 2 minimum, Phase 5 properly |
| Snowflake | Phase 4-5 |
| Databricks | Phase 5-6 |
| PyTorch | Phase 6 only if scikit-learn is not enough |
| Flutter | After Phase 1 is stable and in daily use |
| Profiling / Onboarding | After 30 days of real Phase 1 usage |

---

## 12. Realistic Timeline

| Period | What Actually Gets Done |
|---|---|
| Month 1 | Phase 1 core — transaction form + list + login. Used daily. |
| Month 2 | Add categories, edit/delete. Fix what feels wrong from real usage. |
| Month 3 | Add simple charts (recharts). See spending by category. |
| Month 4 | Phase 1 v2 — user profiling and adaptive onboarding. |
| Month 5-6 | Stop building. Just use the app. Collect real data. |
| Month 7 | Phase 3 — star schema in PostgreSQL using dbt. |
| Month 8 | Phase 4 — connect Power BI to the warehouse. Build dashboards. |
| Month 9+ | Phase 5 and 6 — streaming and ML when data is rich enough. |

---

## 13. Full Phase-to-Tool Map

```
Phase 1     -- React · FastAPI · PostgreSQL · DBeaver
Phase 1 v2  -- + User Profiling · Adaptive Onboarding · Dynamic Categories
Phase 2     -- + Kafka (intro) · WebSockets · React Query
Phase 3     -- + dbt · Airbyte · Airflow
Phase 4     -- + Power BI · Snowflake (optional start)
Phase 5     -- + Kafka (full) · Spark · Snowflake (full)
Phase 6     -- + scikit-learn · MLflow · Databricks
Optional    -- Full Databricks Platform · Delta Lake · MLflow
```

---

## 14. Honest Cost Breakdown

| Tool | Cost | When |
|---|---|---|
| React, FastAPI | Free | Day one |
| PostgreSQL, dbt, Airflow | Free | Day one / Phase 3 |
| Airbyte | Free (self-hosted) | Phase 3 |
| DBeaver | Free | Day one |
| Power BI Desktop | Free | Phase 4 |
| Apache Kafka | Free (self-hosted) | Phase 2-5 |
| Snowflake | Free trial then paid | Phase 4-5 |
| Databricks | Community Edition then paid | Phase 5-6 |
| scikit-learn, MLflow | Free | Phase 6 |

Every phase can be completed with free tools.
Paid services enter only when they add real portfolio or career value.

---

## 15. Skills This Project Proves

| Domain | What It Demonstrates |
|---|---|
| Software Engineering | Full-stack web application with shared backend |
| Data Engineering | ETL pipelines, warehouse design, real-time processing |
| Business Intelligence | Dimensional modeling, star schema, Power BI dashboards |
| Machine Learning | Anomaly detection, forecasting, behavioral clustering |
| ERP Concepts | Operational vs analytical systems, enterprise data architecture |
| System Design | Multi-platform sync, modular and scalable architecture |
| Databricks | Enterprise data lake, Spark processing, ML at scale |

---

## 16. On Failure

The project fails only if it gets abandoned entirely and nothing is learned.

- Phase 1 is buggy but works — not a failure
- Stuck on a problem for two weeks, then fixed it — not a failure
- Never started because it had to be perfect first — the only real failure

Every hour spent debugging is an hour spent becoming someone who can debug.
Every line of AI-generated code that breaks is a chance to understand why.
Time spent learning is never wasted time.

---

## 17. Final Statement

This project is not an exercise.

It solves a real problem right now.
It uses real data generated every day.
It uses the tools companies actually hire for in 2026.
It grows with skills and delivers value at every single phase.

It is the kind of project that separates engineers who understand systems
from engineers who only know tools.

---

Document version: Final Complete — June 2026
Project: Personal Finance Management System
Author: Mortadha
