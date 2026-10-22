# SAP S/4HANA - Integrated Sold-to-Cash Cycle & Analytics

## Overview

This project documents a hands-on **SAP S/4HANA Sales and Distribution (SD)** case study completed as part of the **Supply Chain & Operations Analytics** course in the MBA-DS&DA program at Symbiosis Centre for Information Technology.

The case study focused on executing and analysing an **Integrated Sold-to-Cash (S2C) Cycle** using the Global Bike (GBI) business scenario.

The project combines SAP transaction execution, supply chain process understanding, KPI design, data classification, and Agentic AI use-case analysis.

---

## Business Process

The project covered the complete Sold-to-Cash cycle:

**Customer Creation → Inquiry → Quotation → Sales Order → Stock Check → Sales Order Tracking → Delivery → Goods Issue → Invoice → Customer Payment → Document Flow**

The completed case study used **Big Apple Bikes** as the customer.

### Key SAP Transaction Flow

| Process | Document / Result |
|---|---|
| Customer | BP 126119 – Big Apple Bikes |
| Inquiry | 10000053 – USD 21,400.00 |
| Quotation | 20000044 – USD 20,092.50 |
| Sales Order | Order 45 – 5 EA + 2 EA |
| Delivery | 80000042 |
| Goods Issue | 4900038079 |
| Invoice | 90000032 – USD 20,092.50 |
| Customer Payment | FI JE 1400000030 |

The transaction flow demonstrated how sales, inventory, logistics and financial activities are connected within an integrated ERP process.

---

## SAP Organizational Structure

The case study used the following organizational data:

- **Sales Organization:** US East (UE00)
- **Distribution Channel:** Wholesale (WH)
- **Division:** Bicycles (BI)
- **Plant:** DC Miami (MI00)
- **Storage Location:** Finished Goods (FG00)
- **Company Code:** Global Bike Inc. (US00)

---

## Data Types Identified

Four categories of data required to execute and analyse the S2C cycle were identified:

### 1. Organizational Data

Examples:

- Sales Organization
- Distribution Channel
- Division
- Plant
- Storage Location
- Company Code

### 2. Master Data

Examples:

- Customer master
- Material master
- Material sales data
- Pricing condition records
- Customer account
- G/L accounts

### 3. Transactional Data

Examples:

- Inquiry
- Quotation
- Sales Order
- Outbound Delivery
- Goods Issue
- Billing Document
- Journal Entries
- Customer Payment

### 4. Situational Data

Examples:

- Ordered quantities
- Requested delivery dates
- Customer discounts
- Stock availability
- Picking status
- Shipping date
- Payment status
- Billing block/posting status

---

## KPI Design

The project included analytical KPI design for two S2C roles.

### Sales Person

**1. Quote-to-Order Conversion within Validity (%)**

Measures the percentage of quotations converted into orders before their validity date.

**Why it matters:**  
Helps assess whether quotations are successfully converted into confirmed demand within the permitted period.

**2. Price Realization (%)**

Measures the net value after discounts relative to the gross value.

**Why it matters:**  
Helps evaluate the impact of discounts on realized selling value.

Example from the case:

- Inquiry value: USD 21,400.00
- Quotation value: USD 20,092.50
- Price realization: approximately **93.9%**

---

### Warehouse Supervisor

**1. On-Time Goods Issue (%)**

Measures deliveries for which the actual Goods Issue date is on or before the planned Goods Issue date.

**Why it matters:**  
Goods Issue is an important step in the order-to-cash cycle because delays can affect subsequent billing.

**2. First-Time-Right Goods Issue (%)**

Measures deliveries processed without errors or rework.

**Why it matters:**  
Helps identify operational issues such as stock availability or master-data problems that can interrupt the fulfillment process.

---

## Agentic AI Use Cases

The case study also explored how Agentic AI could support selected S2C roles.

### 1. Sales Person – Quotation Pricing & Follow-up Agent

**Data:** Customer history, pricing conditions, discounts, stock availability and quotation validity.

**AI Actions:**
- Draft quotation from inquiry
- Flag unusual discount overrides
- Remind about approaching quotation expiry

**Human Decision:**
- Approve final discount

**Decision Supported:**
- Which quotations should be followed up?
- What discount can be offered while protecting value?

---

### 2. Warehouse Supervisor – Delivery Readiness Agent

**Data:** Stock by plant/storage location, open orders, planned Goods Issue dates and picking status.

**AI Actions:**
- Check stock and delivery readiness
- Prioritize picking
- Propose Goods Issue
- Raise replenishment request when stock is low

**Human Decision:**
- Approve the final posting

**Decision Supported:**
- Which deliveries should be prioritized?
- When should inventory be replenished or a shipment split?

---

### 3. Accountant – Billing & Cash Collection Agent

**Data:** Goods Issue status, billing documents, payment terms, bank receipts, open items and ageing.

**AI Actions:**
- Propose invoice after Goods Issue
- Match payments with open items
- Draft overdue payment reminders

**Human Decision:**
- Approve billing/posting actions

**Decision Supported:**
- Whether a billing document should be released or held
- Which overdue customers require escalation

---

## Tools & Technologies

- **SAP S/4HANA**
- **SAP Fiori**
- **Global Bike (GBI) business scenario**
- **Claude (Anthropic)** – KPI and Agentic AI ideation
- Supply Chain & Operations Analytics concepts

---

## Key Learning Outcomes

- Understanding of the integrated **Sold-to-Cash business process**
- Hands-on exposure to SAP SD workflow execution
- Understanding of how SD connects with **MM and FI**
- Identification of organizational, master, transactional and situational data
- KPI design based on operational roles
- Linking business KPIs with underlying SAP data
- Understanding potential applications of Agentic AI in ERP workflows
- Translating business processes into data-driven decisions

---

## Project Deliverables

- SAP SD Sold-to-Cash case study presentation
- Process-flow screenshots
- KPI analysis
- Data Types Matrix
- Agentic AI use-case analysis
- GenAI prompts and research references

---

## Academic Context

**Course:** Supply Chain & Operations Analytics  
**Program:** MBA – Data Science & Data Analytics  
**Semester:** III  
**Institute:** Symbiosis Centre for Information Technology  
**Case Study:** Integrated Sold-to-Cash Cycle – 30 Marks

---

## Note

This repository documents an **academic hands-on SAP S/4HANA case study** and is intended to demonstrate practical exposure to ERP processes, business analytics and supply chain operations. It does not represent production SAP implementation experience.
