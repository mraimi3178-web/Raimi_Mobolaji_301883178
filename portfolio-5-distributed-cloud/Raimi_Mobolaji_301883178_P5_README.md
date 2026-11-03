## Cloud Deployment

The insurance_portfolio database was deployed on MongoDB Atlas using the ClusterMobolaji Free-tier cluster. The Atlas overview showed that the cluster is hosted on AWS in one region. This provides evidence of the cloud deployment. Replication and sharding are discussed in this portfolio as database conceptsonly. I did not separately configure them for this project.

## Replication and Availability

Replication keeps copies of the same data on multiple database servers. In an insurance brokerage, this can support business continuity: if the active database server becomes unavailable, another server may take over, allowing staff to continue accessing and processing client records. However, this takeover depends on the replication setup.

## Sharding

Sharding divides a large dataset across multiple servers, with each server storing a portion of the data. An insurance brokerage could, for example, distribute clients by client ID so each server handles a portion of the client records and related activity. This can help the system scale as the number of clients and transactions grows, although the distribution must be designed carefully so queries can find the needed data.

## Consistency

Consistency is the database’s ability to maintain accurate records and apply updates according to its rules. In the brokerage, this matters so staff can rely on correct client, policy, and payment details when servicing clients. With replicated data, the system’s consistency settings determine how updates are reflected across copies.
