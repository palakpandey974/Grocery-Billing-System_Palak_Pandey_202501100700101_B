Smart Payment Processing System (Python OOP)

Problem Statement:
------------------
Design and implement a Smart Payment Processing System using Object-Oriented Programming (OOP) concepts in Python.
The system should allow users to make payments using different methods such as Credit Card, UPI, PayPal, and Digital Wallet.
Each payment method follows a common interface but implements its own business logic for computing the final payable amount.

Requirements:
-------------
- Abstract base class Payment:
  - Stores the user name.
  - Declares abstract method pay(amount).
  - Contains concrete method generate_receipt().

- Payment Types:
  1. CreditCardPayment:
     - 2% gateway fee + 18% GST on fee.
     - Final amount = original + fee + GST.
  2. UPIPayment:
     - Cashback ₹50 if amount > 1000.
     - Final amount = original - cashback.
  3. PayPalPayment:
     - 3% international fee + ₹20 conversion fee.
     - Final amount = original + fees.
  4. WalletPayment:
     - Maintains wallet balance.
     - Deducts amount if balance sufficient, else fails.

- Function process_payment(payment, amount):
  - Accepts any payment object.
  - Calls pay() method.
  - Demonstrates runtime polymorphism.

Approach:
---------
1. Abstraction: Payment as abstract base class.
2. Inheritance: Specialized payment classes inherit Payment.
3. Polymorphism: process_payment() adapts to different payment types.
4. Encapsulation: User details and transaction logic secured in classes.

Sample Output:
--------------
UPI Payment:
------------
Processing UPI Payment...
No Cashback Applied

------ PAYMENT RECEIPT ------
User Name       : Palak Pandey
Original Amount : ₹500.0
Final Amount    : ₹500.0
------------------------------

Credit Card Payment:
--------------------
Processing Credit Card Payment...
Gateway Fee: ₹10.0
GST on Fee: ₹1.8

------ PAYMENT RECEIPT ------
User Name       : Palak Pandey
Original Amount : ₹500.0
Final Amount    : ₹511.8
------------------------------

PayPal Payment:
---------------
Processing PayPal Payment...
Transaction Fee: ₹15.0
Conversion Fee: ₹20.0

------ PAYMENT RECEIPT ------
User Name       : Palak Pandey
Original Amount : ₹500.0
Final Amount    : ₹535.0
------------------------------

Wallet Payment:
---------------
Processing Wallet Payment...
Transaction Successful! Remaining Balance: ₹1500.0

------ PAYMENT RECEIPT ------
User Name       : Palak Pandey
Original Amount : ₹500.0
Final Amount    : ₹500.0
------------------------------

Key Concepts Demonstrated:
--------------------------
- Abstraction
- Inheritance
- Polymorphism
- Encapsulation

Submission:
-----------
Google Form Link:
https://docs.google.com/forms/d/e/1FAIpQLSdRzOdWF6qk-puLAjvc-1P3rs4K037EmdPsxK0YTi1b8JNwwQ/viewform?usp=sharing&ouid=117626677736717658
