# MIS 3371 | Milestone 1 Submission
**Team:** Mathew Budnik, Kamaria Noble, Sebastian Tamayo, Manal Wadif, Christian Saul Hernandez
**Project:** Product Return Request

---

## DOCUMENT 01: Business problem + scope
**Business Problem:** Customers currently request product returns via email or phone calls. Support staff manually verify purchase dates against the 30-day policy and check if items were final sale. This manual process leads to delayed responses, customers asking about their return status, and duplicate requests being filed when customers get impatient.

**In Scope:** Submit one product return request; automatically validate the 30-day window and final-sale eligibility; route defective items over $200 for supervisor approval; show request status to the customer; preserve transaction history.

**Out of Scope:** Actual payment gateway integration for real money movement/refunds, generating physical shipping labels, inventory restocking systems, or accounting software integration.

## DOCUMENT 02: Stakeholders
* **Customer:** Initiates the request. Needs a simple submission form, instant eligibility feedback, and a clear status tracking screen.
* **Customer Support Rep:** Reviews standard returns. Needs accurate order data, return reason codes, and a clear queue of submitted requests.
* **Supervisor:** Approves exceptions. Needs clear visibility into high-value return requests (>$200 defective items) and a way to record their approval/rejection decision.
* **Inventory Auditor:** Monitors return records. Needs traceability of return reasons and system states.

## DOCUMENT 03: Main transaction
**Transaction Event:** Customer submits a product return request.
* **Trigger:** Customer needs to return a purchased item for a refund or replacement.
* **Inputs:** Customer ID, original order number, product/SKU, quantity, reason code, preferred resolution, purchase date, request date.
* **System Action:** Check required data, validate against the 30-day policy and final-sale exclusions; assign a return ID and initial status; route for approval if necessary.
* **Outcome:** Accept for standard processing, route to a supervisor for high-value review, or reject automatically with a reason.

## DOCUMENT 04A: Functional requirements
* **FR-1:** The system shall allow a customer to submit one product return request.
* **FR-2:** The system shall capture the customer ID, order number, SKU, quantity, reason code, and preferred resolution.
* **FR-3:** The system shall automatically reject requests for orders older than 30 days or marked as final-sale.
* **FR-4:** The system shall assign a unique return ID and an initial status.
* **FR-5:** The system shall show the customer the current status of their return.
* **FR-6:** The system shall allow a supervisor to approve or reject requests flagged for high-value review.

## DOCUMENT 04B: Quality / nonfunctional requirements
* **NFR-1:** The form shall be usable by keyboard and utilize accessible HTML labels.
* **NFR-2:** Required-field validation shall clearly identify which specific input the customer must correct.
* **NFR-3:** The system shall preserve key status changes and timestamps for auditability.
* **NFR-4:** The interface shall remain usable on common laptop and mobile screen sizes.

## DOCUMENT 05: User stories + acceptance criteria
* **Customer Story:** As a customer, I want to submit a return request online so that I can easily initiate a refund without calling support. 
  * **Acceptance:** Given valid order details within the 30-day window, when I submit the form, then I receive a unique Return ID and a "Submitted" status.
* **Supervisor Story:** As a supervisor, I want to see high-value return requests so that I can review and approve exceptions. 
  * **Acceptance:** Given a return request for a defective item over $200, when I open the review queue, then the request is visible and awaiting my decision.

## DOCUMENT 06: Business rules
* **BR-1:** The return request date must be within 30 days of the original delivery date.
* **BR-2:** Items flagged as "final-sale" or "clearance" are not eligible for return.
* **BR-3:** The requested return quantity cannot exceed the original purchased quantity.
* **BR-4:** A request citing "defective" for an item valued over $200 requires supervisor approval.

## DOCUMENT 07: Team charter
* **Git / Integration Lead (Technical Anchor):** Mathew Budnik (Manages the GitHub repository, terminal operations, Claude Code prompts, core system architecture, and final code merges. Translates business rules into functional application logic).
* **JavaScript / Logic Lead:** Sebastian Tamayo (Maps out business rules, validation steps, and logic flows. Will pair-program and collaborate directly with the Integration Lead to learn syntax and implement the client-side behavior).
* **Requirements / Product Lead:** Manal Wadif (Manages project scope and user stories. Ensures the final product solves the defined business problem. Zero-coding role).
* **UI / Accessibility Lead:** Kamaria Noble (Designs the interface layout, defines HTML structures, and ensures keyboard/accessibility compliance. Zero-coding role).
* **QA / Documentation Lead:** Christian Saul Hernandez (Executes test scenarios, captures project evidence, and compiles submission documents).

**Team Norms & Communication:** Respond within 24 hours on workdays. Given varying technical backgrounds, the Integration Lead (Mathew) and Logic Lead (Sebastian) will handle code implementation. The Product and UI Leads (Manal, Kamaria) will handle business logic, design deliverables, and non-functional requirements.
**Unresponsive Member Protocol:** If a team member (e.g., Christian) is unresponsive for more than 48 hours, the active team members will immediately absorb their duties (QA and Documentation will be split among active members) to prevent bottlenecks. Missed commitments will be documented for the instructor.
**Git Workflow:** Mathew (Integration Lead) holds primary merge authority. Sebastian will assist with technical commits. Non-technical members will review deliverables via GitHub's web interface or local screenshots to verify business requirements are met before final merges.

## DOCUMENT 08: GitHub repository evidence
**Repository Name:** mis3371-product-return
**Default branch:** main
**Team Members:** Mathew E Budnik, Kamaria R Noble, Sebastian Tamayo, Manal Wadif, Christian Saul Hernandez

* **Repository URL:** https://github.com/mBudnikUH/mis3371-product-return
* **Repository Home Screenshot:**
  [INSERT SCREENSHOT SHOWING README HERE]
* **Collaborators Screenshot:** 
  [INSERT SCREENSHOT OF COLLABORATORS PAGE HERE]
