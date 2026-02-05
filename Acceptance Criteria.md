***Acceptance Criteria***
----

**1**: Successful user registration
Given the user is on Demoblaze
When the user enters valid credentials in Sign up
Then the account should be created.

**2**: Successful login
Given the user has an existing account
When the user enters valid username and password
Then the user should be logged in.

**3**: Add products to cart
Given the user is logged in
When the user adds products to the cart
Then the products appear in the cart.

**4**: Checkout
Given the user has products in the cart
When the user completes the purchase
Then the order is successful.


**5**: Invalid login
Given the user enters invalid credentials
When login is attempted
Then a proper error message is displayed.
