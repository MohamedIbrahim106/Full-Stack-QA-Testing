/Test_Cases
  ├── Task_I_User_Stories_Test_Cases.xlsx
  ├── Task_II_Bug_Report.xlsx
  ├── Task_III_Checkout_Test_Plan.docx
  ├── Task_IV_API_Test_Cases.xlsx
/Postman
  ├── Bosta_API_Environment.json
  ├── Bosta_API_Collection.json
/Readme.md

# Full-Stack-QA-Testing
A comprehensive QA testing project covering user story validation, manual functional testing, bug reporting, checkout process test planning, and API testing with Postman. Includes detailed test cases, bug reports, API assertions, and structured documentation for portfolio and professional review.

Project Title: QA Testing Assignment – Comprehensive Manual & API Testing
Overview
This project involves creating detailed test documentation, executing manual tests, preparing bug reports, and performing API testing using Postman. The goal is to ensure full functional coverage for the provided user stories, website functionalities, checkout process, and delivery tracking API.

Task I – Test Case Creation for User Stories
Create a well-structured and comprehensive set of test cases for the following user stories, covering all positive, negative, boundary, and edge cases.

User Story 1: Open a Credit Card Account
As a customer,
I want to open a credit card account,
So that I can receive applicable discounts.

Acceptance Criteria:

If the customer is new, they get a 15% discount on all purchases today.

If the customer is existing and has a loyalty card, they get a 10% discount.

If the customer has a coupon, they get a 20% discount (cannot be combined with the new customer discount).

Discount amounts are additive where applicable (except the new customer rule).

User Story 2: Contact Us
As a customer,
I want to contact the website about a problem with my product,
So that I can get support.

Acceptance Criteria:

Email field is mandatory and must be valid (format: name@domain.xyz).

Contact Name field is mandatory.

Message field is mandatory and must not exceed 500 characters.

User Story 3: WhatsApp Plugin
As a business,
I want to use a WhatsApp plugin in my dashboard,
So that I can communicate with my customers.

Acceptance Criteria:

WhatsApp plugin is installed via phone number and OTP.

User can chat with customers.

User can share dashboard-saved products with customers.

User can send images to customers.

Deliverable:

Test cases should include:

Test Case ID

Description

Preconditions

Steps to Execute

Expected Result

Actual Result (to be filled during execution)

Status (Pass/Fail)

Priority & Severity (optional)

Task II – Manual Testing & Bug Reporting
Visit the target website.

Perform manual testing on:

Add to cart functionality.

Products sorting functionality.

Identify and document any bugs found.

Bug Report Format:

Bug ID

Title

Description

Steps to Reproduce

Expected Result

Actual Result

Screenshots (if applicable)

Severity

Priority

Task III – Test Plan for Full Checkout Process
Design a comprehensive test plan covering:

Adding items to cart.

User authentication.

Applying discount.

Entering shipping details.

Payment (via 3rd party integration).

Order confirmation.

The plan should include:

Scope

Test Objectives

Test Approach

Test Data

Roles & Responsibilities

Test Environment

Test Schedule

Risks & Mitigation

Deliverables

Task IV – API Testing for Delivery History
API Endpoint:
GET https://tracking.bosta.co/shipments/track/:trackingNumber

Test Data (Tracking Numbers):

6636234

7234258

9442984

1094442

URL Params:

Param	Type	Mandatory	Description
trackingNumber	string	Yes	The delivery tracking number.

Headers:

Field	Type	Description
Content-Type	string	application/json or text/xml (default: application/json)
X-Requested-By	string	Landmark
Accept	string	application/json or application/xml (default: application/json)

Success Response (200):

CurrentStatus – TrackingCurrentStatus object.

TrackingNumber – string.

TrackingURL – array of customer support numbers.

SupportPhoneNumbers – array of strings.

CreateDate – creation date of delivery.

TransitEvents – array of TrackingTransitEvent objects containing full delivery history.

Error Codes:

404 – No delivery matched the given tracking number.

500 – Server error.

Deliverables:

Test cases for:

Valid tracking numbers.

Invalid tracking numbers.

Boundary/edge scenarios.

Error handling.

Postman:

Create a new environment with the base URL (https://tracking.bosta.co).

Use a tracking number as a variable.

Add assertions:

Response code is 200.

Response time is < 100ms
