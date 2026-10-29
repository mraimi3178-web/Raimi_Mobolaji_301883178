## Document Model

The NoSQL model is stored in the clients collection in the insurance_portfolio database with each document representing one client, and the client’s details at the top level. The client’s policies are embedded in a policies array, and each policy contains its related payments. I inserted two sample client documents in MongoDB Atlas; the screenshots show the documents and their embedded records.

## Suitability

Each staff member can see a client’s details, policies, and payments together in one view because the policies and payments are embedded in the client’s document. Searching across many clients for policies nearing expiry may be easier with a relational database, where policies are stored as separate rows and can be filtered by end date.
