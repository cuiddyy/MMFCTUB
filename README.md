# MMFCTUB: Multi-Modal Financial Credit Table Understanding Benchmark

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Paper](https://arxiv.org/abs/2601.04643)](link-to-paper)
[![Dataset](https://img.shields.io/badge/Dataset-HuggingFace-yellow.svg)](link-to-dataset)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

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
- **🔢 12 Input Numbers**: Various numerical data points for calculation tasks
- **🔄 3 Cross-Table Paradigms**: 
  - Homo. Static (Cross-table Operations Between Homogeneous Static Tables)
  - Homo. Dynamic (Cross-table Operations Between Homogeneous Dynamic Tables)
  - Hetero. (Cross-table Operations Between Heterogeneous Tables)
  - Inclusion relationships (Paradigm → Table Types):
    1. Homo. Static = Credit Agreement Table
    2. Homo. Dynamic = Credit Transaction Table, Account Detail Table
    3. Hetero. = Account Detail Table + Residence Info Table, Account Detail Table + Occupation Info Table
- **📑 5 Core Table Types**:
  - Credit Transaction Table
  - Residence Info Table
  - Occupation Info Table
  - Account Detail Table
  - Credit Agreement Table

### Three-Aspect Evaluation Framework

#### 1️⃣ **Table Structure Perception (TSP)**
Evaluates MLLMs' ability to comprehend table contents and inter-table relationships. Specifically, TSP assesses models' capacity to perceive table structures, including spatial layouts and cross-table relationships. Evaluation spans two dimensions:
- **Structural perception**: Assessed across multiple cross-table paradigms.
- **Scope perception**: Assessed across three table count ranges (3-5, 6-8, 9-13).

By minimizing domain knowledge and computational demands in question design, we isolate structural perception capabilities. Performance is measured by answer accuracy.

#### 2️⃣ **Domain Knowledge Utilization**
Assesses financial domain expertise through mask-and-recovery evaluation:
- **3 Knowledge Levels**: Perception, Analysis, Reasoning
- **5 Domain Knowledge Types**: Account, Amount, Temporal, Ratio, Weight

#### 3️⃣ **Domain Numerical Calculation**
Tests arithmetic reasoning in financial contexts:
- **3 Calculation Operators**: Addition (+), Subtraction (-), Division (÷)
- **54 Applicant Indicators**: Credit utilization, account duration, turnover efficiency
- **Scenarios**: Real-world calculation from credit assessment

---

## 📊 Dataset Statistics

| Dimension | Count | Description |
|-----------|-------|-------------|
| **Total Samples** | 7,657 | High-quality CTU question-answer pairs |
| **Applicants** | 246 | Unique credit applicant profiles |
| **Credit Tables** | 19,564 | Across 5 major table types |
| **Table Input Numbers** | 12 | Numerical data points per sample |
| **Table Fields** | 60+ | Domain-specific financial fields |
| **Credit Categories** | 5 | Comprehensive credit report coverage |
| **Cross-Table Paradigms** | 3 | Inter-table relationship patterns |
| **Knowledge Levels** | 3 | Perception, Analysis, Reasoning |
| **Domain Knowledge Types** | 5 | Account, Amount, Temporal, Ratio, Weight |
| **Calculation Operators** | 3 | Addition, Subtraction, Division |
| **Applicant Indicators** | 54 | Financial indicators for loan applicants |
| **Question Types** | 3 | Single Selection, Multi Selection, Calculation |

### Credit Table Categories

1. **📝 credit transaction tables**:
2. **💰 residence information tables**: Loan balances, overdrafts, and total credit
3. **💳 occupation information tables**: Card limits, usage, and account duration
4. **📅 account detail tables**: Payment records, delays, and compliance
5. **🔍 credit agreement tables**: Application history and inquiry patterns

---
