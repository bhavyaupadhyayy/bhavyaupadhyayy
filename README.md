<div align="center">
  <img src="banner.svg" alt="Bhavya Upadhyay — Data Engineer" width="100%" />
</div>

<div align="center">

<a href="https://readme-typing-svg.demolab.com">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&pause=1000&color=38BDF8&center=true&vCenter=true&width=640&lines=Data+Engineer+%C2%B7+ML+Practitioner;AWS+ETL+at+scale+%E2%80%94+10M%2B+records%2Fmonth;Tested+pipelines+%C2%B7+honest+evaluation;Source-grounded+multi-agent+LLM+systems" alt="Data Engineer · ML Practitioner" />
</a>

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-Live-38BDF8?style=for-the-badge&logo=googlechrome&logoColor=white&labelColor=0D1117)](https://bhavyaupadhyay-portfolio.vercel.app)
[![Resume](https://img.shields.io/badge/Résumé-PDF-2E9EF7?style=for-the-badge&logo=readthedocs&logoColor=white&labelColor=0D1117)](https://bhavyaupadhyay-portfolio.vercel.app/Bhavya_Upadhyay_Resume_Updated.pdf)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0D1117)](https://www.linkedin.com/in/bhavyaupadhyay/)
[![Email](https://img.shields.io/badge/Email-Say_hi-D14836?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117)](mailto:officiallybhavya@gmail.com)

</div>

<div align="center">

`10M+ records/mo`&nbsp;&nbsp;·&nbsp;&nbsp;`99.9% pipeline SLA`&nbsp;&nbsp;·&nbsp;&nbsp;`498 S&P 500 modeled`&nbsp;&nbsp;·&nbsp;&nbsp;`0.726 test AUC`&nbsp;&nbsp;·&nbsp;&nbsp;`124 tests / 93% cov`

</div>

---

## 🧭 About

I'm a **Data Engineer** (ML on the side) who builds end-to-end data systems — and is honest about how they're built. Streaming and batch ingestion, test-gated transformation pipelines, ML models with real evaluation, and multi-agent LLM systems whose claims trace back to a source.

At **TCS (Air Canada)** I shipped AWS Lambda ETL processing **10M+ records/month**, cut data latency ~50%, and lifted pipeline SLA compliance to **99.9%**. Now finishing my **MS in Data Science at UC Irvine** on a full merit scholarship, while building retention models and KPI dashboards across 20+ graduate programs as a Data Analyst at the Graduate Division.

What I care about: **pipelines that survive real, messy data**, **ML reported with its limitations attached**, and **LLM systems you can actually trust**.

```yaml
role:       Data Engineer / ML Engineer   # full-time, available Jan 2027
strongest:  Python · SQL · AWS · Airflow · dbt · Snowflake
flagship:   EDGAR-X — multi-agent financial intelligence on real SEC data
based:      Irvine, CA
contact:    officiallybhavya@gmail.com
```

---

## 📊 EDGAR-X — How It Actually Works

A **7-layer multi-agent financial intelligence system** on real SEC data. This is the built architecture — not a wishlist. **[🔴 Try the live demo →](https://edgar-x-26rm39rzy6c8fjzyb9pxdt.streamlit.app)**

```mermaid
%%{init: {'flowchart': {'curve': 'basis', 'nodeSpacing': 55, 'rankSpacing': 75}}}%%
flowchart LR
    A["SEC EDGAR · XBRL"] -->|backfill| C[("Snowflake Raw")]
    B["FRED macro"] -->|backfill| C
    C -->|"dbt · 75 tests"| D["Staging → Marts"]
    D --> E["XGBoost screen · AUC 0.726"]
    D --> F["LLM agents · grounded memos"]
    E --> H["Live Streamlit dashboard"]
    F --> G["LLM-as-judge"]
    G --> H

    classDef src  fill:#161b22,stroke:#58A6FF,color:#E6EDF3;
    classDef core fill:#0d3b5c,stroke:#38BDF8,color:#E6EDF3;
    classDef out  fill:#1a3326,stroke:#3fb950,color:#E6EDF3;
    class A,B src;
    class C,D,E core;
    class F,G,H out;
```

> Real data on **498 S&P 500 companies** (7,863 XBRL fundamentals rows, 4,758 parsed 10-Ks). The dbt test suite caught **four real extraction bugs**. Agents use **code-supplied provenance** — the model *can't* fabricate a citation — and every memo is independently scored by an LLM judge. Framed honestly as a **ranked screen (test ROC-AUC 0.726)**, not a classifier. Cloud IaC is written as deployment-ready Terraform/Kubernetes but left undeployed to keep it free to run.

---

## 🚀 Featured Projects

| Project | What it is | Stack |
|---|---|---|
| **[📊 EDGAR-X](https://github.com/bhavyaupadhyayy/EDGAR-X)** · [demo](https://edgar-x-26rm39rzy6c8fjzyb9pxdt.streamlit.app) | 7-layer system: SEC/FRED → Snowflake → tested dbt → revenue-direction model + source-grounded LLM agents scored by an automated judge. Honest about what's built vs. deployed. | `Python` `dbt` `Snowflake` `XGBoost` `Anthropic API` `Terraform` |
| **[✈️ Flightline](https://github.com/bhavyaupadhyayy/Flightline-End-to-End-Flight-Data-Pipeline)** | Re-runnable, test-gated US flight pipeline: BTS → Snowflake → dbt (26/26 tests) → live Streamlit, orchestrated with Airflow + a scaffolded Kafka streaming path. CI on every push. | `Airflow` `dbt` `Snowflake` `Kafka` `Docker` |
| **[🛰️ Signal Miner](https://github.com/bhavyaupadhyayy/saas-signal-miner)** | LLM pipeline (LangChain + RAG) turning unstructured data from 250+ sources into clean, validated records. | `LangChain` `RAG` `Supabase` `Docker` |
| **[🔎 Duplicate Detection](https://github.com/bhavyaupadhyayy/bayesian-duplicate-detection)** | Semantic dedup over 250K+ job postings; precision **68% → 92%**, ~3× faster matching via optimized ANN indexing. | `Sentence Transformers` `Milvus` |
| **[🩺 Skin Lesion Classification](https://github.com/bhavyaupadhyayy/skin-lesion-classification)** | EfficientNet-B0 + CBAM on ISIC 2019 (8 classes); 4-variant ablation, Grad-CAM, served via FastAPI. | `PyTorch` `FastAPI` `Grad-CAM` |

---

## 🛠️ Tech Stack

**Languages**
<br/>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**Data Engineering & Cloud**
<br/>
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

**ML / AI**
<br/>
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-006600?style=flat-square&logo=xgboost&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)

**Analytics & Viz**
<br/>
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=tableau&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

---

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=bhavyaupadhyayy&show_icons=true&hide_rank=true&hide_border=true&count_private=true&include_all_commits=true&bg_color=0D1117&title_color=38BDF8&icon_color=38BDF8&text_color=C9D1D9" alt="GitHub stats" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=bhavyaupadhyayy&layout=compact&hide_border=true&langs_count=8&bg_color=0D1117&title_color=38BDF8&text_color=C9D1D9" alt="Top languages" />

</div>

---

<div align="center">
<sub>Building reliable data systems, one tested pipeline at a time.</sub>
</div>
