# Bug Report Examples - Demoblaze

## Purpose
This document contains **example bug reports** demonstrating proper bug documentation format and structure. These examples show professional QA bug reporting skills.

---

## 🐛 EXAMPLE BUG #001: Cart Total Not Updated After Item Removal

**Status:** Example (Demonstration)  
**Severity:** Medium  
**Priority:** High  
**Found By:** Maciej Miszewski 
**Date:** January 2026

### Environment
- **Application:** Demoblaze E-commerce
- **URL:** https://www.demoblaze.com
- **Browser:** Chrome 120.0.6099.130
- **OS:** Windows 11 Pro
- **Screen Resolution:** 1920x1080

### Description
When user removes an item from the shopping cart, the total price does not update automatically. User must refresh the page to see correct total.

### Steps to Reproduce
1. Log in to Demoblaze
2. Add "Samsung galaxy s6" ($360) to cart
3. Add "Nokia lumia 1520" ($820) to cart
4. Navigate to Cart page
5. Verify total shows $1180
6. Click "Delete" next to "Samsung galaxy s6"
7. Observe total price

### Expected Result
- Total price should immediately update to $820 (only Nokia remaining)
- No page refresh should be required
- Cart subtotal should recalculate automatically

### Actual Result
- Total price still displays $1180 (sum of both products)
- Deleted product disappears from cart but total remains unchanged
- User must manually refresh page to see correct total

### Impact
- **User Experience:** Confusing for users, may lead to incorrect purchase amounts
- **Business Impact:** Medium - users may lose trust in cart accuracy
- **Workaround:** Refresh page manually

### Suggested Fix
Implement JavaScript event listener to recalculate cart total when item is removed.

### Attachments
- Screenshot_before_delete.png
- Screenshot_after_delete.png
- Console_log_errors.txt

---

## 🐛 EXAMPLE BUG #002: Product Image Not Loading on Mobile

**Status:** Example (Demonstration)  
**Severity:** Low  
**Priority:** Medium  
**Found By:** Maciej Miszewski  
**Date:** January 2026

### Environment
- **Application:** Demoblaze E-commerce
- **URL:** https://www.demoblaze.com
- **Browser:** Chrome Mobile 120.0
- **Device:** iPhone 12 Pro
- **OS:** iOS 16.5
- **Screen Resolution:** 390x844

### Description
Product images fail to load on mobile devices when browsing the Phones category. Desktop version works correctly.

### Steps to Reproduce
1. Open Demoblaze on mobile device (iPhone 12 Pro)
2. Click "Phones" category
3. Observe product listings
4. Check if images are visible

### Expected Result
- All product images should load and display correctly
- Images should be responsive and fit mobile screen
- No broken image icons should appear

### Actual Result
- Product images show broken image icon (📷 ❌)
- Image src path appears incorrect on mobile
- Desktop version displays images correctly

### Impact
- **User Experience:** Users cannot see products, may not purchase
- **Business Impact:** High - affects conversion rate on mobile
- **Workaround:** Use desktop version

### Root Cause (Analysis)
Possible CSS media query issue or incorrect image path for mobile viewport.

### Suggested Fix
Review responsive design CSS and image loading logic for mobile devices.

---

## 🐛 EXAMPLE BUG #003: Login Modal Does Not Close After Successful Login

**Status:** Example (Demonstration)  
**Severity:** Minor  
**Priority:** Low  
**Found By:** Maciej Miszewski 
**Date:** January 2026

### Environment
- **Application:** Demoblaze E-commerce
- **URL:** https://www.demoblaze.com
- **Browser:** Firefox 121.0
- **OS:** macOS Sonoma 14.2

### Description
After successful login, the login modal window sometimes does not close automatically. User must manually close it by clicking the X button or clicking outside the modal.

### Steps to Reproduce
1. Go to Demoblaze homepage
2. Click "Log in" button
3. Enter valid credentials
4. Click "Log in" in modal
5. Observe modal behavior

### Expected Result
- After successful login, modal should close automatically
- User should see "Welcome [username]" immediately
- Page should be ready for interaction

### Actual Result
- Login is successful (verified by "Welcome" message appearing)
- Modal remains open and visible
- User must manually close modal
- **Frequency:** Intermittent (occurs ~30% of the time)

### Impact
- **User Experience:** Minor annoyance, adds extra click
- **Business Impact:** Low - does not block functionality
- **Workaround:** Click X or click outside modal

### Additional Notes
- Issue appears more frequent on Firefox than Chrome
- May be timing issue with modal close event
- Related to successful login alert handling

---

## 📝 Bug Reporting Guidelines

### Severity Levels
- **Critical:** Application crash, data loss, security vulnerability
- **High:** Major functionality broken, no workaround
- **Medium:** Feature not working as expected, workaround available
- **Low:** Minor UI issues, cosmetic problems

### Priority Levels
- **Critical:** Fix immediately
- **High:** Fix in current sprint
- **Medium:** Fix in next sprint
- **Low:** Fix when resources available

### Required Information
1. ✅ Clear, descriptive title
2. ✅ Environment details (browser, OS, version)
3. ✅ Step-by-step reproduction steps
4. ✅ Expected vs Actual results
5. ✅ Screenshots/videos when applicable
6. ✅ Impact assessment
7. ✅ Suggested workaround (if available)

---

**Note:** The bug reports above are examples created for demonstration purposes to showcase professional bug documentation skills. They may not represent actual bugs in the Demoblaze application.
