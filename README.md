# BankingSystem

Implementation of bank accounts supporting opening/closing, withdrawals, and deposits of money. There may be many deposits and withdrawals occurring in parallel so concurrently have to be allowed.

## Opening an account

An account can be opened. On opening, its initial balance should not be negative. If a negative balance is given to the Open function, nil must be returned, otherwise the newly created account must be returned.

## Closing an account

An account can be closed. When closing an account, the Close method must return the balance the account has and a boolean true indicating the account was closed successfully. Closing an account does not succeed if the account is already closed. When an account is closed, its balance must be set to 0.

## Getting the account balance

The Balance method allows a user to check the current balance of an account. It must return the balance of the account and a boolean indicating if the operation succeeded. Checking the balance only doesn't succeed if the account is closed.

## Deposits / Withrawals

Deposits and withdrawals are both handled by the Deposit method. If the argument given to the method is a positive amount, then that amount of money must be deposited in the account. If the amount given is negative, that amount of money must be withdrawn from the account. If the account is closed, its balance must not be modified.

Deposit returns the new balance of the account and a boolean that indicates if the operation succeeded. Deposit must fail if the account is closed or if there is not enough money to withdraw from the account.

## Testing

The tests will execute some operations concurrently.
