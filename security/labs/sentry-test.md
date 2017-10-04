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
[root@ip-172-31-6-242 centos]# sudo groupadd selector
[root@ip-172-31-6-242 centos]# sudo groupadd inserters
[root@ip-172-31-6-242 centos]# sudo useradd -u 1100 -g selector george
[root@ip-172-31-6-242 centos]# sudo useradd -u 1200 -g inserters ferdinand
[root@ip-172-31-6-242 centos]# kadmin.local: add_principal george
bash: kadmin.local:: command not found
[root@ip-172-31-6-242 centos]# kadmin.local
Authenticating as principal wjguerrero/admin@WGSEBC.COM with password.
kadmin.local:  admin
kadmin.local: Unknown request "admin".  Type "?" for a request list.
kadmin.local:  add_principal george
WARNING: no policy specified for george@WGSEBC.COM; defaulting to no policy
Enter password for principal "george@WGSEBC.COM":
Re-enter password for principal "george@WGSEBC.COM":
Principal "george@WGSEBC.COM" created.
kadmin.local:  add_principal ferdinand
WARNING: no policy specified for ferdinand@WGSEBC.COM; defaulting to no policy
Enter password for principal "ferdinand@WGSEBC.COM":
Re-enter password for principal "ferdinand@WGSEBC.COM":
Principal "ferdinand@WGSEBC.COM" created.
0: jdbc:hive2://localhost:10000/default> CREATE ROLE reads;
INFO  : Compiling command(queryId=hive_20171004202626_7e23f131-4790-42be-826f-6cc3be40aa3d): CREATE ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171004202626_7e23f131-4790-42be-826f-6cc3be40aa3d); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20171004202626_7e23f131-4790-42be-826f-6cc3be40aa3d): CREATE ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004202626_7e23f131-4790-42be-826f-6cc3be40aa3d); Time taken: 0.037 seconds
INFO  : OK
No rows affected (0.154 seconds)
0: jdbc:hive2://localhost:10000/default> CREATE ROLE writes;
INFO  : Compiling command(queryId=hive_20171004202626_82587670-a5f5-4519-877b-dbb16de0dc18): CREATE ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171004202626_82587670-a5f5-4519-877b-dbb16de0dc18); Time taken: 0.123 seconds
INFO  : Executing command(queryId=hive_20171004202626_82587670-a5f5-4519-877b-dbb16de0dc18): CREATE ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004202626_82587670-a5f5-4519-877b-dbb16de0dc18); Time taken: 0.022 seconds
INFO  : OK
No rows affected (0.156 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT SELECT ON DATABASE default TO ROLE reads;
INFO  : Compiling command(queryId=hive_20171004202727_abdbdfec-7db2-452f-8a9b-2d460c4c31dc): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171004202727_abdbdfec-7db2-452f-8a9b-2d460c4c31dc); Time taken: 0.065 seconds
INFO  : Executing command(queryId=hive_20171004202727_abdbdfec-7db2-452f-8a9b-2d460c4c31dc): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004202727_abdbdfec-7db2-452f-8a9b-2d460c4c31dc); Time taken: 0.028 seconds
INFO  : OK
No rows affected (0.105 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ROLE reads TO GROUP selector;
INFO  : Compiling command(queryId=hive_20171004202727_adf11e2d-8dd2-4b36-b38d-821db002fa7c): GRANT ROLE reads TO GROUP selector
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171004202727_adf11e2d-8dd2-4b36-b38d-821db002fa7c); Time taken: 0.051 seconds
INFO  : Executing command(queryId=hive_20171004202727_adf11e2d-8dd2-4b36-b38d-821db002fa7c): GRANT ROLE reads TO GROUP selector
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004202727_adf11e2d-8dd2-4b36-b38d-821db002fa7c); Time taken: 0.025 seconds
INFO  : OK
No rows affected (0.1 seconds)
0: jdbc:hive2://localhost:10000/default> REVOKE ALL ON DATABASE default FROM ROLE writes;
INFO  : Compiling command(queryId=hive_20171004202727_8fcad5a0-6482-47da-976d-475826edbfed): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171004202727_8fcad5a0-6482-47da-976d-475826edbfed); Time taken: 0.059 seconds
INFO  : Executing command(queryId=hive_20171004202727_8fcad5a0-6482-47da-976d-475826edbfed): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004202727_8fcad5a0-6482-47da-976d-475826edbfed); Time taken: 0.075 seconds
INFO  : OK
No rows affected (0.146 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT SELECT ON default.sample_07 TO ROLE writes;
INFO  : Compiling command(queryId=hive_20171004202828_718d0639-03c7-4dd9-9517-2e6ea26d1b79): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171004202828_718d0639-03c7-4dd9-9517-2e6ea26d1b79); Time taken: 0.059 seconds
INFO  : Executing command(queryId=hive_20171004202828_718d0639-03c7-4dd9-9517-2e6ea26d1b79): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004202828_718d0639-03c7-4dd9-9517-2e6ea26d1b79); Time taken: 0.029 seconds
INFO  : OK
No rows affected (0.1 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ROLE writes TO GROUP inserters;
INFO  : Compiling command(queryId=hive_20171004202929_acdb4488-4d79-43cc-8445-a8163d7de46f): GRANT ROLE writes TO GROUP inserters
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171004202929_acdb4488-4d79-43cc-8445-a8163d7de46f); Time taken: 0.056 seconds
INFO  : Executing command(queryId=hive_20171004202929_acdb4488-4d79-43cc-8445-a8163d7de46f): GRANT ROLE writes TO GROUP inserters
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004202929_acdb4488-4d79-43cc-8445-a8163d7de46f); Time taken: 0.027 seconds
INFO  : OK
No rows affected (0.095 seconds)
[george@ip-172-31-5-64 centos]$ kinit
Password for george@WGSEBC.COM:
[george@ip-172-31-5-64 centos]$ beeline
Beeline version 1.1.0-cdh5.9.3 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-5-64.us-east-2.compute.internal@WGSEBC.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-5-64.us-east-2.compute.internal@WGSEBC.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171004203232_5d7ae43e-84cc-4dbb-8340-ffce576108a0): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171004203232_5d7ae43e-84cc-4dbb-8340-ffce576108a0); Time taken: 0.065 seconds
INFO  : Executing command(queryId=hive_20171004203232_5d7ae43e-84cc-4dbb-8340-ffce576108a0): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004203232_5d7ae43e-84cc-4dbb-8340-ffce576108a0); Time taken: 0.125 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.275 seconds)
0: jdbc:hive2://localhost:10000/default> quit;
Error: Error while compiling statement: FAILED: ParseException line 1:0 cannot recognize input near 'quit' '<EOF>' '<EOF>' (state=42000,code=40000)
0: jdbc:hive2://localhost:10000/default> [george@ip-172-31-5-64 centos]$
[ferdinand@ip-172-31-5-64 centos]$ kinit
Password for ferdinand@WGSEBC.COM:
[ferdinand@ip-172-31-5-64 centos]$ beeline
Beeline version 1.1.0-cdh5.9.3 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-5-64.us-east-2.compute.internal@WGSEBC.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-5-64.us-east-2.compute.internal@WGSEBC.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20171004203333_793eec4f-b8f3-402e-9a9e-15e9e7d8f63d): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171004203333_793eec4f-b8f3-402e-9a9e-15e9e7d8f63d); Time taken: 0.057 seconds
INFO  : Executing command(queryId=hive_20171004203333_793eec4f-b8f3-402e-9a9e-15e9e7d8f63d): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004203333_793eec4f-b8f3-402e-9a9e-15e9e7d8f63d); Time taken: 0.113 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.251 seconds)
