# 📋 Test Plan — SauceDemo E-Commerce Manual Testing

**Document Version:** 1.0  
**Prepared By:** [Your Name]  
**Date:** July 2026  
**Application:** SauceDemo (https://www.saucedemo.com/)  
**Document Status:** Final  

---

## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Objectives](#2-objectives)
3. [Scope](#3-scope)
4. [Features to Test](#4-features-to-test)
5. [Features Not to Test](#5-features-not-to-test)
6. [Test Environment](#6-test-environment)
7. [Browser Compatibility](#7-browser-compatibility)
8. [Test Strategy](#8-test-strategy)
9. [Entry Criteria](#9-entry-criteria)
10. [Exit Criteria](#10-exit-criteria)
11. [Risks & Assumptions](#11-risks--assumptions)

---

## 1. Project Overview

**SauceDemo** is a demo e-commerce web application hosted at [https://www.saucedemo.com/](https://www.saucedemo.com/) developed by Sauce Labs for the purpose of training and practice in software testing. It simulates a real-world online shopping experience, including user authentication, product listing, shopping cart management, and multi-step checkout.

This test plan defines the scope, strategy, and approach for performing **manual functional testing** on the SauceDemo application. The goal is to verify that all key e-commerce workflows function as expected and to document any deviations from expected behavior.

| Field | Details |
|---|---|
| **Project Name** | SauceDemo Manual Testing Portfolio |
| **Application Under Test** | SauceDemo |
| **Application URL** | https://www.saucedemo.com/ |
| **Testing Type** | Manual Functional Testing |
| **Project Start Date** | July 1, 2026 |
| **Project End Date** | July 7, 2026 |
| **Prepared By** | [Your Name] |
| **Reviewed By** | [Reviewer Name] |

---

## 2. Objectives

The primary objectives of this testing effort are:

1. **Verify functional correctness** of all major features including Login, Product Listing, Cart, Checkout, and Navigation.
2. **Validate input field validations** and error messages for negative test scenarios.
3. **Ensure UI consistency** and usability across all pages.
4. **Identify and document defects** using a structured bug reporting format.
5. **Assess browser compatibility** across Chrome and Firefox.
6. **Trace all test cases to requirements** using the Requirement Traceability Matrix (RTM).
7. **Produce a test summary report** documenting overall test execution results.

---

## 3. Scope

### In Scope
- Login / Authentication module
- Product listing and sorting
- Product detail page
- Shopping cart (add/remove items, badge count)
- Checkout flow (Step 1: Information, Step 2: Overview, Step 3: Confirmation)
- Navigation (menu, logout, browser back button)
- UI and usability validation (layout, error messages, button states)

### Out of Scope
- Performance / Load testing
- Security / Penetration testing
- API-level testing
- Mobile application testing (native apps)
- Payment gateway integration (SauceDemo uses a mock payment)
- Database-level validation
- Cross-browser testing beyond Chrome and Firefox

---

## 4. Features to Test

| # | Feature | Priority |
|---|---|---|
| 1 | User Login with valid credentials | High |
| 2 | User Login with invalid credentials | High |
| 3 | User Login with empty fields | High |
| 4 | Locked out user login attempt | High |
| 5 | Product listing page — all products displayed | High |
| 6 | Product details — name, price, description, image | Medium |
| 7 | Product sorting — by name (A-Z, Z-A) | Medium |
| 8 | Product sorting — by price (low to high, high to low) | Medium |
| 9 | Add single product to cart | High |
| 10 | Add multiple products to cart | High |
| 11 | Remove product from cart | High |
| 12 | Cart badge count updates | Medium |
| 13 | Checkout — enter valid information | High |
| 14 | Checkout — validation with missing fields | High |
| 15 | Checkout — order summary and price calculation | High |
| 16 | Order completion and confirmation page | High |
| 17 | Logout via sidebar menu | Medium |
| 18 | Navigation menu options | Low |
| 19 | Browser back button behavior | Low |
| 20 | Responsive layout verification | Low |
| 21 | Error message styling | Low |
| 22 | Button alignment and UI consistency | Low |

---

## 5. Features Not to Test

| # | Feature | Reason |
|---|---|---|
| 1 | Real payment processing | SauceDemo uses mock payment; no real transactions |
| 2 | Email notifications | Not implemented in demo app |
| 3 | Account registration | Only pre-defined users exist |
| 4 | Password reset | Not available in demo app |
| 5 | Admin dashboard | Not exposed in demo app |
| 6 | Mobile native apps | Web-only testing scope |
| 7 | Performance under load | Out of scope for manual testing |
| 8 | API endpoints | Covered separately in API testing portfolio |
| 9 | Internationalization (i18n) | English only |

---

## 6. Test Environment

| Parameter | Details |
|---|---|
| **Operating System** | Windows 11 (64-bit) |
| **Primary Browser** | Google Chrome — Latest Stable Version |
| **Secondary Browser** | Mozilla Firefox — Latest Stable Version |
| **Screen Resolution** | 1920 x 1080 |
| **Network** | Stable broadband internet connection |
| **Application URL** | https://www.saucedemo.com/ |
| **Test Execution Tool** | Manual (no automation) |
| **Bug Tracking** | GitHub Issues / Bug Reports document |
| **Test Data** | Refer to Test Data document |

### Test Users
| Username | Password | Expected Behavior |
|---|---|---|
| `standard_user` | `secret_sauce` | Full access — all features work normally |
| `locked_out_user` | `secret_sauce` | Login blocked — error message displayed |
| `problem_user` | `secret_sauce` | Some UI elements may behave incorrectly |
| `performance_glitch_user` | `secret_sauce` | Slow load times simulated |

---

## 7. Browser Compatibility

| Browser | Version | Priority | Test Execution |
|---|---|---|---|
| Google Chrome | Latest | High | Primary |
| Mozilla Firefox | Latest | High | Secondary |
| Microsoft Edge | Latest | Medium | Spot check |
| Safari (Mac) | Latest | Low | Not tested (Windows environment) |
| Internet Explorer | Any | None | Not supported |

---

## 8. Test Strategy

### 8.1 Testing Approach

Testing will follow a **black-box, manual, functional** approach. Test cases are designed based on:
- **Equivalence Partitioning** — valid and invalid input classes
- **Boundary Value Analysis** — edge cases at field limits
- **Decision Table Testing** — for multiple input combinations (e.g., checkout fields)
- **Error Guessing** — commonly known failure scenarios

### 8.2 Test Levels

| Level | Description |
|---|---|
| **Smoke Testing** | Verify critical path: Login → Product → Cart → Checkout → Complete |
| **Functional Testing** | Test each module against expected behavior |
| **Regression Testing** | Re-test fixed defects and related features |
| **UI Testing** | Verify layout, error messages, and visual elements |

### 8.3 Test Execution Process

1. Set up the test environment and verify access to SauceDemo
2. Execute **Smoke Tests** to confirm the application is stable
3. Execute test cases module by module in the order defined in the Test Cases document
4. Log results (Pass/Fail/Blocked) in the Test Cases document
5. Raise bugs for any failures using the Bug Report format
6. Re-test bugs after reporting (if applicable in a demo context)
7. Update the RTM and produce the Test Summary Report

### 8.4 Defect Management

| Severity | Description | Example |
|---|---|---|
| **Critical** | Application crashes or core feature completely broken | Cannot login at all |
| **Major** | Feature significantly broken, no workaround | Checkout button not working |
| **Medium** | Feature partially broken, workaround available | Sort not working for one option |
| **Minor** | Cosmetic or UI issue | Button misalignment |

| Priority | Description |
|---|---|
| **High** | Must be fixed immediately |
| **Medium** | Should be fixed in current release |
| **Low** | Can be deferred to future release |

---

## 9. Entry Criteria

Testing will begin only when the following conditions are met:

- [ ] The SauceDemo application is accessible at https://www.saucedemo.com/
- [ ] Test environment (browser, OS) is set up and functional
- [ ] All test credentials are verified and working
- [ ] Test Plan has been reviewed and approved
- [ ] Test Cases document is complete and reviewed
- [ ] Test Data is prepared

---

## 10. Exit Criteria

Testing will be considered complete when:

- [ ] All planned test cases have been executed (minimum 95%)
- [ ] All **Critical** and **High severity** defects are reported
- [ ] Test execution results are documented in Test Cases sheet
- [ ] Test Summary Report is completed
- [ ] RTM is fully populated
- [ ] Screenshots of test evidence are captured

---

## 11. Risks & Assumptions

### Risks

| Risk ID | Risk | Probability | Impact | Mitigation |
|---|---|---|---|---|
| R001 | SauceDemo application may be temporarily unavailable | Low | High | Test during off-peak hours; retry after 30 minutes |
| R002 | Application may change without notice (it's a demo app) | Medium | Medium | Document the version/date of testing |
| R003 | Browser updates may affect behavior | Low | Low | Pin browser version or note version used |
| R004 | Limited test users (all credentials are hardcoded) | N/A | Low | Use all available test accounts |
| R005 | No real backend validation (demo app) | N/A | Medium | Note any limitations in Test Summary |

### Assumptions

1. SauceDemo is a **demo/practice application** — bugs found may be intentional for training purposes.
2. All reported bugs are either **observed** or clearly labeled as **"Practice Bug Report"**.
3. The application behavior is consistent with standard e-commerce workflows.
4. Test cases are designed based on visible UI and standard functional expectations.
5. No changes to the application will be made during the testing period.
6. The tester has a stable internet connection throughout testing.

---

*Document End — Test Plan v1.0*
