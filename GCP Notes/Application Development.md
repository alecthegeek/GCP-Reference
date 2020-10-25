# Application Development

Can use various GCP services to run applictions

- Computational Resources
    1. Compute Engine — VM in the cloud
    2. K8s
    3. App Engine
        1. Standard (limited language runtimes)
        2. Flexible (use whatever language runtime you want)
    4. Cloud Functions

[GCP APIs](Application%20Development/GCP%20APIs.md)

## Data Storage

[Google Course notes on Data Storage Options](https://storage.googleapis.com/cloud-training/gcpdev/1.2/Student/(online)%2003_Data%20Storage%20Options.pdf)

Secure data connections

Easier on Gen 2

Storage Options

1. Cloud Storage
    - Unstructured blob
    - Unique ID (URI)
2. Cloud Datastore
    - NoSQL
    - Some structure Key-Value store
    - Reliability and performance
    - Do not use for analytics
3. Cloud Firestore
    - Real Time FB
        - No SQL
        - More structured,  hierarchical
    - Cloud Storage for Firestore
4. Cloud Bigtable
    - No SQL
    - Highly scalable
    - Sparse
    - Use for analytics
    - Supports Hbase API
5. Cloud SQL
    - standard SQL using MySQL or PostgresQL
    - Fully managed
        - Replication
        - Failover
        - Backups
    - 2nd Gen version does not require whitelisting because of proxy
6. Spanner
    - SQL
    - Very scalable
    - Very redundant multi regional
    - Careful
        - Don't use incementing keys
7. BigQuery

    Large scale data warehouse for analytics

8. Cloud Filestore

    For applications that require a filesystem interface and a shared filesystem for data. Filestore gives users a simple, native experience for standing up managed Network Attached Storage (NAS) with their Google Compute Engine and Kubernetes Engine instances

# Pub/Sub

[Using Google Cloud Pub/Sub to Integrate Components of Your Application](https://storage.googleapis.com/cloud-training/gcpdev/1.2/Student/(online)%2008_Using%20Pub_Sub%20to%20integrate%20components%20of%20your%20application.pdf)

# APIs and Google Cloud Endpoints

[Managing APIs with Google Cloud Endpoints](https://storage.googleapis.com/cloud-training/gcpdev/1.2/Student/(online)%2011_Managing%20APIs%20with%20Cloud%20Endpoints.pdf)

# Appliction Buid, Container Registry and Deployment

[GCP Build, Registry & Deployment](https://storage.googleapis.com/cloud-training/gcpdev/1.2/Student/(online)%2012_Deploying%20Applications.pdf)

## Deployment Manager

c.f. Ansible, cheif,...

Infra as code ==> parameterised templates. 

Templates can be dynamic (Python and Jinja)