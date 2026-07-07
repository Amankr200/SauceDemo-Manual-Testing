# Test Summary Report — SauceDemo Manual Testing

**Document Version:** 1.0   
**Application:** SauceDemo (https://www.saucedemo.com/)  
**Report Status:** Final  

---

## 1. Executive Summary

This report summarizes the **end-to-end manual testing** performed on the **SauceDemo e-commerce web application**. Testing was conducted to verify the functionality of all major modules including Login, Product Listing, Shopping Cart, Checkout, Navigation, and UI/Usability.

A total of **52 test cases** were executed across **6 functional modules** against **40 identified requirements**. The application demonstrated a high level of functional stability, with the majority of core e-commerce workflows functioning as expected.

---

## 2. Test Execution Overview

| Metric | Value |
|---|---|
| **Application Under Test** | SauceDemo |
| **Application URL** | https://www.saucedemo.com/ |
| **Test Environment** | Windows 11 / Chrome (Latest) |
| **Testing Type** | Manual Functional Testing |

---

## 3. Test Results Summary

### 3.1 Test Scenarios

| Metric | Count |
|---|---|
| **Total Test Scenarios Planned** | 30 |
| **Total Test Scenarios Executed** | 30 |
| **Pass** | 29 |
| **Fail** | 1 |
| **Blocked** | 0 |
| **Not Run** | 0 |

### 3.2 Test Cases

| Metric | Count |
|---|---|
| **Total Test Cases Planned** | 52 |
| **Total Test Cases Executed** | 52 |
| **Pass** | 51 |
| **Fail** | 1 |
| **Blocked** | 0 |
| **Not Run** | 0 |

### 3.3 Test Case Status by Module

| Module | Total | Pass | Fail | Blocked | Pass % |
|---|---|---|---|---|---|
| Login | 9 | 9 | 0 | 0 | 100% |
| Product Page | 8 | 8 | 0 | 0 | 100% |
| Cart | 7 | 7 | 0 | 0 | 100% |
| Checkout | 12 | 12 | 0 | 0 | 100% |
| Navigation | 5 | 4 | 1 | 0 | 80% |
| UI & Usability | 9 | 9 | 0 | 0 | 100% |
| Regression (Cart) | 2 | 2 | 0 | 0 | 100% |
| **Total** | **52** | **51** | **1** | **0** | **98.1%** |

---

## 4. Defects Summary

### 4.1 Bug Count

| Metric | Count |
|---|---|
| **Total Bugs Identified** | 8 |
| **Observed Bugs** | 3 |
| **Practice Bug Reports** | 5 |
| **Critical** | 0 |
| **Major** | 3 |
| **Medium** | 1 |
| **Minor** | 4 |
| **Open** | 8 |
| **Closed / Fixed** | 0 |

### 4.2 Bug Details

| Bug ID | Title | Severity | Priority | Type | Status |
|---|---|---|---|---|---|
| BUG-001 | Locked user login verification | Major | High | Observed | Open |
| BUG-002 | Checkout button active with empty cart | Medium | High | Practice | Open |
| BUG-003 | Browser back allows access after logout | Major | High | Observed | Open |
| BUG-004 | Wrong product images for problem_user | Major | Medium | Observed | Open |
| BUG-005 | Sort selection doesn't persist on refresh | Minor | Low | Practice | Open |
| BUG-006 | Error not cleared when user retypes | Minor | Low | Practice | Open |
| BUG-007 | No order confirmation email sent | Minor | Medium | Practice | Open |
| BUG-008 | "Add to cart" casing inconsistency | Minor | Low | Practice | Open |

---

## 5. Requirements Coverage

| Metric | Count |
|---|---|
| **Total Requirements Identified** | 40 |
| **Requirements Covered by Tests** | 40 |
| **Pass** | 39 |
| **Fail** | 1 |
| **Coverage Percentage** | 100% |
| **Requirements Pass Rate** | 97.5% |

---

## 6. Test Completion Metrics

| Metric | Value |
|---|---|
| **Test Case Completion Rate** | 100% (52/52 executed) |
| **Test Case Pass Rate** | 98.1% (51/52 passed) |
| **Requirements Coverage** | 100% (40/40 covered) |
| **Requirements Pass Rate** | 97.5% (39/40 passed) |
| **Overall Test Completion** | **Complete** |

---

## 7. Module-wise Analysis

### 7.1 Login Module —  PASS (100%)
All 9 login test cases passed successfully. The login module correctly:
- Authenticates valid users and redirects to the inventory page
- Rejects invalid credentials with appropriate error messages
- Validates empty fields with specific error messages
- Blocks locked-out users with the correct error
- Masks the password field input
- Allows error messages to be dismissed

### 7.2 Product Page Module — PASS (100%)
All 8 product page test cases passed. The product page correctly:
- Displays all 6 products with complete information (name, image, price, description, button)
- Allows navigation to individual product detail pages
- Supports all 4 sort options (A-Z, Z-A, Low-High, High-Low)

### 7.3 Cart Module — PASS (100%)
All 7 cart test cases passed. The cart correctly:
- Adds products and updates the badge counter
- Supports multiple product additions
- Removes products and decrements the badge
- Persists cart state during page navigation
- Provides working "Continue Shopping" navigation

### 7.4 Checkout Module — PASS (100%)
All 12 checkout test cases passed. The checkout flow correctly:
- Validates all three required fields (First Name, Last Name, Postal Code)
- Displays accurate item total, tax, and grand total
- Shows payment and shipping information
- Completes the order and shows confirmation
- Provides cancel options at both steps

### 7.5 Navigation Module — PARTIAL PASS (80%)
4 of 5 test cases passed. **TC-038 failed:**
- The browser back button after logout allows access to the inventory page
- This is a known session management issue with SauceDemo (demo app limitation)
- In a real production application, this would be a Major security defect
- Documented as BUG-003

### 7.6 UI & Usability Module — PASS (100%)
All 9 UI test cases passed. The UI is consistent with:
- Proper page titles on each page
- Red styling for error messages with dismiss icon
- Correct button state changes (Add to cart ↔ Remove)
- Cart icon visible across all authenticated pages
- Proper alignment of all UI elements

---

## 8. Test Environment Assessment

| Aspect | Observation |
|---|---|
| **Stability** | Application was stable throughout testing; no crashes or timeouts |
| **Performance** | Page loads were fast on standard broadband connection |
| **Browser Compatibility** | Tested on Chrome — all features functioned correctly |
| **Data Accuracy** | Product prices, tax calculation, and totals were all accurate |

---

## 9. Risks & Observations

| # | Observation | Impact |
|---|---|---|
| 1 | SauceDemo is a demo app — some behaviors are intentionally broken (e.g., problem_user) | Low — expected for demo purposes |
| 2 | Session management (back button after logout) is a gap | High — would be critical in real app |
| 3 | No backend data persistence — cart resets on logout | Low — expected for demo |
| 4 | All user credentials and product data are hardcoded | Low — expected for demo |
| 5 | "Practice Bug Reports" are hypothetical and documented for learning | Informational |

---

## 10. Conclusion

The **SauceDemo e-commerce application** demonstrates a functionally stable and well-structured e-commerce workflow. Testing has confirmed that the core user journeys — from Login through Product Selection, Cart Management, and Checkout Completion — work as intended.

**Key Findings:**
- **Login, Product Page, Cart, Checkout, and UI modules** all achieved a **100% pass rate**
- **Navigation module** had one failure related to **session management** after logout (browser back button behavior)
- **8 bugs** were documented — 3 observed directly, 5 as practice reports for portfolio purposes
- **Overall test pass rate: 98.1%** across 52 test cases

**Recommendation:**  
The application is suitable for continued testing practice. The session management gap (BUG-003) should be noted as a real-world security consideration. All critical and high-priority business flows (login, shopping, checkout) are working correctly.

**Test Completion: COMPLETE**

---

