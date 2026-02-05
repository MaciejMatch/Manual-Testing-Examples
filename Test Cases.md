# Test Cases – Demoblaze Demo Store

This document contains manual test cases prepared for the Demoblaze demo e-commerce application (https://www.demoblaze.com).  
The test cases focus on core user-facing functionality and represent typical manual testing practices.

---

## TC-01 – Successful Registration

**Preconditions:**
- User does not have an existing account

**Steps:**
1. Open the Demoblaze homepage
2. Click the "Sign up" button
3. Enter a valid username and password
4. Click "Sign up" to submit the form

**Expected Result:**
- The account is created successfully
- A confirmation message is displayed

---

## TC-02 – Successful Login

**Preconditions:**
- User account exists

**Steps:**
1. Open the login dialog
2. Enter a valid username and password
3. Click the "Log in" button

**Expected Result:**
- User is logged in successfully
- Username is displayed in the navigation bar

---

## TC-03 – Browse and Select Product

**Preconditions:**
- User is logged in

**Steps:**
1. Navigate to a product category
2. Click on a selected product

**Expected Result:**
- Product details page is displayed
- Product name, price, and description are visible

---

## TC-04 – Add Product to Cart

**Preconditions:**
- User is logged in
- Product details page is open

**Steps:**
1. Click the "Add to cart" button

**Expected Result:**
- Confirmation message is displayed
- Product is added to the shopping cart

---

## TC-05 – View Shopping Cart

**Preconditions:**
- Product has been added to the cart

**Steps:**
1. Open the shopping cart page

**Expected Result:**
- Correct product name, quantity, and price are displayed

---

## TC-06 – Complete Checkout

**Preconditions:**
- User is logged in
- At least one product is present in the cart

**Steps:**
1. Open the shopping cart
2. Click the "Place Order" button
3. Fill in required order details
4. Confirm the purchase

**Expected Result:**
- Order confirmation message is displayed
- Order is completed successfully

---

## TC-07 – Invalid Login Attempt

**Preconditions:**
- User account exists

**Steps:**
1. Open the login dialog
2. Enter an invalid username or password
3. Click the "Log in" button

**Expected Result:**
- Error message indicating invalid credentials is displayed
- User is not logged in
