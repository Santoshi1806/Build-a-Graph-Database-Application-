# Build-a-Graph-Database-Application-

## 📁 Create this GitHub repository

Repository name:

```text
ai-career-skill-graph
```

Inside it, add **exactly these files/folders**:

```text
ai-career-skill-graph/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
├── .env.example
│
├── database/
│   ├── connection.py
│   ├── seed.py
│   ├── schema.cypher
│   └── queries.cypher
│
├── services/
│   └── career_service.py
│
├── data/
│   ├── users.csv
│   ├── skills.csv
│   ├── jobs.csv
│   ├── companies.csv
│   └── courses.csv
│
├── screenshots/
│   ├── dashboard.png
│   ├── job-recommendations.png
│   ├── skill-gap.png
│   └── learning-path.png
│
└── docs/
    └── graph-model.png
```

### 1️⃣ `app.py`

This is your **main Streamlit application**.

```text
app.py
```

It displays:

* Dashboard
* Job recommendations
* Skill-gap analysis
* Related skills
* Learning recommendations

---

### 2️⃣ `requirements.txt`

Add:

```text
streamlit
neo4j
python-dotenv
pandas
```

---

### 3️⃣ `.env.example`

Add:

```text
COGNODB_URI=bolt+s://your-instance-id.databases.cognodb.cloud
COGNODB_USERNAME=cognodb
COGNODB_PASSWORD=your-password
```

⚠️ Do **not** upload your real `.env`.

The assignment specifically says database credentials must not be committed to GitHub. 

---

### 4️⃣ `.gitignore`

Add:

```text
.env
__pycache__/
*.pyc
.venv/
venv/
.streamlit/secrets.toml
```

---

# 📁 database

Create a folder called:

```text
database
```

Inside it add:

### `connection.py`

Contains your CognoDB connection.

### `seed.py`

Creates your sample:

```text
Users
Skills
Jobs
Companies
Courses
Relationships
```

The assignment requires a seed/data-loading script. 

### `schema.cypher`

Contains your database constraints/schema.

### `queries.cypher`

Put your important Cypher queries here:

```text
1. Job recommendation
2. Skill-gap analysis
3. Multi-hop traversal
4. Course recommendation
5. Related skills
```

The assignment requires at least one **2+ hop traversal** and one query that would be awkward in a relational database. 

---

# 📁 services

Create:

```text
services/
└── career_service.py
```

This contains the Python functions that call your Cypher queries.

---

# 📁 data

Create:

```text
data/
├── users.csv
├── skills.csv
├── jobs.csv
├── companies.csv
└── courses.csv
```

Example `skills.csv`:

```csv
id,name,category
S001,Python,Programming
S002,SQL,Database
S003,Machine Learning,AI
S004,Deep Learning,AI
S005,Power BI,Analytics
S006,Statistics,Mathematics
S007,NLP,AI
S008,Computer Vision,AI
S009,Generative AI,AI
S010,LangChain,AI
```

---

# 📁 screenshots

After your application is working, take screenshots and add:

```text
screenshots/
├── dashboard.png
├── job-recommendations.png
├── skill-gap.png
└── learning-path.png
```

The assignment specifically asks the README to include UI screenshots. 

---

# 📁 docs

Create:

```text
docs/
└── graph-model.png
```

This should be your graph diagram:

```text
User
 │
 └── HAS_SKILL ──> Skill
                       │
                       └── RELATED_TO ──> Skill
                                          
Job ── REQUIRES ──> Skill
 │
 └── OFFERED_BY ──> Company

Course ── TEACHES ──> Skill
```

The assignment requires a simple graph-data-model diagram in the README. 

---

# ⭐ Most important: README.md

Your README should have these headings:

```text
# AI Career & Skill Recommendation Graph

## 1. Project Overview

## 2. Problem Statement

## 3. Why a Graph Database?

## 4. Features

## 5. Graph Data Model

## 6. Architecture

## 7. Technology Stack

## 8. Project Structure

## 9. CognoDB Setup

## 10. Environment Variables

## 11. Installation

## 12. Database Seeding

## 13. Running the Application

## 14. Cypher Queries

## 15. Screenshots

## 16. Hosted Demo

## 17. Future Improvements

## 18. Author
```

These sections cover the documentation requested by Wexa, including the use case, graph rationale, model, setup, queries, and screenshots.  

---

# ✅ Final GitHub checklist

Before you submit, your GitHub should show:

```text
✅ app.py
✅ requirements.txt
✅ README.md
✅ .gitignore
✅ .env.example

✅ database/
   ✅ connection.py
   ✅ seed.py
   ✅ schema.cypher
   ✅ queries.cypher

✅ services/
   ✅ career_service.py

✅ data/
   ✅ users.csv
   ✅ skills.csv
   ✅ jobs.csv
   ✅ companies.csv
   ✅ courses.csv

✅ screenshots/
   ✅ dashboard.png
   ✅ job-recommendations.png
   ✅ skill-gap.png
   ✅ learning-path.png

✅ docs/
   ✅ graph-model.png
```

**Do NOT add:**

```text
❌ .env
❌ CognoDB password
❌ API keys
❌ unnecessary files
```
