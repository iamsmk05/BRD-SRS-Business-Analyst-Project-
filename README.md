# Food Delivery App – Order Cancellation & Refund Feature

## Project Overview

This repository is a **Business Analyst portfolio project** focused on writing a complete **Business Requirements Document (BRD)** and **Software Requirements Specification (SRS)** for an end-to-end app feature.

The selected feature is an **Order Cancellation & Refund Management Feature** for a fictional food delivery mobile application. The project shows how a Business Analyst converts a business problem into clear scope, requirements, user stories, process flows, business rules, wireframes, acceptance criteria, and traceability.

---

## Project Objective

To define complete business and functional requirements for a digital order cancellation and refund feature that helps customers cancel eligible orders, view refund estimates, track refund status, and helps support/admin teams handle exceptions with proper audit trail.

---

## Business Problem

Customers currently face confusion while cancelling food orders because cancellation eligibility, refund amount, refund status, and cancellation charges are not transparent. Support teams manually verify order status with restaurant partners and payment teams, resulting in delays, disputes, repeated customer follow-ups, and poor customer experience.

---

## Proposed Solution

Build an in-app cancellation and refund workflow where:

- Customers can cancel eligible orders directly from the app.
- System checks order stage and business rules automatically.
- Refund amount is calculated before confirmation.
- Customer receives refund status updates.
- Admin/support team can manage exceptions.
- Every action is captured in audit logs.

---

## Stakeholders

| Stakeholder | Interest |
|---|---|
| Customer | Cancel order, view refund, track status |
| Restaurant Partner | Receive cancellation update, avoid food waste |
| Customer Support | Resolve refund/cancellation disputes |
| Finance Team | Process refund accurately |
| Product Manager | Improve customer experience and retention |
| Operations Team | Reduce manual intervention |
| Engineering Team | Build app/backend/payment workflow |
| Legal/Compliance | Ensure fair refund policy and audit trail |

---

## Key KPIs

| KPI | Purpose |
|---|---|
| Cancellation Request Volume | Track feature usage |
| Refund Success Rate | Measure refund completion efficiency |
| Average Refund Processing Time | Monitor customer experience |
| Support Tickets Related to Cancellation | Measure reduction in manual support |
| Cancellation Fee Collected | Track business impact |
| Exception Cases | Identify manual intervention volume |
| Customer Satisfaction After Refund | Track experience quality |

---

## In Scope

- Customer cancellation request flow
- Refund eligibility check
- Refund amount preview
- Cancellation reason capture
- Customer confirmation screen
- Admin/support exception queue
- Notification triggers
- Audit trail
- Refund status tracking
- Requirement traceability and test scenarios

## Out of Scope

- Full food delivery app development
- Payment gateway implementation
- Restaurant inventory automation
- Loyalty/referral refunds
- Wallet product implementation

---

## Deliverables Included

| Folder | Content |
|---|---|
| documentation/ | BRD, SRS, user stories, use cases, RTM, acceptance criteria, business rules, test scenarios |
| diagrams/ | As-Is process, To-Be process, feature context diagram |
| wireframes/ | Feature wireframe image |
| dashboard/ | Requirement management dashboard image |
| presentation/ | PPT and PDF case study |
| linkedin/ | LinkedIn carousel, preview image, caption |

---

## Functional Requirement Summary

- Customer can view cancel button based on order stage.
- System validates cancellation eligibility.
- System calculates refundable amount.
- Customer selects cancellation reason.
- Customer confirms cancellation.
- System triggers restaurant/admin/payment notifications.
- Customer can track refund status.
- Admin can approve/reject exception refunds.
- System maintains audit logs.

---

## Business Rules Summary

- If restaurant has not accepted the order, customer gets 100% refund.
- If food preparation has started, cancellation fee may apply.
- If restaurant cancels the order, customer gets 100% refund.
- Refund should be processed to original payment method unless wallet refund is selected.
- Cancellation is not allowed after delivery partner picks up order, except admin exception.
- Admin override must capture reason and approver details.

---

## Repository Structure

```text
requirements-brd-srs-food-delivery-feature/
│
├── README.md
├── documentation/
│   ├── BRD.md
│   ├── SRS.md
│   ├── User_Stories.md
│   ├── Use_Cases.md
│   ├── Business_Rules.md
│   ├── Acceptance_Criteria.md
│   ├── RTM.md
│   └── Test_Scenarios.md
│
├── diagrams/
│   ├── as_is_process_flow.png
│   ├── to_be_process_flow.png
│   └── feature_context_diagram.png
│
├── wireframes/
│   └── feature_wireframe.png
│
├── dashboard/
│   └── requirements_dashboard.png
│
├── presentation/
│   ├── brd_srs_case_study.pptx
│   └── brd_srs_case_study.pdf
│
└── linkedin/
    ├── linkedin_preview.png
    ├── linkedin_carousel.pdf
    └── linkedin_post_caption.txt
```

---

## Skills Demonstrated

- Business Requirement Documentation
- Software Requirement Specification
- Requirement Elicitation
- Stakeholder Analysis
- Functional Requirements
- Non-Functional Requirements
- User Stories
- Acceptance Criteria
- Use Case Writing
- Process Mapping
- Business Rule Definition
- Requirement Traceability Matrix
- UAT/Test Scenario Planning
- Product Workflow Thinking

---

## Author

Business Analyst Portfolio Project
