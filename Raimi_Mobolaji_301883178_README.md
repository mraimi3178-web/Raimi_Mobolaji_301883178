# Raimi_Mobolaji_301883178
MIT 8103 Advanced Database Systems CA - September 2026 Cohort
# MIT 8103 Advanced Database Systems Portfolio

Name: Raimi Mobolaji

Student ID: 301883178

## Case study

Impact Insurance Brokers Limited (fictional company) is an insurance brokerage company that connects individuals or organizations seeking insurance cover for their various assets with insurers willing to carry such liabilities. A major part of their daily operations involve the need to maintain accurate client details, policies, and payments. Respond to inquiries and client-history requests, match policies to payments, and identify policies nearing expiry for renewal follow-up. This focus of this case study will be spooling from the database, policies nearing expiry for adequate follow for renewal. This case study was also used throughout the five portfolio activities, as required by the assessment brief.

## Users

Members of staff of Impact Insurance Brokers Limited will use the database to maintain client's details, policies and payment. As well as filter out the end dates of all policies to ascertain which ones are nearing expiry for necessary renewal follow-up.

## Main Operations

1. Add a new client and record or update their contact details.
2. Create a policy for an existing client, including its insurer, cover type, dates and annual premium.
3. Record a payment against the correct policy.
4. Find a client and view their details, policies and payment history.
5. List a client’s policies and payments when responding to an enquiry.
6. Find policies that are nearing expiry so staff can follow up with clients about renewal.
7. Review payments for a policy and compare them with its premium.
8. Update a client’s details or correct policy information when it changes.

## Business Rules

1. Each client must have a unique Client ID and a client name. Phone number, email, and address may be blank.
2. A client may have no policies or several policies. Each policy belongs to exactly one client.
3. Each policy must have a unique Policy ID and include its client ID, cover type, insurer, start date, end date, and annual premium.
4. A policy’s end date must be later than its start date.
5. Each policy may have no payments or several payments. Each payment belongs to exactly one policy.
6. Each payment must have a unique Payment ID and include its policy ID, payment date, amount, and payment method.
7. Annual premiums and payment amounts must be greater than zero.
8. A policy’s Client ID must match an existing client, and a payment’s Policy ID must match an existing policy.

## Portfolio folders

- portfolio-1-database-design: design, schema and normalisation.
- portfolio-2-query-optimisation: queries, plans and performance analysis.
- portfolio-3-transactions-concurrency: commit, rollback and concurrency.
- portfolio-4-nosql: NoSQL model, implementation and suitability.
- portfolio-5-distributed-cloud: distributed or cloud database exercise.
