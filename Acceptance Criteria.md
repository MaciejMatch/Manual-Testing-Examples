# Acceptance Criteria – Demoblaze Demo Store

The following acceptance criteria define the conditions that must be met for core user-facing functionalities of the Demoblaze demo e-commerce store.

---

## AC-01: Successful User Registration

**Given** the user is on the Demoblaze homepage  
**When** the user enters a valid username and password in the "Sign up" form  
**Then** the account is created successfully  
**And** a confirmation message is displayed

---

## AC-02: Successful Login

**Given** the user has an existing account  
**When** the user enters a valid username and password and submits the login form  
**Then** the user is logged in successfully  
**And** the username is displayed in the navigation bar

---

## AC-03: Add Products to Cart

**Given** the user is logged in  
**When** the user adds one or more products to the shopping cart  
**Then** the selected products appear in the cart  
**And** the cart reflects the correct product details

---

## AC-04: Checkout Process

**Given** the user has products in the shopping cart  
**When** the user completes the purchase process  
**Then** the order is placed successfully  
**And** an order confirmation message is displayed

---

## AC-05: Invalid Login Attempt

**Given** the user enters an invalid username or password  
**When** the login attempt is submitted  
**Then** an error message indicating invalid credentials is displayed  
**And** the user is not logged in
