# Cybersecurity Governance, Risk & Human Risk Executive Scorecard (Power BI)

![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Data%20Modeling-0078D4?style=for-the-badge)
![Star Schema](https://img.shields.io/badge/Architecture-Star%20Schema%20(12%20Tables)-0D9488?style=for-the-badge)
![Frameworks](https://img.shields.io/badge/Frameworks-NIST%20CSF%202.0%20%7C%20CIS%20v8.1%20%7C%20ISO%2027001%20%7C%20PCI--DSS%20%7C%20SOC%202-1E3A8A?style=for-the-badge)

An interactive, two-page **Microsoft Power BI** executive dashboard designed for **Cybersecurity Strategy, Governance, Risk & Compliance (GRC)** leadership. Built to consolidate 24 months of multi-domain telemetry (2023–2024) across **Cybersecurity Maturity Assessments (CMA)**, **Issue & Exception Remediation SLAs**, **Human Risk Management (Phishing & Security Awareness)**, and **Operational Security & Patch Compliance**.

---

## Dashboard Preview

### Page 1: Executive Governance & Human Risk Scorecard
Provides leadership with a single-pane view of control maturity against target state, remediation SLA performance, phishing resilience trends, department human risk scores, and incident financial exposure.

![Executive Scorecard Dashboard](Executive%20Scorecard%20Dashboard.png)

#### Interactive Cross-Filtering (Synced Multi-Page Slicers)
Executives and audit stakeholders can dynamically slice all KPIs and visuals across both report pages by **Reporting Year**, **Business Department**, and **Compliance Framework**:

* **Filter by Reporting Year (2023 vs. 2024 YoY Comparison):**
  ![Executive Scorecard Year Slicer](Executive%20Scorecard_Year_Expanded.png)

* **Filter by Business Unit / Department:**
  ![Executive Scorecard Department Slicer](Executive%20Scorecard_Department_Expanded.png)

* **Filter by Regulatory & Control Framework:**
  ![Executive Scorecard Framework Slicer](Executive%20Scorecard_Framework_Expanded.png)

---

### Page 2: Governance Action Register & Risk Drill-Down
Operational register for tracking open audit findings, control gaps, overdue remediation items, and active policy exceptions—featuring conditional severity formatting and exposure breakdowns by record type and status.

![Action Register Dashboard](Action%20Register%20Dashboard.png)

#### Department-Level Accountability Drill-Down
Filtering by business unit isolates overdue items, active exceptions, and SLA targets for targeted stakeholder follow-up:

![Action Register Department Drill-Down](Action%20Register_Department_Expanded.png)

---

## Business Problem & Governance Objectives

Enterprise security programs often struggle with fragmented reporting across GRC platforms, security awareness tools, and operational vulnerability/SOC logs. This solution unifies those telemetry streams into an executive-ready **Star Schema** data model that answers four core leadership questions:

1. **Program Maturity (CMA):** How is control maturity progressing toward target state across NIST CSF 2.0, CIS Controls v8.1, ISO/IEC 27001, PCI-DSS, and SOC 2?
2. **Governance & Issue Management:** What percentage of audit findings, control gaps, and process actions meet remediation SLAs, and which items are overdue or operating under active policy exceptions?
3. **Human Risk & Security Awareness:** Are phishing simulation click rates decreasing and employee reporting rates improving across high-exposure business units?
4. **Control Effectiveness & Operational Alignment:** How do quarterly patch compliance rates and security incident trends correlate with overall governance posture?

---

## Key Metrics & Verified Results (2023 vs. 2024)

| Governance Domain | KPI / KRI Metric | 2024 Performance | YoY Change vs. 2023 |
| :--- | :--- | :---: | :---: |
| **Cybersecurity Maturity (CMA)** | Average CMA Maturity Score (5.0 Scale) | **3.61** (Q4: **3.80**) | **+0.45 pts** |
| **Cybersecurity Maturity (CMA)** | Average Control Effectiveness | **86.2%** | **+12.8 pts** |
| **Issue & Exception Governance** | Remediation SLA Compliance Rate | **79.0%** | **+1.4 pts** |
| **Issue & Exception Governance** | Active Governance Backlog | **44 Items** (18 Overdue, 9 Exceptions) | Tracked to Resolution |
| **Human Risk Management** | Phishing Simulation Click Rate | **4.58%** | **-1.69 pts** (Risk Reduction) |
| **Human Risk Management** | Phishing Report Rate / Training Completion | **65.4%** / **91.5%** | **+14.2 pts** / **+10.5 pts** |
| **Vulnerability & Patch Governance** | Quarterly Patch Compliance Rate | **83.5%** | **+13.7 pts** |

---

## Star Schema Data Architecture

The semantic model separates **6 Lookup Dimension tables** (`1` side) from **6 Fact tables** (`*` side) via single-direction relationships for unambiguous filter propagation:

* **Dimensions (`dim_*`):** `dim_date`, `dim_department`, `dim_security_domain`, `dim_severity`, `dim_attack_type`, `dim_attack_source`
* **Governance & Human Risk Facts:** `fact_cma_maturity`, `fact_grc_issues_exceptions`, `fact_human_risk_awareness`
* **Operational Security Facts:** `fact_patch_compliance`, `fact_incidents`, `fact_firewall_uptime`

---

## Repository Contents

```text
├── Executive Scorecard Dashboard.png
├── Executive Scorecard_Year_Expanded.png
├── Executive Scorecard_Department_Expanded.png
├── Executive Scorecard_Framework_Expanded.png
├── Action Register Dashboard.png
├── Action Register_Department_Expanded.png
└── README.md
