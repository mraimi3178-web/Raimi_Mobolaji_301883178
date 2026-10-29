## Rollback

A Rollback demonstration was carried out by inserting a temporary payment into a transaction and the transaction was rolled back. The payment was checked to ensure it was not saved on the database and it was confirmed that no payment remained in the database.

## Commit
A commit was demonstrated by inserting a payment of ₦75,000 for Policy 280. After the transaction was committed, a check confirmed that the payment remained saved in the database.

## Concurrency Control

Concurrency control was demonstrated using two sessions. The first session locked Policy 280, while the second tried to lock the same row using the NOWAIT option. The second session returned an error immediately instead of waiting, showing how the database handles competing access to a locked row.
