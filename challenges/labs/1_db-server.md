```
MariaDB [(none)]> SHOW VARIABLES like 'hostname';
```
| Variable_name | Value            |
|---------------|------------------|
| hostname      | ip-172-31-45-105 |

```
MariaDB [(none)]> SHOW VARIABLES like 'version';
```
+---------------+----------------+
| Variable_name | Value          |
+---------------+----------------+
| version       | 5.5.57-MariaDB |
+---------------+----------------+

```
MariaDB [(none)]> show databases;
```
+--------------------+
| Database           |
+--------------------+
| information_schema |
| amon               |
| hue                |
| metastore          |
| mysql              |
| nav                |
| navms              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
