# Amazon Aurora PostgreSQL Fast Failover for Amazon RDS Aurora PostgreSQL Global Database

#Cross-Region Failover or SwitchOver

A Lambda DBMonitor function continually monitor the primary region (every 10 seconds) from the secondary region, and enacts failover if it observes 30 seconds of consecutive failures. Lambda DBMonitor function can be configured to run more or less frequently.

![Screenshot 2024-07-09 at 3 58 15 PM](https://github.com/justinaws/amazon-aurora-global-database-endpoint-management/assets/147440980/60a409fa-7304-4902-98dd-473ce28da62c)

#Deploying This Solution

1. Create a Lambda function in the seconday region using aurora_db_switch_or_fail_over.py 

2.  Configure following parameters for Lambda function
     GLOBAL_APP_DB_PROXY_WRITER_ENDPOINT_REGION
     GLOBAL_APP_DB_CLUSTER_IDENTIFIER
     REGIONAL_APP_DB_CLUSTER_ARN
     
License
This library is licensed under the MIT-0 License. See the LICENSE file.

Note that the Python code depends on, but does not include, the LGPL-3.0 licensed Psycopg PostgreSQL adapter.
