# Bharat Tender Intelligence (BTI)

### AI-Powered Tender Intelligence, Transparency & Fraud Detection Platform

Bharat Tender Intelligence (BTI) is an AI-powered digital platform designed to improve transparency, security, and efficiency in public procurement and MPLAD Scheme project implementation.

The platform connects government authorities, verified implementing agencies, and citizens through a structured tender lifecycle while using AI-assisted intelligence, explainable evaluation, anomaly detection, and audit mechanisms to identify potential risks and improve decision-making.

---

## 🎯 Problem Statement

Public procurement and project implementation involve large amounts of tender, agency, proposal, financial, and monitoring data.

Manual processes can make it difficult to:

- Identify suspicious tender or proposal patterns
- Verify implementing agencies efficiently
- Compare proposals consistently
- Detect potential anomalies and irregularities
- Track project execution transparently
- Maintain a reliable audit trail
- Provide citizens with meaningful transparency

BTI addresses these challenges through a centralized, role-based, AI-assisted tender intelligence platform.

---

## 💡 Our Solution

BTI provides a complete digital workflow covering:

**Agency Verification → Tender Creation → Tender Discovery → Proposal Submission → AI-Assisted Evaluation → Government Review → Award → Project Monitoring → Risk & Anomaly Intelligence → Audit**

The platform is designed around three primary user groups:

### 🏛️ Government Portal
Government authorities can:

- Create and manage tenders
- Review verified agencies
- Evaluate submitted proposals
- Use AI-assisted proposal intelligence
- Shortlist and award proposals
- Monitor projects
- View risk alerts and analytics
- Investigate potential fraud or anomalies
- Access audit logs

### 🏢 Agency Portal
Verified implementing agencies can:

- Complete organization registration
- Submit GSTIN-based verification information
- Maintain compliance information
- Discover relevant tenders
- View tender requirements
- Understand tender-agency matching
- Submit proposals
- Track proposal status
- Monitor awarded project activities

### 👥 Public/Citizen Portal
Citizens can access transparency-oriented information about public projects and implementation activities without requiring access to restricted government operations.

---

## 🔐 Key Features

### 1. Verified Agency Registration

BTI uses GSTIN-based organization verification to establish an authoritative organization identity.

The verification workflow includes:

- GSTIN normalization
- GSTIN validation
- Organization records
- Verification status
- Verification events
- Government verification review
- Audit history

Only verified agencies receive full access to tender participation workflows.

---

### 2. Government Tender Management

Government users can create and manage tenders with structured information including:

- Tender title
- Category
- Description
- Location
- Financial requirements
- Capability requirements
- Special requirements
- Important dates
- Closing date
- Tender status

Draft and published tender states are handled separately to prevent incomplete tenders from becoming publicly actionable.

---

### 3. Intelligent Tender Discovery

BTI matches verified agencies with relevant tenders using a weighted matching model.

### Matching Score — 100 Points

| Parameter | Maximum Score |
|---|---:|
| Category Match | 35 |
| Geography Match | 25 |
| Capabilities | 20 |
| Financial Eligibility | 20 |
| **Total** | **100** |

The platform also provides an explanation of why a tender matches an agency rather than presenting only an unexplained score.

---

### 4. Proposal Management

Agencies can submit structured proposals against eligible tenders.

The proposal workflow includes:

- Proposal creation
- Draft saving
- Compliance declarations
- Experience information
- Past project information
- Proposal submission
- Government review
- Shortlisting
- Award workflow

---

### 5. AI Proposal Intelligence

BTI integrates AI-assisted proposal intelligence into the government proposal review workflow.

Instead of replacing the government's decision, the AI provides decision-support information such as:

- Overall proposal assessment
- Evaluation dimensions
- Structured scoring
- Strengths
- Potential weaknesses
- Supporting reasoning
- Explainable evaluation information

The final decision remains with the authorized government user.

---

### 6. Project Monitoring

After a proposal is awarded, BTI provides project monitoring capabilities to track implementation progress.

Government users can monitor project milestones and implementation information through the centralized portal.

---

### 7. Risk & Anomaly Intelligence

BTI is designed to identify potential irregularities and risk patterns across tender and project data.

The intelligence layer can be used to surface:

- Suspicious patterns
- Unusual project activity
- Risk indicators
- Potential anomalies
- Relationships between procurement records
- Cases requiring further investigation

The system is intended as a **decision-support and investigation aid**, not as an automatic declaration of fraud.

---

### 8. Audit Trail

Important actions within the platform are designed to maintain traceability.

Audit information can support:

- Verification activities
- Tender lifecycle events
- Proposal workflow events
- Government decisions
- Project monitoring activities
- Investigation workflows

This improves accountability and makes important actions easier to review.

---

## 🏗️ System Architecture

```text
                    ┌───────────────────────┐
                    │      Public Portal    │
                    └───────────┬───────────┘
                                │
                    ┌───────────▼───────────┐
                    │   Bharat Tender       │
                    │   Intelligence (BTI)  │
                    └───────────┬───────────┘
                                │
          ┌─────────────────────┼─────────────────────┐
          │                     │                     │
 ┌────────▼────────┐   ┌────────▼────────┐   ┌───────▼────────┐
 │ Government      │   │ Verified Agency │   │ AI Intelligence│
 │ Portal          │   │ Portal          │   │ Layer          │
 └────────┬────────┘   └────────┬────────┘   └───────┬────────┘
          │                     │                     │
          └─────────────────────┼─────────────────────┘
                                │
                    ┌───────────▼───────────┐
                    │       Firebase        │
                    │ Auth + Firestore      │
                    └───────────┬───────────┘
                                │
                    ┌───────────▼───────────┐
                    │ Audit / Risk /        │
                    │ Monitoring Data       │
                    └───────────────────────┘
