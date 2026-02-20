# Project FinSentinel :- Pre-Delinquency Intervention Engine

**Team :- DropZone**

| Member | Role |
|--------|------|
| Nikhil Shah | AI Systems Lead & Model Architect |
| Ragini Pawar | ML Engineer & Model Architect |
| Sanat Sanjeev | Full Stack Developer & Integration Lead |
| Shaktisingh Suryawanshi | Data Engineer & Feature Architect |

**College :- Vishwakarma Institute of Technology, Pune**

**Link :- https://github.com/Raginipawar/Project-Finsentinel**

---

## Table of Contents

| Section | Reference |
|---------|-----------|
| [Problem Statement Chosen](#problem-statement-chosen) | Overview of the chosen problem statement |
| [Demo Video](#demo-video) | Video demonstration link and explanation |
| [Introduction](#introduction) | Project context, background, and scope |
| [Objectives](#objectives) | Project goals and deliverables |
| [USPs](#usps) | Unique Selling Propositions overview |
| [Impact](#impact) | Impact assessment and benefits |
| [Market Analysis](#market-analysis) | Comparative analysis and market positioning |
| [Methodology Details](#methodology-details) | In-depth methodology and technical approach |
| &emsp;[Architecture](#architecture) | Architecture diagram |
| &emsp;[User Flow](#user-flow) | User flow diagram |
| &emsp;[Understanding the Flow](#understanding-the-flow) | Visual representation of process flow |
| [Design Considerations](#design-considerations) | Key design decisions and reasoning |
| [Tech Stack](#tech-stack) | Technologies and tools used |
| [Security Aspects](#security-aspects) | Security strategy and data protection |
| [Scalability](#scalability) | Scalability approaches and infrastructure |
| [Future Scope](#future-scope) | Planned enhancements and roadmap |
| [Closing Remarks](#closing-remarks) | Final thoughts and acknowledgments |

---

## Problem Statement Chosen

**Pre-Delinquency Intervention Engine**

Banks currently intervene **after** a customer misses a payment, at which point recovery rates drop by 60% and collections cost 15-20% of the recovered amount. The challenge is to build a system that detects financial distress **2-4 weeks before** the first missed payment, enabling proactive and empathetic intervention that protects both the customer and the bank.

---

## Some Points to Consider

- Please go through the README first before watching the demo video for better understanding.
- Please also see our **Architecture** and **User Flow** diagrams for complete technical clarity.
- The system is designed and proposed for validation on **500,000 synthetic customers** with realistic Indian banking transaction patterns.
- For demo purposes we have used the most accessible technology available to us.

---

## Demo Video

> Coming Soon - Demo video will be added here.

---

## Introduction

In India's rapidly evolving digital lending landscape, financial distress does not appear suddenly. It **builds silently over weeks**. A customer paying only the minimum credit card due while juggling three EMIs and two BNPL platforms is sinking, but every bank system shows them as healthy. By the time they miss a payment, the damage, a 7-year credit history scar, broken customer trust, and expensive collections, is already done.

**Project FinSentinel** is an AI-powered pre-delinquency intervention engine that models financial distress as a **story unfolding over time**, not a point-in-time snapshot. It uses a three-model ensemble of a Temporal Fusion Transformer, a Variational Autoencoder, and a CNN-BiLSTM to detect novel distress signals including the **Minimum Due Trap** and **EMI Burden Index** that traditional XGBoost-based models completely miss.

FinSentinel does not just flag risk. It outputs a **Bucket Migration Probability Matrix** (B0 to NPA), a **30-day distress trajectory**, and a **credit score consequence forecast**, then triggers a **LangGraph agentic intervention** that sends a personalized, empathetic message showing the customer their 7-year consequence before it is too late.

---

## Objectives

- **Detect Pre-Default Distress**
  Identify financial stress 2-4 weeks before the first missed payment using a three-model ensemble, giving Barclays a decisive intervention window.

- **Model Distress as a Trajectory, Not a Snapshot**
  Move beyond static XGBoost scoring to time-series modeling that captures how a customer's financial behavior deteriorates week over week.

- **Surface Novel Signals Traditional Models Miss**
  Compute the EMI Burden Index, detect the Minimum Due Trap, identify the Robbing Peter to Pay Paul pattern, and flag BNPL overload, signals discovered through real borrower interviews.

- **Output Actionable Risk Intelligence**
  Produce Bucket Migration Matrices (B0 to B1 to B2 to NPA), 30-day distress trajectories, credit score impact forecasts, and SHAP explanations, not a single opaque risk score.

- **Enable Personalized Agentic Intervention**
  Use a LangGraph agent to select the right intervention type per customer and generate empathetic messages that show customers their 7-year credit consequence, making them partners in their own recovery.

- **Provide Macro-Level Portfolio Intelligence**
  Detect correlated distress clusters across employer and geographic segments via the Stress Contagion Detector, giving Barclays early warning of systemic events before they cascade.

---

## USPs

The following are the Unique Selling Propositions FinSentinel offers:

### 1. Distress Consensus Engine
**Multiple independent signals must AGREE** before raising an alert. VAE behavioral drift, TFT multi-horizon trajectory, CNN-BiLSTM transaction patterns, and EMI Burden Index all converge before a customer is flagged, eliminating the false positives that make banks distrust ML systems.

### 2. Bucket Migration Probability Matrix
**Predicts exact probability of moving B0 to B1 to B2 to NPA** over 90 days using banking's own DPD terminology, not a generic risk score but a regulator-ready migration forecast with credit score impact and time-to-NPA estimate.

### 3. EMI Burden Index + Minimum Due Trap
**Novel signals discovered from real borrower interviews.** Detects the Minimum Due payment pattern, Robbing Peter to Pay Paul debt cycle, and BNPL overload in the 22-28 demographic, catching distress 6-8 weeks before the first missed payment.

### 4. Stress Contagion Detection
**Identifies correlated distress clusters across employer and geography.** When 200 customers at the same company show stress in the same fortnight, FinSentinel flags it as one systemic event, not 200 individual risks.

### 5. Agentic Intervention Engine (LangGraph)
**Decides WHICH intervention to trigger** based on customer segment, risk severity, and history, then generates a personalized empathetic message showing the customer their 7-year credit consequence, making them partners in their own recovery.

### 6. Financial Stress Fingerprinting (VAE)
**Personalizes risk thresholds to each customer's own behavioral baseline.** Asks not "does this customer look like a defaulter" but "does this customer look like a stressed version of themselves", eliminating bias against gig workers and irregular earners.

---

## Impact

**Project FinSentinel** delivers a transformative shift from reactive collections to proactive financial wellness. By intervening 2-4 weeks before default, Barclays can:

- **Reduce default rates** by catching customers before they enter the bucket migration cascade
- **Cut collections costs** by avoiding the 15-20% recovery cost associated with post-default collections
- **Preserve customer trust** through empathetic, early intervention that protects the customer relationship
- **Enable regulatory compliance** via SHAP-backed explanations and RBI Fair Practices Code-aligned messaging
- **Gain macro-level portfolio intelligence** through Stress Contagion detection that provides systemic risk signals unavailable in any single-customer model

The system also protects customers by showing them the 7-year consequence of default before it happens, giving them the agency to act.

---

## Market Analysis

Existing solutions fall into two categories: **Reactive Collections Tools** (act after default) and **Generic Risk Scoring Engines** (static snapshot, no trajectory). FinSentinel sits at their intersection and goes beyond both.

| | Reactive Collections Tools | FinSentinel | Generic Risk Scoring Engines |
|--|--|--|--|
| **Players** | FICO Collections, Experian PowerCurve, Temenos, Finnone Neo | **Our Product** | CIBIL, XGBoost Models, SAS Credit Risk, Moody's, CRIF High Mark |
| **Timing** | After default | 2-4 weeks BEFORE default | After alert only |
| **Trajectory** | No | 30-day distress trajectory | Point-in-time snapshot |
| **Personalization** | No | VAE personal baseline | Population thresholds |
| **Novel Signals** | No | EMI Burden, Min Due Trap | Misses Minimum Due Trap |
| **Intervention** | Collections only | LangGraph agentic | None |

**FinSentinel combines the domain knowledge of collections tools with the predictive power of risk engines, and adds behavioral fingerprinting, agentic intervention, Bucket Migration forecasting, and Stress Contagion detection that neither category offers.**

---

## Methodology Details

FinSentinel is a pre-delinquency intervention engine that detects financial distress 2-4 weeks before the first missed payment using a **four-stage pipeline**: data ingestion, feature engineering, multi-model prediction, and agentic intervention.

### Architecture

> Note: Please zoom in for full detail.

![System Architecture](https://github.com/user-attachments/assets/20d06e02-3aea-4e4c-9d12-9787875804a2)

### User Flow

> Note: Please zoom in for full detail.

![User Flow](https://github.com/user-attachments/assets/b150e9ca-7e99-4629-a3c7-1a6fc04a165f)

### Understanding the Flow

**Stage 1 - Data Ingestion**
Raw transactions (UPI, NEFT, ATM, EMI auto-debits, salary credits) are ingested via Apache Kafka (simulated) into a partitioned PostgreSQL database. Customer profiles, cross-product data (FD/RD, credit card, BNPL), and macro context (employer, geography) are captured weekly per customer.

**Stage 2 - Feature Engineering**
Novel distress signals are computed per customer per week:
- **EMI Burden Index** - Total monthly EMIs divided by average salary credit. Flags at 50% / 65% / 75% thresholds
- **Minimum Due Trap** - Paying only credit card minimum due for 2+ consecutive months while holding 3+ active EMIs
- **Robbing Peter to Pay Paul** - Lending app UPI repaid within 24 hours of salary credit
- **Velocity Features** - Salary delay trends, savings drawdown rate, ATM withdrawal bursts
- **Financial Maturity Score** - Age-adjusted risk for the 22-28 BNPL-heavy demographic
- **Stress Contagion Signals** - Correlated anomaly detection across employer and geographic clusters

**Stage 3 - Three-Model AI Ensemble**
Three independent models run in parallel:
- **Temporal Fusion Transformer (TFT)** - Predicts default probability at 7/14/21/28-day horizons. Built-in attention means natively explainable. Google Research 2021, via pytorch-forecasting
- **Variational Autoencoder (VAE)** - Learns each customer segment's healthy behavioral baseline. Detects drift from their own normal, not a population average. Latent space visualization shows the customer's embedding migrating toward the risk cluster
- **CNN + BiLSTM** - Reads raw transaction sequences directly. CNN detects local burst patterns; BiLSTM captures temporal ordering

The **Distress Consensus Engine** combines all three signals via an XGBoost + SHAP layer. A risk flag is escalated only when multiple independent signals agree, producing four tiers: **Watch - Monitor - Intervene - Critical**

**Stage 4 - Agentic Intervention**
The **LangGraph Decision Engine** reads the risk tier, customer segment, age, and intervention history, then:
1. Selects the appropriate intervention (SMS payment holiday / app notification / RM call / debt consolidation)
2. Generates a personalized, empathetic message via **Llama (Groq API)** showing the customer their 7-year credit consequence
3. Tracks whether the customer opened, accepted, and improved, feeding results back into the agent for continuous self-improvement (closed-loop learning)

---

## Design Considerations

### 1. Why a Three-Model Ensemble Instead of XGBoost Alone?
XGBoost treats each prediction as an independent snapshot. Financial distress is a **story unfolding over time**, salary arriving later each month, savings declining, minimum due payments increasing. The TFT captures this trajectory, the VAE captures personal deviation, and the CNN-BiLSTM captures raw sequence patterns. No single model sees all three dimensions.

### 2. Why VAE for Behavioral Fingerprinting?
A gig worker with irregular income will always look "risky" against a population-level threshold designed for salaried customers. The VAE trains on each segment's own healthy patterns, so irregular income is only a signal if it deviates from that customer's own normal. This eliminates systematic bias against non-traditional earners.

### 3. Why the Distress Consensus Engine?
Banks distrust ML risk systems because of false positives. Flagging healthy customers damages trust and wastes collections resources. By requiring **multiple independent models to agree** before escalating, FinSentinel dramatically reduces false positives while maintaining high recall on true pre-default cases.

### 4. Why LangGraph for Intervention?
Rule-based intervention such as "send SMS if score > 0.7" ignores context. A 26-year-old first-time credit user needs different messaging than a 45-year-old salaried customer. LangGraph's agent architecture allows the system to **reason about which intervention to trigger** based on segment, severity, age, and past response history, genuinely agentic behavior, not a chatbot bolted on.

### 5. Why Synthetic Data?
Using real customer data in a hackathon context raises significant privacy concerns. Synthetic data generated to match realistic Indian banking patterns (salary on 1st-2nd, UPI-heavy transactions, BNPL platforms, EMI auto-debits) allows the system to be built, validated, and demonstrated without exposing any real customer information.

### 6. Why PostgreSQL with Monthly Partitioning?
Transaction data grows continuously. Monthly partitioning ensures that queries on recent data, which is where all the relevant distress signals are, never scan historical partitions, keeping latency low regardless of total dataset size.

---

## Tech Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Data and Features** | Python, pandas, numpy | Synthetic data generation + feature engineering |
| **ML Core** | PyTorch (VAE + CNN-BiLSTM) | Behavioral fingerprinting + pattern detection |
| **Primary Forecaster** | pytorch-forecasting (TFT) | Multi-horizon 7/14/21/28-day prediction |
| **Explainability** | XGBoost + SHAP | Compliance-grade feature importance |
| **Orchestration** | Apache Kafka (simulated) | Real-time transaction ingestion |
| **Agentic Layer** | LangGraph + LangChain | Intervention decision engine |
| **LLM** | Llama (Groq API) | Personalized message generation |
| **Database** | PostgreSQL (partitioned) | Scalable transaction + risk storage |
| **Frontend** | React.js | Banker dashboard + intervention UI |
| **Backend** | Node.js + FastAPI | Core logic, ML serving, API endpoints |

---

## Security Aspects

Security and data protection are core design constraints for FinSentinel, not afterthoughts.

### 1. Privacy and Isolation by Design
- All customer transaction data is processed **in-memory**, no raw PII persists post-inference
- Customer identifiers are **hashed at ingestion**, the model only sees anonymized behavioral vectors, never account numbers or phone numbers
- The entire system is built and demonstrated on **100% synthetic data**, zero real customer exposure at any stage
- **FastAPI endpoints** enforce request-level authentication and rate limiting, risk scores and customer profiles are never publicly accessible

### 2. Model Integrity and Explainability
- Every risk flag is backed by a **SHAP explanation**, no black-box decisions. Bankers see exactly which signals drove the alert
- The **Distress Consensus Engine** requires multiple independent model signals to agree before escalation, a single model's bias cannot flag a customer alone
- The **VAE personalizes thresholds per segment**, gig workers are not falsely flagged against salaried customer thresholds, eliminating systematic bias
- All model outputs include **confidence intervals**, the system never presents an overconfident single-point score

### 3. RBI Compliance and Ethical Intervention
- All customer-facing messages follow the **RBI Fair Practices Code for Lenders**, empathetic tone, no coercive language, customer always has the right to decline
- Every intervention message includes **full transparency**, the customer is told why they were contacted and what the bank is offering
- The **closed-loop feedback tracker** monitors intervention acceptance across segments, if a message type shows low acceptance, the agent self-corrects

### 4. Infrastructure Security
- **AES-256 encryption at rest** and **TLS 1.3 in transit** for all stored behavioral data
- **Groq API** is called server-side only, only anonymized context is passed to the LLM, raw customer data never leaves the backend
- All model artifacts are version-controlled, full audit trail of every model change

---

## Scalability

FinSentinel is designed for production-scale banking from the ground up.

### 1. Scalable Data Architecture
- **PostgreSQL with monthly partitioning** on transaction date, recent data queries never scan historical partitions, keeping latency low as data grows
- **FastAPI paginated endpoints**, a portfolio of 500K+ customers is never loaded into memory at once, only requested slices are served

### 2. Scalable Inference Design
- **Batch inference** for nightly full-portfolio risk scoring, no real-time bottleneck
- **Delta streaming** for high-risk customers only, CNN-BiLSTM triggers only on new anomaly signals, not every customer every hour
- **Model artifacts are serialized and cached**, no retraining needed for daily inference runs

### 3. Horizontal Scaling Path
- **Stateless FastAPI workers** scale horizontally behind a load balancer, no single point of failure
- **Apache Kafka** handles real-time transaction ingestion with consumer groups per customer segment, designed to grow from thousands to millions of transactions per day
- Adding GPU nodes **linearly increases inference throughput** with no architectural changes needed

### 4. Why the Model Stack is Efficient
- **TFT and VAE run per segment, not per customer individually**, one inference pass covers the entire segment cluster
- **LangGraph agent runs on-demand only for flagged customers**, not for the full portfolio, keeping compute costs proportional to actual risk events

---

## Future Scope

1. **Real Banking Data Integration:** Integrate with live CBS, NACH, and CIBIL APIs to train on real transaction patterns and validate signal accuracy on actual default cases.

2. **Multi-Bank Stress Contagion Network:** Expand Stress Contagion detection across multiple institutions, catching systemic sector-wide distress before it triggers a banking cascade.

3. **Vernacular Customer Communication:** Extend LangGraph agent to Hindi, Marathi, Tamil, and regional languages, critical for Tier 2/3 customers most vulnerable to the Minimum Due Trap.

4. **Account Aggregator Framework Integration:** Leverage India's AA framework to pull consented cross-bank data, giving FinSentinel a complete 360 degree debt picture beyond Barclays alone.

5. **Customer Self-Service Portal:** Let customers simulate "what if I take one more EMI?", shifting FinSentinel from a bank tool to a proactive financial wellness product.

6. **Regulator-Ready Audit Dashboard:** Build an RBI-facing interface showing model decisions, intervention history, and outcomes, positioning FinSentinel as a compliance asset, not just a risk tool.

---

## Closing Remarks

Thank you for the opportunity to present FinSentinel. We have tried to document as much of our design thinking, architecture, and methodology as possible, and we hope the depth of the idea reflects the seriousness with which we approached the problem.

Financial distress is not a data problem. It is a human problem. FinSentinel is built on the belief that if you catch someone early enough, and talk to them with respect and clarity about what is at stake, most people will act. The technology exists to do this. We just have to build it.

**Team DropZone - VIT Pune - Barclays Hack-O-Hire 2026**
