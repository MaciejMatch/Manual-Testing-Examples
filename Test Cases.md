# Test Cases - Demoblaze E-commerce Store

## Overview
This document contains detailed test cases for the Demoblaze demo e-commerce application.  
Test execution date: January 2026  
Tester: Maciej Miszewski

---

## TC-001: User Registration - Valid Data
**Module:** User Management  
**Priority:** High  
**Type:** Positive  

**Preconditions:** 
- User is on Demoblaze homepage
- Username "QAtest_user001" does not exist in system

**Test Steps:**
1. Click "Sign up" button in navigation bar
2. Enter username: "QAtest_user001"
3. Enter password: "Test@12345"
4. Click "Sign up" button in modal window

**Expected Result:** 
- Alert appears with message: "Sign up successful."
- Modal window closes after clicking OK
- User can now log in with created credentials

**Actual Result:** ✅ Pass  
**Notes:** Registration successful, credentials stored correctly

---

## TC-002: User Registration - Empty Username
**Module:** User Management  
**Priority:** High  
**Type:** Negative  

**Preconditions:** 
- User is on Demoblaze homepage

**Test Steps:**
1. Click "Sign up" button in navigation bar
2. Leave username field empty
3. Enter password: "Test@12345"
4. Click "Sign up" button in modal window

**Expected Result:** 
- Alert appears with message: "Please fill out Username and Password."
- User is not registered
- Modal remains open

**Actual Result:** ✅ Pass  
**Notes:** Proper validation for empty username field

---

## TC-003: User Registration - Empty Password
**Module:** User Management  
**Priority:** High  
**Type:** Negative  

**Preconditions:** 
- User is on Demoblaze homepage

**Test Steps:**
1. Click "Sign up" button in navigation bar
2. Enter username: "QAtest_user002"
3. Leave password field empty
4. Click "Sign up" button in modal window

**Expected Result:** 
- Alert appears with message: "Please fill out Username and Password."
- User is not registered

**Actual Result:** ✅ Pass  
**Notes:** Proper validation for empty password field

---

## TC-004: User Registration - Duplicate Username
**Module:** User Management  
**Priority:** Medium  
**Type:** Negative  

**Preconditions:** 
- User "QAtest_user001" already exists in system

**Test Steps:**
1. Click "Sign up" button
2. Enter username: "QAtest_user001"
3. Enter password: "AnotherPassword123"
4. Click "Sign up" button

**Expected Result:** 
- Alert appears with message: "This user already exist."
- User is not registered again

**Actual Result:** ✅ Pass  
**Notes:** System correctly prevents duplicate usernames

---

## TC-005: User Login - Valid Credentials
**Module:** User Management  
**Priority:** High  
**Type:** Positive  

**Preconditions:** 
- User "QAtest_user001" exists with password "Test@12345"

**Test Steps:**
1. Click "Log in" button in navigation bar
2. Enter username: "QAtest_user001"
3. Enter password: "Test@12345"
4. Click "Log in" button in modal window

**Expected Result:** 
- User is successfully logged in
- "Welcome QAtest_user001" appears in navigation bar
- "Log in" button changes to "Log out"
- Modal window closes

**Actual Result:** ✅ Pass  
**Notes:** Login successful, session established correctly

---

## TC-006: User Login - Invalid Password
**Module:** User Management  
**Priority:** High  
**Type:** Negative  

**Preconditions:** 
- User "QAtest_user001" exists with password "Test@12345"

**Test Steps:**
1. Click "Log in" button
2. Enter username: "QAtest_user001"
3. Enter password: "WrongPassword"
4. Click "Log in" button

**Expected Result:** 
- Alert appears with message: "Wrong password."
- User remains logged out

**Actual Result:** ✅ Pass  
**Notes:** Proper authentication validation

---

## TC-007: User Login - Non-existent Username
**Module:** User Management  
**Priority:** Medium  
**Type:** Negative  

**Preconditions:** 
- User "NonExistentUser999" does not exist

**Test Steps:**
1. Click "Log in" button
2. Enter username: "NonExistentUser999"
3. Enter password: "AnyPassword123"
4. Click "Log in" button

**Expected Result:** 
- Alert appears with message: "User does not exist."
- User remains logged out

**Actual Result:** ✅ Pass  
**Notes:** System correctly identifies non-existent users

---

## TC-008: Add Product to Cart - Single Item
**Module:** Shopping Cart  
**Priority:** High  
**Type:** Positive  

**Preconditions:** 
- User is on Demoblaze homepage
- User is logged in

**Test Steps:**
1. Click on product "Samsung galaxy s6"
2. Click "Add to cart" button
3. Confirm alert "Product added"
4. Click "Cart" in navigation

**Expected Result:** 
- Alert confirms "Product added."
- Product appears in cart with correct name
- Price displays correctly ($360)
- Delete option is available

**Actual Result:** ✅ Pass  
**Notes:** Product successfully added to cart

---

## TC-009: Add Multiple Products to Cart
**Module:** Shopping Cart  
**Priority:** High  
**Type:** Positive  

**Preconditions:** 
- User is logged in
- Cart is empty

**Test Steps:**
1. Go to homepage
2. Click on "Samsung galaxy s6", click "Add to cart", confirm alert
3. Go back to homepage
4. Click on "Nokia lumia 1520", click "Add to cart", confirm alert
5. Navigate to Cart

**Expected Result:** 
- Both products appear in cart
- Samsung galaxy s6: $360
- Nokia lumia 1520: $820
- Total: $1180

**Actual Result:** ✅ Pass  
**Notes:** Multiple items correctly displayed with accurate total

---

## TC-010: Remove Product from Cart
**Module:** Shopping Cart  
**Priority:** High  
**Type:** Positive  

**Preconditions:** 
- User is logged in
- Cart contains "Samsung galaxy s6" ($360)

**Test Steps:**
1. Navigate to Cart
2. Click "Delete" link next to product
3. Observe cart contents

**Expected Result:** 
- Product is removed from cart
- Cart updates immediately
- Total price updates or shows $0 if cart is empty

**Actual Result:** ✅ Pass  
**Notes:** Product successfully removed, cart updated

---

## TC-011: Browse Products by Category - Phones
**Module:** Product Browsing  
**Priority:** Medium  
**Type:** Positive  

**Preconditions:** 
- User is on Demoblaze homepage

**Test Steps:**
1. Click "Phones" in Categories menu
2. Observe displayed products

**Expected Result:** 
- Only phone products are displayed
- Products include: Samsung galaxy s6, Nokia lumia 1520, Nexus 6, etc.
- No laptops or monitors shown

**Actual Result:** ✅ Pass  
**Notes:** Category filtering works correctly

---

## TC-012: Complete Purchase - Place Order
**Module:** Checkout  
**Priority:** High  
**Type:** Positive  

**Preconditions:** 
- User is logged in
- Cart contains product "Samsung galaxy s6" ($360)

**Test Steps:**
1. Navigate to Cart
2. Click "Place Order" button
3. Fill in form:
   - Name: "John Doe"
   - Country: "USA"
   - City: "New York"
   - Credit card: "1234567812345678"
   - Month: "12"
   - Year: "2026"
4. Click "Purchase" button

**Expected Result:** 
- Success message appears: "Thank you for your purchase!"
- Order details displayed (Amount, Card Number, Name, Date)
- "OK" button closes the modal
- Cart is cleared after purchase

**Actual Result:** ✅ Pass  
**Notes:** Checkout process completed successfully, order confirmation received

---

## TC-013: Place Order - Empty Required Fields
**Module:** Checkout  
**Priority:** High  
**Type:** Negative  

**Preconditions:** 
- User is logged in
- Cart contains at least one product

**Test Steps:**
1. Navigate to Cart
2. Click "Place Order"
3. Leave Name field empty
4. Fill other fields with valid data
5. Click "Purchase"

**Expected Result:** 
- Alert appears: "Please fill out Name and Creditcard."
- Order is not placed
- Modal remains open

**Actual Result:** ✅ Pass  
**Notes:** Proper validation for required fields

---

## TC-014: User Logout
**Module:** User Management  
**Priority:** Medium  
**Type:** Positive  

**Preconditions:** 
- User is logged in as "QAtest_user001"

**Test Steps:**
1. Click "Log out" button in navigation bar
2. Observe navigation bar

**Expected Result:** 
- User is logged out
- "Welcome" message disappears
- "Log out" button changes to "Log in"
- User can no longer access user-specific features

**Actual Result:** ✅ Pass  
**Notes:** Logout successful, session terminated

---

## TC-015: Navigate Between Product Pages
**Module:** Product Browsing  
**Priority:** Low  
**Type:** Positive  

**Preconditions:** 
- User is on Demoblaze homepage

**Test Steps:**
1. Observe "Previous" and "Next" buttons below products
2. Click "Next" button
3. Observe displayed products
4. Click "Previous" button

**Expected Result:** 
- "Next" displays next set of products
- "Previous" returns to previous set
- Pagination works smoothly
- Page does not reload completely

**Actual Result:** ✅ Pass  
**Notes:** Pagination working correctly

---

## Test Execution Summary

| Status | Count | Percentage |
|--------|-------|------------|
| ✅ Pass | 15 | 100% |
| ❌ Fail | 0 | 0% |
| 🔄 Blocked | 0 | 0% |
| **Total** | **15** | **100%** |

**Test Coverage:**
- User Registration: 4 test cases
- User Login/Logout: 4 test cases
- Shopping Cart: 3 test cases
- Product Browsing: 2 test cases
- Checkout: 2 test cases

**Conclusion:** All critical user flows tested and passed successfully. Application is ready for use.
