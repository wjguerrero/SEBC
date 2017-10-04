beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-5-64.us-east-2.compute.internal@WGSEBC.COM
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-5-64.us-east-2.compute.internal@WGSEBC.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES
. . . . . . . . . . . . . . . . . . . .>
0: jdbc:hive2://localhost:10000/default> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20171004200909_9ee66c11-33de-4762-a444-a76cfcb21867): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171004200909_9ee66c11-33de-4762-a444-a76cfcb21867); Time taken: 0.135 seconds
INFO  : Executing command(queryId=hive_20171004200909_9ee66c11-33de-4762-a444-a76cfcb21867): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004200909_9ee66c11-33de-4762-a444-a76cfcb21867); Time taken: 0.446 seconds
INFO  : OK
No rows affected (1.766 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20171004200909_ec378c8e-40ba-4e0f-be7e-ce1f2aafaa95): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171004200909_ec378c8e-40ba-4e0f-be7e-ce1f2aafaa95); Time taken: 0.076 seconds
INFO  : Executing command(queryId=hive_20171004200909_ec378c8e-40ba-4e0f-be7e-ce1f2aafaa95): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004200909_ec378c8e-40ba-4e0f-be7e-ce1f2aafaa95); Time taken: 0.07 seconds
INFO  : OK
No rows affected (0.157 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ROLE sentry_admin TO GROUP wjguerrero;
INFO  : Compiling command(queryId=hive_20171004201212_fe05e14a-46eb-463f-a27a-e2a8881746ea): GRANT ROLE sentry_admin TO GROUP wjguerrero
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171004201212_fe05e14a-46eb-463f-a27a-e2a8881746ea); Time taken: 0.074 seconds
INFO  : Executing command(queryId=hive_20171004201212_fe05e14a-46eb-463f-a27a-e2a8881746ea): GRANT ROLE sentry_admin TO GROUP wjguerrero
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004201212_fe05e14a-46eb-463f-a27a-e2a8881746ea); Time taken: 0.064 seconds
INFO  : OK
No rows affected (0.148 seconds)
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171004201212_efe2a4ed-52cc-41c7-a11a-d6786c6e837d): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171004201212_efe2a4ed-52cc-41c7-a11a-d6786c6e837d); Time taken: 0.2 seconds
INFO  : Executing command(queryId=hive_20171004201212_efe2a4ed-52cc-41c7-a11a-d6786c6e837d): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004201212_efe2a4ed-52cc-41c7-a11a-d6786c6e837d); Time taken: 0.203 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.505 seconds)

