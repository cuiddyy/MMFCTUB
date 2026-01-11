# MMFCTUB: Multi-Modal Financial Credit Table Understanding Benchmark

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![ArXiv:2601.04643](https://img.shields.io/badge/ArXiv-2601.04643-blue.svg?style=flat-square)](https://arxiv.org/abs/2601.04643)
[![Dataset](https://img.shields.io/badge/Dataset-HuggingFace-yellow.svg?style=flat-square)](link-to-dataset)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg?style=flat-square)](https://www.python.org/downloads/)
<div align="center">
<img src="assets/framework.png" width="900"/>
</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Benchmark Highlights](#-benchmark-highlights)
- [Dataset Statistics](#-dataset-statistics)
- [Quick Start](#-quick-start)
- [Evaluation](#-evaluation)
- [Leaderboard](#-leaderboard)
- [Dataset Structure](#-dataset-structure)
- [Examples](#-examples)
- [Citation](#-citation)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)
- [Contact](#-contact)

---

## 🎯 Overview

**MMFCTUB** (Multi-Modal Financial Credit Table Understanding Benchmark) is a comprehensive benchmark designed to evaluate Multimodal Large Language Models (MLLMs) on financial credit report understanding tasks. It addresses the critical gap in assessing MLLMs' capabilities in processing specialized financial tables that encode applicants' economic profiles through domain-specific layouts and numerical relationships.

### Why MMFCTUB?

Credit reports present unique challenges for MLLMs:

- 🏦 **Domain-Specific Knowledge**: Requires understanding of financial terminology and credit assessment concepts
- 📊 **Complex Table Structures**: Multi-table layouts with cross-table dependencies
- 🔢 **Numerical Reasoning**: Accurate calculations involving credit limits, balances, and ratios
- 📈 **Real-World Impact**: Critical for loan approval and risk assessment decisions

Existing benchmarks inadequately assess MLLM performance on such specialized financial tables. MMFCTUB fills this gap with **7,657+ high-quality samples** across **5 credit table categories**.

---

## 🌟 Key Features

### Comprehensive Coverage

- **📊 7,600+ Samples**: High-quality CTU (Credit Table Understanding) question-answer pairs
- **👥 246 Applicants**: Diverse credit applicant profiles across 9 credit levels
- **📋 19,564 Tables**: Real-world credit tables across 5 major categories
- **🔤 60+ Fields**: Domain-specific financial fields covering complete credit profiles
- **🔢 12 Input Numbers**: Number of Input Tables
- **54 Applicant Indicators**: Credit utilization, account duration, turnover efficiency
- **3 Calculation Operators**: Addition, Subtraction, Division
- **3 Question Types**: Single Selection, Multi Selection, Calculation
- **Scenarios**: Real-world calculation from credit assessment
- **📑 5 Core Table Types**:
  - [Credit Transaction Table](credit_transaction_table.png)
  - [Residence Info Table](residence_info_table.png)
  - [Occupation Info Table](occupation_info_table.png)
  - [Account Detail Table]
    - [Non-revolving Loan Account Table](non_revolving_loan_account_table.png)
    - [Revolving Loan Account Table](revolving_loan_account_table.png)
    - [Sub Account Under Revolving Credit Account Table](sub_account_under_revolving_credit_account_table.png)
  - [Credit Agreement Table](credit_agreement_table.png)
- **🔄 3 Cross-Table Paradigms**: 
  - Homo. Static (Cross-table Operations Between Homogeneous Static Tables)
  - Homo. Dynamic (Cross-table Operations Between Homogeneous Dynamic Tables)
  - Hetero. (Cross-table Operations Between Heterogeneous Tables)
  - Inclusion relationships (Paradigm → Table Types):
    1. Homo. Static = Credit Agreement Table
    2. Homo. Dynamic = Credit Transaction Table, Account Detail Table
    3. Hetero. = Account Detail Table + Residence Info Table, Account Detail Table + Occupation Info Table

### Three-Aspect Evaluation Framework

#### 1️⃣ **Table Structure Perception (TSP)**
Evaluates MLLMs' ability to comprehend table contents and inter-table relationships. Specifically, TSP assesses models' capacity to perceive table structures, including spatial layouts and cross-table relationships. Evaluation spans two dimensions:
- **Structural perception**: Assessed across multiple cross-table paradigms.
- **Scope perception**: Assessed across three table count ranges (3-5, 6-8, 9-13).

By minimizing domain knowledge and computational demands in question design, we isolate structural perception capabilities. Performance is measured by answer accuracy.

#### 2️⃣ **Domain Knowledge Utilization**
Assesses financial domain expertise through mask-and-recovery evaluation:
- **3 Knowledge Levels**: Perception, Analysis, Reasoning([Categroy Detail](knowledge_utilization_model_level))
- **5 Domain Knowledge Types**: Account, Amount, Temporal, Ratio, Weight([Categroy Detail](knowledge_utilization_domain_level))

#### 3️⃣ **Domain Numerical Calculation**
Tests arithmetic reasoning in financial contexts:
- **3 Calculation Operators**: Addition (+), Subtraction (-), Division (÷)

---
### Credit Table Categories

1. **📝 credit transaction tables**:
2. **💰 residence information tables**: Loan balances, overdrafts, and total credit
3. **💳 occupation information tables**: Card limits, usage, and account duration
4. **📅 account detail tables**: Payment records, delays, and compliance
5. **🔍 credit agreement tables**: Application history and inquiry patterns

---
