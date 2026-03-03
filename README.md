# casb-defender
casb-defender for hackathon competition;


I-Driven CASB for Indian SMEs-------
Summary:
Indian SMEs rapidly adopt SaaS platforms but lack advanced security monitoring. The AI-powered CASB proposed hardens security & does the following real-time:
- Monitors SaaS access logs in real-time
- Detects anomalous access behaviour
- Flags insider threats and compromised accounts
- Provides explainable risk scores
- Detects data exfiltration patterns
- Runs fully containerised & production ready

Problem Statement:
Enterprises face trivial problems like:
- No visibility into SaaS Usage
- Data leakage
- No SIEM infrastructure

Solution: A lightweight Ai-powered CASB proactively triaging and preventing massive security breaches.

Architecture:
Connected SaaS Platform Logs(Google workplace, M365, Salesforce) --> Log Ingestion API(REST, webhooks+OAUTH) --> Apache Kafka stream layer --> Real-time feature engineering inference using ML Model for threat detection (Microservices) --> Display alerts on dashboard & email(FastAPI, React , PostgreSQL)



Detection Models:
- Login Anamoly using Isolation forest
- Data exfiltration using autoencoder
- Impossible travel using Geospatial anomaly detection
- Privilege escalation using Behavioral profiling



ML Piepeline:
Raw logs
User Behaviour Profiling
Session Vectorization
Anomaly Score
Explainability
Alerts


Risk scoring formula: RS = 0.4* Login_Anamoly_Score + 0.3* Data_Infiltration_Score + 0.2* Location_Deviation + 0.1* Device_Risk

Containerized Deployment usign Docker & K8s
Plug and play saas integrations


Sample User Flow:
User Login Event
Log API
Kafka Topic
Consumer
Feeature Builder
Model
Risk score
Alert DB
Dashboard


Observabillity & monitoring using prometheus;



Leveraging Openclaw for threat simulation & adversarial testing :
Since, we don't have real enterprise data logs, we simulate scenarios, generate threats & emulate data exfiltration patterns using openclaw. Further clean+adversarial logs can be used for training dataset to make realistic ML model.


Integrate into CI pipeline for automated robustness validation & security aware ML lifecycle



