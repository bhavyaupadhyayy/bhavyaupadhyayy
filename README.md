<div align="center">
  <img src="banner.svg" alt="Bhavya Upadhyay - Data Engineer & ML Practitioner" width="100%" />
</div>

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bhavyaupadhyay/)
[![Portfolio](https://img.shields.io/badge/Portfolio-1A1A1A?style=for-the-badge&logo=googlechrome&logoColor=white)](https://www.bhavyaupadhyay.site/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:officiallybhavya@gmail.com)
[![Resume](https://img.shields.io/badge/Resume-2E9EF7?style=for-the-badge&logo=readthedocs&logoColor=white)](https://bhavyaupadhyay.site)

</div>

---

## 🧭 About

**Data Engineer & ML practitioner** who builds end-to-end data and ML systems and is honest about how they're built. I work across the whole stack: streaming and batch ingestion, tested transformation pipelines, ML models with real evaluation, and multi-agent LLM systems with grounded, source-attributed output.

At **TCS (Air Canada)** I shipped AWS Lambda ETL pipelines processing **10M+ records/month**, cutting data latency by 50% and lifting pipeline SLA compliance to 99.9%. Now completing my **Master of Data Science at UC Irvine** on a full merit scholarship, while working as a Data Analyst at the Graduate Division building retention models and KPI dashboards across 20+ programs.

What I care about: pipelines that survive real, messy data; ML results reported with their limitations attached; and LLM systems whose claims you can actually trace back to a source.

```yaml
Role:        Data Engineer / ML Engineer  (full-time, available Jan 2027)
Strongest:   Python · SQL · AWS · Airflow · dbt · Snowflake
Built:       EDGAR-X — multi-agent financial intelligence on real SEC data
Contact:     officiallybhavya@gmail.com
```

---

## 📊 EDGAR-X — How It Works

A 7-layer multi-agent financial intelligence system on real SEC data. The diagram is the actual built architecture. **[🔴 Try the live demo →](https://edgar-x-26rm39rzy6c8fjzyb9pxdt.streamlit.app)**

```mermaid
flowchart LR
    A["SEC EDGAR<br/>filings + XBRL"] -->|checkpointed backfill| C[("Snowflake<br/>Raw")]
    B["FRED<br/>macro data"] -->|backfill| C
    C -->|dbt · 75 tests| D["Staging →<br/>Marts"]
    D --> E["XGBoost<br/>ranked screen<br/>AUC 0.726"]
    D --> F["LLM agents<br/>grounded memos"]
    F --> G(["LLM-as-judge<br/>evaluation"])
    E --> H(["Live Streamlit<br/>dashboard"])
    G --> H

    classDef src fill:#161b22,stroke:#58A6FF,color:#E6EDF3;
    classDef core fill:#0d3b5c,stroke:#29B5E8,color:#E6EDF3;
    classDef out fill:#1a3326,stroke:#3fb950,color:#E6EDF3;
    class A,B src;
    class C,D,E core;
    class F,G,H out;
```

> Real data on **498 S&P 500 companies** (7,863 XBRL fundamentals rows, 4,758 parsed 10-Ks). dbt tests caught four real extraction bugs. Agents use **code-supplied provenance** — the model can't fabricate a citation — and every memo is independently scored. The live dashboard runs free and permanently on a static snapshot; cloud infrastructure is written as deployment-ready Terraform/Kubernetes (not deployed, to avoid cost).

---

## 🚀 Featured Projects

### 📊 [EDGAR-X — Multi-Agent Financial Intelligence System](https://github.com/bhavyaupadhyayy/EDGAR-X) · [🔴 Live demo](https://edgar-x-26rm39rzy6c8fjzyb9pxdt.streamlit.app)
A 7-layer system that ingests real **SEC EDGAR** + **FRED** data for 498 S&P 500 companies into **Snowflake**, transforms it through a tested **dbt** pipeline, trains a revenue-direction model, and runs **LLM agents** that write source-grounded research memos — each scored by an automated judge — with a self-improvement loop, a live dashboard, and deployment-ready cloud IaC. Honestly documented throughout: what's built, what's deployed, and what would cost money to run.
`Python` · `Kafka` · `Airflow` · `dbt` · `Snowflake` · `XGBoost` · `Anthropic API` · `Terraform` · `Kubernetes`

### ✈️ [Flightline — End-to-End Flight Data Pipeline](https://github.com/bhavyaupadhyayy/Flightline-End-to-End-Flight-Data-Pipeline)
Batch ingestion of US BTS data → **Snowflake** → **dbt** (26/26 tests) → live **Streamlit** dashboard, orchestrated with **Airflow**, with a working **Kafka** streaming path for live flight positions from the OpenSky API. CI lints SQL with `sqlfluff` and runs `dbt build` on every push.
`Airflow` · `dbt` · `Snowflake` · `Kafka` · `Docker` · `GitHub Actions`

### 🛰️ [Signal Miner — LLM Market Intelligence](https://github.com/bhavyaupadhyayy/saas-signal-miner)
LLM pipeline (LangChain prompt chaining + RAG) turning unstructured market data from 250+ sources into clean, structured records. Containerized with Docker.
`Python` · `LangChain` · `RAG` · `Supabase` · `Docker`

### 🔎 [Duplicate Detection in Job Postings](https://github.com/bhavyaupadhyayy/bayesian-duplicate-detection)
Semantic deduplication over 250K+ postings; precision lifted **68% → 92%**, ~3x faster matching via optimized ANN indexing.
`Sentence Transformers` · `Milvus` · `RAG`

### 🩺 [Skin Lesion Classification](https://github.com/bhavyaupadhyayy/skin-lesion-classification)
EfficientNet-B0 + CBAM attention on ISIC 2019 (8 classes); ablation across 4 variants, Grad-CAM interpretability, served via FastAPI.
`PyTorch` · `FastAPI` · `Grad-CAM`

---

## 🛠️ Tech Stack

**Languages**
<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white" />
<img src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white" />
</p>

**Data Engineering & Cloud**
<p>
<img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white" />
<img src="https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white" />
<img src="https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white" />
<img src="https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white" />
<img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white" />
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
</p>

**ML / AI**
<p>
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" />
<img src="https://img.shields.io/badge/XGBoost-006600?style=flat-square&logo=xgboost&logoColor=white" />
<img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" />
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
</p>

**Analytics & Viz**
<p>
<img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
<img src="https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=tableau&logoColor=white" />
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" />
</p>

---

<div align="center">
<sub>Building reliable data systems, one pipeline at a time.</sub>
</div>
