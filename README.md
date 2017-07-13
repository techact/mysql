# mysql

SELECT table_schema AS "Database name", SUM(data_length + index_length) / 1024 / 1024 AS "Size (MB)" FROM information_schema.TABLES GROUP BY table_schema;

+---------------------+--------------+
| Database name       | Size (MB)    |
+---------------------+--------------+
| info                |   0.01562500 |
| information_schema  |   0.00878906 |
| mysql               |   0.64052296 |
| performance_schema  |   0.00000000 |
+---------------------+--------------+


SELECT table_name AS "Table", round(((data_length + index_length) / 1024 / 1024 ), 2) "Size in MB" FROM information_schema.TABLES WHERE table_schema = "mysql";

+---------------------------+------------+
| Table                     | Size in MB |
+---------------------------+------------+
| columns_priv              |       0.00 |
| db                        |       0.01 |
| event                     |       0.00 |
| func                      |       0.00 |
| general_log               |       0.00 |
| help_category             |       0.00 |
| help_keyword              |       0.12 |
| help_relation             |       0.03 |
| help_topic                |       0.48 |
| host                      |       0.00 |
| ndb_binlog_index          |       0.00 |
| plugin                    |       0.00 |
| proc                      |       0.00 |
| procs_priv                |       0.00 |
| proxies_priv              |       0.01 |
| servers                   |       0.00 |
| slow_log                  |       0.00 |
| tables_priv               |       0.00 |
| time_zone                 |       0.00 |
| time_zone_leap_second     |       0.00 |
| time_zone_name            |       0.00 |
| time_zone_transition      |       0.00 |
| time_zone_transition_type |       0.00 |
| user                      |       0.00 |
+---------------------------+------------+

