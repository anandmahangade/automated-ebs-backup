# Automated EBS Volume Backup using AWS Lambda & SNS

## 📌 Project Overview
This project implements a **serverless, fully automated EBS snapshot solution** that scans **all AWS regions**, identifies **in-use EBS volumes**, creates **on-demand snapshots**, and sends **notifications via SNS**.

It is designed for:
- Data protection
- Disaster recovery
- Cost‑efficient, hands‑free backups

---

## 🛠️ Tech Stack
- AWS Lambda
- Amazon EC2
- Amazon EBS Snapshots
- Amazon SNS
- Amazon CloudWatch
- Python (boto3)

---

## 📂 Project Structure
```
automated-ebs-backup/
│
├── lambda_function/
│   ├── lambda_function.py
│   ├── requirements.txt
│
├── iam-policy/
│   └── lambda-ebs-snapshot-policy.json
│
├── sns/
│   └── sns-setup.md
│
├── cloudwatch/
│   └── eventbridge-rule.md
│
├── architecture/
│   └── architecture-overview.md
│
└── README.md
```

---

## 🧠 Lambda Function Code
**File:** `lambda_function/lambda_function.py`

---

## 📦 Dependencies
**File:** `lambda_function/requirements.txt`
```
boto3
```
*(Note: boto3 is preinstalled in AWS Lambda, this file is mainly for local testing)*

---

## 🔐 IAM Policy
**File:** `iam-policy/lambda-ebs-snapshot-policy.json`


---

## 📢 SNS Setup
**File:** `sns/sns-setup.md`

### Steps:
1. Create an SNS Topic (Standard)
2. Create a subscription (Email/SMS)
3. Confirm subscription
4. Copy Topic ARN
5. (Optional) Modify Lambda to publish snapshot summary to SNS

---

## ⏰ Automation using EventBridge
**File:** `cloudwatch/eventbridge-rule.md`

### Steps:
1. Open EventBridge
2. Create rule
3. Schedule (example: once daily)
4. Target: Lambda Function
5. Enable rule

---

## 🏗️ Architecture Overview
**File:** `architecture/architecture-overview.md`

```
EventBridge (Schedule)
        │
        ▼
   AWS Lambda
        │
        ├── Describe Regions
        ├── Scan In‑Use Volumes
        ├── Create Snapshots
        └── Send SNS Notification
```

---

## 🚀 Deployment Steps (Clean & Clear)

1. Create IAM Role for Lambda
2. Attach IAM policy provided
3. Create Lambda Function (Python 3.9+)
4. Paste `lambda_function.py`
5. Increase timeout to **5 minutes**
6. Create SNS Topic and subscription
7. Create EventBridge schedule
8. Test Lambda manually

---

## 📈 Outcome
- Fully automated, serverless backup solution
- Multi‑region coverage
- Zero manual intervention
- Cost‑efficient snapshots

---
## Output 
<img width="1912" height="811" alt="Screenshot 2026-04-14 181947" src="https://github.com/user-attachments/assets/340d09b1-b490-455d-9550-06d93837307b" />
<img width="1919" height="775" alt="Screenshot 2026-04-14 182016" src="https://github.com/user-attachments/assets/dab465b7-eced-4eea-b6ca-b608b33fa176" />
<img width="1919" height="815" alt="Screenshot 2026-04-14 182257" src="https://github.com/user-attachments/assets/e054d711-1da2-4258-b10a-ce559199e8bd" />

## 🧑‍💻 Author
**Anand Mahangade**  
Cloud & DevOps Engineer (Fresher)

---

