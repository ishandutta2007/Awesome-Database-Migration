# Awesome-Database-Migration

## Top Database Migration Platforms Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Database Migration, Change Data Capture & Cross-Engine Replication*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Database Migration**. These tools help organizations migrate databases between engines, versions, and cloud environments—while minimizing downtime and ensuring data integrity.



**Examples** include AWS DMS, Fivetran HVR, Qlik Replicate, Striim, Azure DMS, Google DMS, DBConvert, Ispirer Toolkit, Flyway, and Bytebase (the category leaders).



**Open-source emphasis**: Database migration has a **mature and production-proven open-source ecosystem**. **Ape-DTS** (Rust) provides ultra-fast replication between MySQL, PostgreSQL, Redis, MongoDB, Kafka, and ClickHouse . **Debezium** powers CDC across five databases . **Flyway** and **Liquibase** dominate schema migration . **ReplicaDB** handles bulk data transfer between relational and non-relational databases . **GH-OST** enables online schema changes for MySQL at GitHub scale (12,373 stars) . This section documents these production-grade solutions.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents



- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[AWS Database Migration Service (DMS)](https://aws.amazon.com/dms/)**  

  AWS-native database migration service. Supports homogeneous and heterogeneous migrations with continuous replication (CDC). Integrates with Schema Conversion Tool (SCT) for Oracle/SQL Server to PostgreSQL/Aurora migrations.



- **[Fivetran HVR](https://www.fivetran.com/)**  

  Enterprise CDC and replication platform (HVR acquired by Fivetran). Provides real-time replication across on-premises and cloud databases with low-impact log-based capture.



- **[Qlik Replicate](https://www.qlik.com/)**  

  Enterprise database replication (formerly Attunity). Supports 30+ databases with real-time CDC, detailed transaction logging, and hybrid deployment.



- **[Striim](https://www.striim.com/)**  

  Real-time data integration and streaming platform. Provides sub-60-second CDC latency with enterprise governance.



- **[Azure Database Migration Service](https://azure.microsoft.com/)**  

  Azure-native migration service. Supports SQL Server, MySQL, PostgreSQL, and MongoDB migrations with minimal downtime.



- **[Google Database Migration Service](https://cloud.google.com/)**  

  Google Cloud migration service for MySQL, PostgreSQL, and SQL Server to Cloud SQL and AlloyDB.



- **[DBConvert](https://dbconvert.com/)**  

  Commercial database migration and synchronization tool. Supports 40+ database types with GUI-based migration workflows.



- **[Ispirer Toolkit](https://www.ispirer.com/)**  

  Database and application migration toolkit. Specializes in legacy database migrations (Oracle, Sybase, DB2) to modern platforms.



- **[Flyway Enterprise](https://www.red-gate.com/)**  

  Commercial edition of Flyway. Adds undo scripts, drift detection, and object-level versioning for schema migrations .



- **[Bytebase Cloud](https://bytebase.com/)**  

  Managed database CI/CD platform with migration workflows, SQL review, and approval gates.



## Open-Source GitHub Projects



### Cross-Engine Migration & Replication



- **[Ape-DTS](https://github.com/apecloud/ape-dts)**  

  **Ultra-fast data transfer suite written in Rust.** Provides replication between **MySQL, PostgreSQL, Redis, MongoDB, Kafka, and ClickHouse** . **584 stars, 96 forks**. Ideal for **disaster recovery and migration scenarios** . Part of the ApeCloud ecosystem alongside KubeBlocks (3,041 stars) . **Open source**.



- **[ReplicaDB](https://github.com/osalvador/ReplicaDB)**  

  **Open-source tool for efficiently transferring bulk data between relational and non-relational databases.** Designed for database replication and migration at scale . **Open source**.



- **[Debezium](https://github.com/debezium/debezium)**  

  **The de facto standard for log-based change data capture.** Captures changes from **PostgreSQL, MySQL, SQL Server, Oracle, and MongoDB** . **Built-in Outbox Event Router** for event-driven architectures. **Apache-2.0**. Widely used in production at scale.



- **[rsync-ai](https://github.com/rsync-ai/rsync)**  

  **Self-hosted, source-available AI data platform for batch pipelines, CDC, scheduled models, and lineage.** **21 connectors** including PostgreSQL, MySQL, SQL Server, Oracle, ClickHouse, MongoDB, Snowflake, BigQuery, S3, and Stripe . **Debezium-backed CDC on five databases**. Natural language pipeline creation ("sync MySQL orders to S3 every hour") with human-in-the-loop gates. **Temporal workflow durability**. **Source-available**.



### Schema Migration Frameworks



- **[Flyway](https://github.com/flyway/flyway)**  

  **Developer-friendly SQL-first migration tool.** **Apache-2.0 licensed** (Community edition). Uses versioned SQL scripts applied in order, tracked by a schema history table . **50+ database support**. Spring Boot integration. **Best for**: Developer-first teams wanting minimal setup.



- **[Liquibase](https://github.com/liquibase/liquibase)**  

  **Cross-database abstraction migration tool.** **Apache-2.0 licensed**. Uses changelog/changeset concept in SQL, XML, YAML, or JSON . **60+ database support**. Standardized rollbacks. **Best for**: Enterprise and regulated environments needing governance.



- **[Evolve](https://github.com/lecaillon/Evolve)**  

  **Database migration tool for .NET and .NET Core, inspired by Flyway.** Uses plain SQL scripts. Cross-platform with .NET library, .NET tool, and standalone CLI . **Best for**: .NET teams wanting Flyway-like simplicity.



- **[Herd](https://pkg.go.dev/github.com/mattdowdell/sandbox@v0.5.36/pkg/herd)**  

  **Go library for applying migrations to PostgreSQL.** Migrations implement `herd.Migration` interface with Version and Migrate methods. **Only up-migrations supported**—problematic migrations corrected by additional migrations . **Best for**: Go applications needing lightweight embedded migrations.



### Online Schema Changes



- **[GH-OST](https://github.com/github/gh-ost)**  

  **GitHub's Online Schema-migration Tool for MySQL.** **12,373 stars, 1,256 forks** . **Triggerless** online schema changes—does not use triggers like pt-online-schema-change. Allows pausing, resuming, and dynamic reconfiguration. **Best for**: MySQL schema changes with zero downtime.



- **[pg_chameleon](https://github.com/the4thdoctor/pg_chameleon)**  

  **MySQL to PostgreSQL replica system.** **380 stars, 83 forks** . Provides logical replication from MySQL to PostgreSQL. **Best for**: MySQL-to-PostgreSQL migrations.



- **[pglogical](https://github.com/2ndQuadrant/pglogical)**  

  **Logical replication extension for PostgreSQL.** Provides much faster replication than Slony, Bucardo, or Londiste, as well as cross-version upgrades . **Best for**: PostgreSQL-native logical replication.



### Additional Strong Open-Source Options



- **Cross-Engine Migration**: **Ape-DTS** (Rust, MySQL/PostgreSQL/Redis/MongoDB/Kafka/ClickHouse) , **ReplicaDB** (relational + non-relational) , **rsync-ai** (21 connectors, CDC) .

- **CDC**: **Debezium** (PostgreSQL, MySQL, SQL Server, Oracle, MongoDB) .

- **Schema Migration**: **Flyway** (SQL-first, 50+ DBs) , **Liquibase** (cross-DB abstraction) , **Evolve** (.NET, Flyway-inspired) , **Herd** (Go, PostgreSQL) .

- **Online Schema Changes**: **GH-OST** (MySQL, triggerless, 12k+ stars) , **pg_chameleon** (MySQL→PostgreSQL) , **pglogical** (PostgreSQL logical replication) .



**Frameworks for building custom systems**: Combine **Ape-DTS** for ultra-fast cross-engine replication, **Debezium** for log-based CDC, **Flyway** or **Liquibase** for schema migration, **GH-OST** for MySQL online schema changes, and **ReplicaDB** for bulk data transfer. Add **Kafka** for event streaming, **PostgreSQL** for metadata persistence, and **Docker** for deployment.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Database migration platforms handle sensitive production data; ensure proper access controls, encryption, and compliance with data protection regulations.

- **Open-source reality**: The open-source ecosystem for database migration is **mature and production-proven**. **Ape-DTS** provides ultra-fast cross-engine replication in Rust . **Debezium** is the de facto CDC standard . **Flyway** and **Liquibase** dominate schema migration with 50+ and 60+ database support respectively . **GH-OST** enables triggerless online schema changes for MySQL at GitHub scale . **ReplicaDB** handles bulk data transfer between relational and non-relational databases . However, **commercial platforms** (AWS DMS, Fivetran HVR, Qlik Replicate, Striim) provide **managed infrastructure, enterprise-grade monitoring, schema conversion tools, and dedicated support** that open-source alternatives require significant operational investment to match. The open-source path is **genuinely viable** for organizations with strong data engineering capacity.



---



**Made for database engineers, data platform teams, DevOps professionals, and migration specialists.**

Let's make database migration more open, transparent, and reliable.
