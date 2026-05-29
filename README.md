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


# Acceptance Criteria

## Feature: Customer Cancels Eligible Order

### Scenario 1: Order is eligible for full refund
Given the customer has an order that is not accepted by restaurant
When the customer clicks Cancel Order
Then system should show 100% refund amount
And customer should be able to confirm cancellation
And order status should become Cancelled
And refund request should be created

### Scenario 2: Order is not eligible for cancellation
Given the delivery partner has picked up the order
When customer opens order details
Then Cancel Order button should be disabled or hidden
And system should display cancellation not allowed message

### Scenario 3: Cancellation fee applies
Given food preparation has started
When customer requests cancellation
Then system should show cancellation fee
And final refundable amount
And customer should confirm before cancellation

### Scenario 4: Refund API fails
Given customer confirms cancellation
When payment gateway refund API fails
Then system should create support queue item
And show refund pending status to customer

### Scenario 5: Admin approves exception refund
Given refund case is in exception queue
When admin approves refund with remarks
Then refund should be initiated
And audit log should capture admin action
# Business Requirements Document (BRD)

## 1. Project Name

Food Delivery App – Order Cancellation & Refund Feature

## 2. Document Purpose

This Business Requirements Document defines the business need, objectives, scope, stakeholders, current pain points, future-state process, business rules, KPIs, assumptions, dependencies, and success criteria for the Order Cancellation & Refund feature.

## 3. Business Background

Food delivery platforms receive frequent customer cancellation and refund requests. In the current process, customers often rely on customer support to understand cancellation eligibility and refund status. This creates delays, increases support workload, and leads to poor customer experience.

## 4. Business Problem

The existing cancellation and refund process is manual, unclear, and inconsistent. Customers do not always know whether they can cancel, how much refund they will receive, or when the refund will be completed. Support teams need to manually verify order state, restaurant action, and payment status.

## 5. Business Objectives

1. Provide a transparent in-app cancellation process.
2. Reduce customer support dependency.
3. Automatically calculate refund amount based on business rules.
4. Improve customer trust through refund tracking.
5. Reduce manual operational effort.
6. Maintain audit trail for dispute handling.
7. Improve SLA compliance for refunds.

## 6. Stakeholders

| Stakeholder | Role / Responsibility |
|---|---|
| Customer | Requests cancellation and tracks refund |
| Restaurant Partner | Receives cancellation updates and confirms preparation status |
| Customer Support | Handles exceptions and customer disputes |
| Finance Team | Ensures refund processing and reconciliation |
| Product Manager | Owns feature roadmap and business outcome |
| Operations Team | Monitors cancellation trends and exceptions |
| Engineering Team | Builds frontend, backend, and integrations |
| Compliance/Legal | Reviews refund policy and audit requirements |

## 7. Scope

### In Scope

- Cancel button visibility based on order state
- Cancellation reason capture
- Refund eligibility validation
- Refund amount preview
- Cancellation confirmation screen
- Refund status tracking
- Customer notification
- Restaurant/admin notification
- Admin exception queue
- Audit log
- Requirement traceability and UAT scenarios

### Out of Scope

- Full payment gateway development
- Restaurant inventory management
- Loyalty point refunds
- Coupon/offer engine redesign
- Full customer support CRM rebuild

## 8. As-Is Process Summary

1. Customer contacts support or tries to cancel manually.
2. Support checks order status manually.
3. Support contacts restaurant/operations.
4. Refund eligibility is checked manually.
5. Customer waits for response.
6. Finance processes refund separately.
7. Customer has limited visibility.

## 9. To-Be Process Summary

1. Customer opens order details.
2. System checks if cancellation is allowed.
3. Customer selects cancellation reason.
4. System calculates refund amount.
5. Customer confirms cancellation.
6. Restaurant/admin/payment gateway is notified.
7. Refund status becomes visible to customer.
8. Audit log is stored.

## 10. Business Requirements

| BR ID | Business Requirement | Priority |
|---|---|---|
| BR-01 | Customers must be able to cancel eligible orders directly from the app. | High |
| BR-02 | Customers must see refund amount before confirming cancellation. | High |
| BR-03 | Cancellation eligibility must be based on order stage. | High |
| BR-04 | Customers must receive cancellation and refund status notifications. | High |
| BR-05 | Support/admin users must be able to manage exceptional refund cases. | Medium |
| BR-06 | Finance users must be able to reconcile refund transactions. | Medium |
| BR-07 | System must maintain complete audit trail for cancellation/refund actions. | High |

## 11. Business Rules

1. Before restaurant acceptance: 100% refund.
2. After restaurant acceptance but before preparation: cancellation fee may apply.
3. After preparation starts: partial/no refund based on policy.
4. Restaurant cancelled order: 100% refund.
5. Payment failure duplicate: full refund to original method.
6. Admin override requires reason and approver ID.
7. Refund SLA should be visible to customer.

## 12. Success Metrics

| KPI | Target |
|---|---|
| Support tickets related to cancellation | Reduce by 30% |
| Average refund status enquiry | Reduce by 40% |
| Refund SLA compliance | > 95% |
| Customer cancellation satisfaction | > 4.2/5 |
| Manual exception cases | < 10% of cancellations |

## 13. Assumptions

- Order status data is available in real time.
- Payment gateway supports refund API.
- Restaurant preparation status is reliable.
- Customer is logged in while requesting cancellation.
- Notification service is available.

## 14. Dependencies

- Order management system
- Payment gateway refund API
- Restaurant partner app
- Notification service
- Admin panel
- Customer support workflow

## 15. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Refund API failure | Customer dissatisfaction | Retry and support queue |
| Incorrect order status | Wrong refund calculation | Real-time status validation |
| Restaurant delay in status update | Dispute | Restaurant SLA and audit |
| Policy confusion | Customer complaints | Clear refund preview |

## 16. Business Outcome

The feature improves transparency, reduces support workload, standardizes cancellation policy, and gives customers clear refund visibility while maintaining operational control and auditability.
# Business Rules

| Rule ID | Business Rule | Priority |
|---|---|---|
| BR-01 | If restaurant has not accepted the order, customer receives 100% refund. | High |
| BR-02 | If food preparation has started, cancellation fee may apply. | High |
| BR-03 | If delivery partner has picked up order, customer cancellation is blocked. | High |
| BR-04 | If restaurant cancels, customer receives 100% refund. | High |
| BR-05 | Refund should be processed to original payment method unless wallet refund is selected. | Medium |
| BR-06 | Admin override must capture approver name, reason, and timestamp. | High |
| BR-07 | Cancellation reason is mandatory. | Medium |
| BR-08 | Refund SLA must be displayed to customer. | High |
| BR-09 | Refund failed cases must move to admin support queue automatically. | High |
| BR-10 | Customer should not be able to submit duplicate cancellation request for same order. | High |
# Process Flow Summary

## As-Is Process

1. Customer contacts support or tries to cancel manually.
2. Support checks order status manually.
3. Support contacts restaurant or operations.
4. Refund eligibility is decided manually.
5. Customer receives delayed update.
6. Finance processes refund manually.
7. Customer has limited refund visibility.

## To-Be Process

1. Customer taps Cancel Order.
2. System checks order status and cancellation rules.
3. System calculates refund amount.
4. Customer reviews cancellation fee and refund timeline.
5. Customer confirms cancellation.
6. Restaurant/admin/payment gateway receives trigger.
7. Refund status is visible to customer.
8. Audit trail is stored.

## Improvement Summary

- Reduced manual support dependency
- Better refund transparency
- Faster cancellation processing
- Lower customer follow-up volume
- Better audit and compliance control
# Requirement Traceability Matrix (RTM)

| Req ID | Requirement | User Story | Use Case | Test Scenario | Priority | Status |
|---|---|---|---|---|---|---|
| FR-01 | Show cancel button for eligible orders | US-01 | UC-01 | TS-01 | High | Approved |
| FR-03 | Capture cancellation reason | US-03 | UC-01 | TS-02 | High | Approved |
| FR-05 | Calculate refund amount | US-02 | UC-02 | TS-03 | High | Approved |
| FR-07 | Confirm cancellation | US-01 | UC-01 | TS-04 | High | Approved |
| FR-10 | Initiate refund request | US-04 | UC-03 | TS-05 | High | In Review |
| FR-11 | Show refund status | US-04 | UC-03 | TS-06 | High | Approved |
| FR-14 | Admin handles exception refund | US-06 | UC-04 | TS-07 | Medium | Draft |
| FR-16 | Export refund report | US-07 | UC-05 | TS-08 | Medium | Draft |
# Software Requirements Specification (SRS)

## 1. Project Name

Food Delivery App – Order Cancellation & Refund Feature

## 2. Purpose

This SRS defines the functional and non-functional requirements for implementing the Order Cancellation & Refund feature in a food delivery mobile application and admin panel.

## 3. System Users

- Customer
- Restaurant Partner
- Admin / Support Agent
- Finance User
- System Scheduler / Notification Service

## 4. Functional Requirements

| FR ID | Functional Requirement | Priority |
|---|---|---|
| FR-01 | System shall display Cancel Order button on order details page when order is eligible. | High |
| FR-02 | System shall hide/disable cancellation option when order is not eligible. | High |
| FR-03 | Customer shall select a cancellation reason before submitting request. | High |
| FR-04 | System shall validate current order stage before cancellation confirmation. | High |
| FR-05 | System shall calculate refund amount based on cancellation policy. | High |
| FR-06 | System shall show refund amount, cancellation fee, and expected refund timeline before confirmation. | High |
| FR-07 | Customer shall confirm cancellation after viewing refund estimate. | High |
| FR-08 | System shall update order status to Cancelled after confirmation. | High |
| FR-09 | System shall notify restaurant partner about cancellation. | Medium |
| FR-10 | System shall initiate refund request to payment gateway. | High |
| FR-11 | Customer shall view refund status from order details. | High |
| FR-12 | System shall send app/email/SMS notification for cancellation and refund status updates. | Medium |
| FR-13 | Admin shall view cancellation/refund requests in admin queue. | Medium |
| FR-14 | Admin shall approve/reject exceptional refund cases. | Medium |
| FR-15 | System shall store audit log for each cancellation/refund action. | High |
| FR-16 | Finance user shall export refund report for reconciliation. | Medium |

## 5. Non-Functional Requirements

| NFR ID | Requirement |
|---|---|
| NFR-01 | Cancellation eligibility check should complete within 2 seconds. |
| NFR-02 | Refund status page should load within 3 seconds. |
| NFR-03 | System should be available 99.5% monthly. |
| NFR-04 | Only authorized users should access refund/admin functions. |
| NFR-05 | All refund actions must be logged for audit. |
| NFR-06 | Customer data and payment information must be protected. |
| NFR-07 | UI should be simple and understandable for non-technical customers. |

## 6. Input Fields

### Customer Cancellation Form

| Field | Type | Required | Validation |
|---|---|---|---|
| Order ID | System generated | Yes | Existing active order |
| Cancellation Reason | Dropdown | Yes | Must select one |
| Additional Comment | Text | No | Max 250 characters |
| Refund Method | Dropdown | Conditional | Wallet/original method if supported |
| Confirmation | Checkbox/Button | Yes | User must confirm |

## 7. Cancellation Reasons

- Ordered by mistake
- Delivery taking too long
- Restaurant requested cancellation
- Found better option
- Payment issue
- Other

## 8. Output / Notifications

- Cancellation confirmation message
- Refund amount message
- Refund reference ID
- Refund timeline
- Admin queue entry for exceptions
- Audit log entry

## 9. API / Integration Requirements

| Integration | Purpose |
|---|---|
| Order Service | Fetch current order status |
| Payment Gateway | Initiate refund |
| Restaurant App | Notify cancellation |
| Notification Service | Send SMS/email/push update |
| Admin Panel | Manage exceptions |

## 10. Error Handling

| Scenario | Expected System Response |
|---|---|
| Order already picked up | Show cancellation not allowed message |
| Payment gateway refund failed | Create support ticket and show pending status |
| Restaurant status unavailable | Show retry option or route to support |
| Customer cancels confirmation | No action taken |
| Refund amount cannot be calculated | Route to admin review |

## 11. Security Requirements

- Customer can only cancel their own order.
- Admin actions require role-based access.
- Refund override must require admin reason.
- Audit log must not be editable by normal users.
- Sensitive payment details should not be displayed.

## 12. Reporting Requirements

The system should support reporting on:

- Total cancellation requests
- Refund amount processed
- Cancellation reason distribution
- Refund SLA breach count
- Admin exception cases
- Restaurant-wise cancellation count

## 13. Acceptance Criteria Summary

- Customer can cancel eligible order successfully.
- Refund estimate is shown before cancellation.
- Ineligible orders cannot be cancelled by customer.
- Refund status is visible after cancellation.
- Admin can handle exception cases.
- Audit log is generated.
# Test Scenarios / UAT Scenarios

| Test ID | Scenario | Expected Result |
|---|---|---|
| TS-01 | Customer opens eligible order | Cancel button should be visible |
| TS-02 | Customer submits cancellation without reason | System should show validation error |
| TS-03 | Customer cancels before restaurant accepts | Full refund should be calculated |
| TS-04 | Customer cancels after preparation starts | Cancellation fee should apply |
| TS-05 | Customer cancels after delivery pickup | Cancellation should be blocked |
| TS-06 | Refund API success | Refund status should show Initiated/Processed |
| TS-07 | Refund API failure | Case should move to admin queue |
| TS-08 | Admin approves exception refund | Refund should initiate and audit log should update |
| TS-09 | Finance exports refund report | Report should download with correct data |
| TS-10 | Customer tracks refund status | Refund stage and expected date should display |
# Use Cases

| Use Case ID | Use Case Name | Primary Actor | Goal |
|---|---|---|---|
| UC-01 | Cancel Eligible Order | Customer | Cancel order directly from app |
| UC-02 | View Refund Estimate | Customer | Understand refund before cancellation |
| UC-03 | Track Refund Status | Customer | Monitor refund progress |
| UC-04 | Review Exception Refund | Support/Admin | Handle non-standard refund cases |
| UC-05 | Export Refund Report | Finance | Reconcile refund transactions |

## UC-01: Cancel Eligible Order

### Actor
Customer

### Preconditions
- Customer is logged in.
- Order belongs to customer.
- Order is in eligible state.

### Main Flow
1. Customer opens order details.
2. Customer taps Cancel Order.
3. System checks order stage.
4. Customer selects cancellation reason.
5. System displays refund estimate.
6. Customer confirms cancellation.
7. System updates order status.
8. System initiates refund.
9. Customer receives confirmation.

### Alternate Flow
If order is not eligible, system displays cancellation not allowed message and support contact option.

### Postconditions
- Order is cancelled.
- Refund request is created.
- Audit log is stored.
# User Stories

## Customer Stories

### US-01: Cancel Eligible Order
As a customer, I want to cancel an eligible order from the app so that I do not need to contact support.

### US-02: View Refund Estimate
As a customer, I want to see refundable amount before confirming cancellation so that I can make an informed decision.

### US-03: Select Cancellation Reason
As a customer, I want to select a cancellation reason so that the business can understand cancellation patterns.

### US-04: Track Refund Status
As a customer, I want to track refund status so that I know when my money will be returned.

## Admin / Support Stories

### US-05: View Exception Cases
As a support agent, I want to view refund exceptions so that I can resolve customer issues quickly.

### US-06: Override Refund Decision
As an admin, I want to override refund decisions with remarks so that genuine exceptional cases can be handled.

## Finance Stories

### US-07: Export Refund Report
As a finance user, I want to export refund reports so that I can reconcile refund transactions.

## Restaurant Partner Stories

### US-08: Receive Cancellation Notification
As a restaurant partner, I want to receive cancellation notifications so that preparation can be stopped when possible.
