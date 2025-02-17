![image](https://github.com/user-attachments/assets/53e33d42-3395-4ada-a0a5-04ecd1c02457)
### IBM Data replication methods covered in this repo
- Change Data Capture (CDC) (DataMirror heritage product formerly known as Transformation Server)
- Q Replication 
- SQL Replication (formerly known as DataPropagator on mainframe and DPropR for LUW)
- StreamSets  
- DataStage  
[IBM Docs - CDC -- Source and Target](https://www.ibm.com/docs/en/idr/11.4.0?topic=requirements-supported-source-targets)  
[IBM Docs - SQL / Q rep and Event Publishing -- Sources and Target](https://www.ibm.com/docs/en/idr/11.4.0?topic=overviews-supported-sources-targets)  
[IBM Docs - SQL / Q rep / Event Publishing -- Comparison](https://www.ibm.com/docs/en/idr/11.4.0?topic=overviews-comparison-q-replication-sql-replication-event-publishing)  
[IBM Docs - Q rep -- Comparison to HADR](https://www.ibm.com/docs/en/idr/11.4.0?topic=po-comparison-q-replication-high-availability-disaster-recovery-hadr)  

![image](https://github.com/user-attachments/assets/cba800dd-e489-44a6-9fc2-e710020b4d01)
![image](https://github.com/user-attachments/assets/89fe0317-f24f-4e89-b2fe-eb10d36d632a)

|*01-2025            |CDC                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |Q Rep                       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
|Sources             |Db2® on Cloud (formerly dashDB® for Transactions)1 Db2 Warehouse (formerly dashDB Local)2 Db2 Warehouse on Cloud (formerly dashDB for Analytics)2 IBM® Db2 for Linux®, UNIX and Windows (LUW) IBM Db2 for i IBM Db2 for z/OS® IMS Informix® Microsoft SQL Server Microsoft Azure SQL Database3 Microsoft  Azure SQL Database Managed Instance3 MariaDB MySQL Oracle PostgreSQL (including Amazon RDS for PostgreSQL, Amazon Aurora PostgreSQL, Azure Database for PostgreSQL) Sybase VSAM                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |Db2 (Except iSeries) Oracle |
|Targets             |Apache Hadoop Apache Kafka (known compatible commercial distributions include Amazon MSK, Confluent Platform, Cloudera Distribution of Apache Kafka, Hortonworks Data Platform, IBM BigInsights®, IBM Event Streams) Amazon Redshift CDC Replication Engine for Event Server CDC Replication Engine for FlexRep CockroachDB Db2 on Cloud (formerly dashDB for Transactions)1 Db2 Warehouse (formerly dashDB Local) Db2 Warehouse on Cloud (formerly dashDB for Analytics) EDB Postgres Advanced Server Google BigQuery IBM Cloudant® IBM Db2 for Linux, UNIX and Windows (LUW) IBM Db2 for i IBM Db2 for z/OS IBM InfoSphere® DataStage® IBM Integrated Analytics System IBM MQ for z/OS (using Classic CDC for z/OS) IBM Performance Server (IPS) Informix Microsoft Azure SQL Database Microsoft Azure SQL Database Managed Instance Microsoft SQL Server MySQL Netezza® Netezza Performance Server (NPS®) Oracle (includes Oracle RDS as a target) PostgreSQL (including Amazon RDS for PostgreSQL, Amazon Aurora PostgreSQL, Azure Database for PostgreSQL) SingleStoreDB Snowflake Sybase Teradata YugabyteDB|Db2 (Except iSeries) Oracle |
|Capture             |*Log based                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |Log based                   |
|Transport           |TCP/IP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |MQ Series                   |
|Throughput**        |10K+tps                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |50K+tps                     |
|Latency             |sub-second                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |sub-second                  |
|Unique Consideration|non-Db2 / CPU                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |High volume                 |

