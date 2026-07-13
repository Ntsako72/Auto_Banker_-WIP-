README. Account Balance Processor

Description

This small Python script is used to process the account balance of a customer. It reads the customers account information, which includes the account number, account type, minimum balance and current balance. Then it calculates the balance after applying a service charge or interest. The account balance processor supports two types of accounts: Savings and Checking.

The Savings account has a fixed 4 percent interest when the balance is sufficient and a $10 service charge when the balance is below the minimum. The Checking account has an interest rate that depends on the balance relative to the minimum balance and a $25 service charge when the balance is below the minimum.

Requirements

- You need to have Python 3.x installed on your computer.

- You do not need to install any libraries.

Files

- script.py is the Python script that contains the code. You can rename it if you want.

Usage

1. Save the code in a file for example script.py.

2. Run the script from a terminal by typing python script.py.

3. Follow the prompts:

Enter the account number, which can be any string.

Enter the account type, which is either s for Savings or 'c' for Checking.

Enter the minimum balance, which is a numeric value.

Enter the current balance, which is also a numeric value.

Rules

- The script checks if the account type is valid. If not it will keep asking until you enter s or 'c'.

- The script tries to convert the current balances to numbers. If it fails it will print an error message and stop.

- If the current balance is less than the balance:

For a Savings account it subtracts a $10 service charge.

For a Checking account it subtracts a $25 service charge.

It prints a message indicating the service charge applied.

- If the current balance is greater than or equal to the balance:

For a Savings account it adds 4 percent interest to the current balance.

For a Checking account the interest rate is:

. 3 Percent if the current balance is less than or equal to the balance plus $5000.

. 5 Percent if the current balance is greater than the minimum balance plus $5000.

It adds the interest to the balance and prints a message indicating the rate applied.

- The script prints an account summary showing the account number, account type, final balance and a message describing the action taken.

Example sessions

Example 1. Savings, balance below minimum:

- Input:

Account number: 12345

Account type: s

Minimum balance: 500

balance: 400

- Result:

Final Balance: $390.00

Message: Service charge of $10 applied for Savings account.

Example 2. Checking, balance meets minimum. Triggers 5 percent:

- Input:

Account number: ABC987

Account type: c

Minimum balance: 1000

Current balance: 7000

- Result:

Interest rate: 5 percent

Final Balance: current balance plus 5 percent of the current balance

Message: 5 percent interest added to Checking account.

Suggestions

- This script is simple. Is not suitable for batch or production use.

- It does not store any data. Log any transactions.

- The error handling can be improved:

Of stopping when the input is invalid it can ask for the input again.

It can check if the account number is in the format.

- You can add tests, command-line arguments or return results instead of printing them to make it easier to integrate with other programs.

- You can use the module to handle currency to avoid precision issues with floating point numbers.
