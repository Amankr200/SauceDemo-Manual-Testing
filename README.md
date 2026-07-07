# SauceDemo Manual Testing Portfolio


## Project Overview

This repository showcases a complete end-to-end Manual Testing portfolio for the [SauceDemo](https://www.saucedemo.com/) e-commerce web application. It was created to demonstrate professional QA skills including test planning, test case design, defect reporting, and traceability.

> **Application Under Test (AUT):** SauceDemo — https://www.saucedemo.com/  
> **Application Type:** E-Commerce Web Application  
> **Testing Type:** Manual Functional Testing  
> **Tester:** Aman Kumar

---

## Objective

Performed end-to-end manual testing of the SauceDemo e-commerce application to:
- Validate core business functionalities across all major modules
- Identify and document defects using industry-standard bug reporting
- Ensure the application meets expected requirements
- Demonstrate professional QA documentation skills

---

## Repository Structure

```
SauceDemo-Manual-Testing/
│
├── README.md                              <- This file
├── Test Plan.md                           <- Comprehensive test plan document
├── Test Scenarios.csv                     <- 30 test scenarios
├── Test Cases.csv                         <- 52 detailed test cases
├── Bug Reports.csv                        <- Identified & practice bug reports
├── RTM.csv                                <- Requirement Traceability Matrix
├── Test Data.csv                          <- Test data used during testing
├── Test Summary Report.md                 <- Final test execution summary
├── Screenshots/                           <- Test execution evidence
│   ├── 01_Login_Page.png
│   ├── 02_Product_Listing_Page.png
│   ├── 03_Product_Detail_Page.png
│   ├── 04_Cart_Page.png
│   ├── 05_Checkout_Step1_Your_Information.png
│   ├── 06_Checkout_Step2_Overview.png
│   ├── 07_Checkout_Complete.png
│   ├── 08_Error_Locked_Out_User.png
│   └── 09_Error_Invalid_Credentials.png
└── JIRA/                                  <- JIRA bug tracking simulation (CSV)
    ├── JIRA_Bug_Tracker.csv              <- Master tracker - all 10 bugs
    ├── BUG-001.csv                        <- Locked user session path review
    ├── BUG-002.csv                        <- Checkout active with empty cart
    ├── BUG-003.csv                        <- Back button bypasses logout
    ├── BUG-004.csv                        <- Wrong images for problem_user
    ├── BUG-005.csv                        <- Sort preference not persisted
    ├── BUG-006.csv                        <- Error styling not auto-cleared
    ├── BUG-007.csv                        <- No order confirmation email
    ├── BUG-008.csv                        <- Add to Cart casing inconsistency
    ├── BUG-009.csv                        <- Performance glitch user delay
    └── BUG-010.csv                        <- Postal code field no validation
```

---

## Modules Tested

| Module | Description |
|---|---|
| Login | Authentication, validation, error handling |
| Product Listing | Product display, sorting, filtering |
| Product Detail | Individual product view, add to cart |
| Cart | Add/remove items, quantity, badge count |
| Checkout | Multi-step checkout, form validation, order completion |
| Navigation | Menu, logout, browser back button |
| UI & Usability | Layout, alignment, error message styling |

---

## Deliverables

| Deliverable | Description | Status |
|---|---|---|
| [Test Plan](./Test%20Plan.md) | Project scope, strategy, risks | Complete |
| [Test Scenarios](./Test%20Scenarios.csv) | 30 high-level test scenarios | Complete |
| [Test Cases](./Test%20Cases.csv) | 52 detailed step-by-step test cases | Complete |
| [Bug Reports](./Bug%20Reports.csv) | 8 directly observed/practice defects | Complete |
| [RTM](./RTM.csv) | Requirement Traceability Matrix | Complete |
| [Test Data](./Test%20Data.csv) | Input data for all test cases | Complete |
| [Test Summary Report](./Test%20Summary%20Report.md) | Final execution results | Complete |
| [Screenshots](./Screenshots/) | Visual test evidence | Complete |
| [JIRA Bug Tracker](./JIRA/JIRA_Bug_Tracker.csv) | Master JIRA simulation - all 10 bugs | Complete |
| [JIRA Individual Reports](./JIRA/) | BUG-001 to BUG-010 in CSV format | Complete |

---

## Test Summary

| Metric | Count |
|---|---|
| Total Test Scenarios | 30 |
| Total Test Cases | 52 |
| Passed | 51 |
| Failed | 1 |
| Blocked | 0 |
| Bugs Identified (CSV) | 8 |
| JIRA Bug Reports (Excel) | 10 |
| Test Coverage | ~95% |
| Test Completion | 98.1% |

---

## Skills Demonstrated

- Manual Testing — Hands-on test execution across all modules
- Functional Testing — Validating features against expected behavior
- Regression Testing — Re-testing post-fix scenarios
- Smoke Testing — Core functionality validation
- Test Case Design — Writing clear, reusable, detailed test cases
- Test Scenario Design — Identifying coverage areas from requirements
- Bug Reporting — Structured defect documentation with severity/priority
- JIRA Bug Tracking Simulation — 10 professional bug reports using JIRA-style templates in CSV format
- Defect Life Cycle — Bug ID, status tracking, severity/priority classification
- Requirement Traceability Matrix (RTM) — Mapping requirements to tests
- SDLC & STLC — Understanding of software and test life cycles

---

## JIRA Bug Tracking Simulation

A complete JIRA-style bug tracking simulation is included in the `JIRA/` folder. All reports are in Excel format (.xlsx).

**No real JIRA instance required** — this demonstrates the same professional defect management skills using a JIRA-like template structure.

### Master Bug Tracker

| File | Contents |
|---|---|
| [JIRA_Bug_Tracker.csv](./JIRA/JIRA_Bug_Tracker.csv) | All 10 bugs in one flat table with: Bug ID, Summary, Module, Severity, Priority, Status, Assignee, Steps, Expected Result, Actual Result |

### Individual Bug Reports

Each bug report follows a professional JIRA-style template with:
- Bug ID, Summary, Module, Type
- Severity, Priority, Status, Assignee, Reporter
- Description
- Steps to Reproduce
- Expected Result
- Actual Result
- Environment and date information

| Bug ID | Summary | Severity | Priority | Status |
|---|---|---|---|---|
| [BUG-001](./JIRA/BUG-001.csv) | Locked user session path needs review | Major | High | Open |
| [BUG-002](./JIRA/BUG-002.csv) | Checkout button active with empty cart | Medium | High | Open |
| [BUG-003](./JIRA/BUG-003.csv) | Browser back button bypasses logout | Major | High | Open |
| [BUG-004](./JIRA/BUG-004.csv) | Wrong product images for problem_user | Major | Medium | Open |
| [BUG-005](./JIRA/BUG-005.csv) | Sort preference not persisted on refresh | Minor | Low | Open |
| [BUG-006](./JIRA/BUG-006.csv) | Login error styling not auto-cleared | Minor | Low | Open |
| [BUG-007](./JIRA/BUG-007.csv) | No order confirmation email sent | Minor | Medium | Open |
| [BUG-008](./JIRA/BUG-008.csv) | Add to Cart button casing inconsistency | Minor | Low | Open |
| [BUG-009](./JIRA/BUG-009.csv) | Performance glitch user login delay | Major | High | Open |
| [BUG-010](./JIRA/BUG-010.csv) | Postal code field no input validation | Medium | Medium | Open |

---

## Test Environment

| Parameter | Details |
|---|---|
| **OS** | Windows 11 |
| **Browser** | Google Chrome (Latest) |
| **Application URL** | https://www.saucedemo.com/ |
| **Network** | Stable broadband connection |

---

## Test Users

| Username | Password | Role/Status |
|---|---|---|
| `standard_user` | `secret_sauce` | Standard authenticated user |
| `locked_out_user` | `secret_sauce` | Locked account |
| `problem_user` | `secret_sauce` | User with UI issues |
| `performance_glitch_user` | `secret_sauce` | Slow-loading user |

---

## Screenshots Preview

| Page | Screenshot |
|---|---|
| Login Page | `Screenshots/01_Login_Page.png` |
| Product Listing | `Screenshots/02_Product_Listing_Page.png` |
| Cart | `Screenshots/04_Cart_Page.png` |
| Checkout Complete | `Screenshots/07_Checkout_Complete.png` |
| Error - Locked User | `Screenshots/08_Error_Locked_Out_User.png` |
