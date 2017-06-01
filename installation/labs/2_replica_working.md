```
mysql> SHOW MASTER STATUS;
+-------------------------+----------+--------------+------------------+
| File                    | Position | Binlog_Do_DB | Binlog_Ignore_DB |
+-------------------------+----------+--------------+------------------+
| mysql_binary_log.000004 |      290 |              |                  |
+-------------------------+----------+--------------+------------------+
1 row in set (0.00 sec)
```
```
mysql> START SLAVE;
ERROR 1200 (HY000): The server is not configured as slave; fix in config file or with CHANGE MASTER TO
mysql> CHANGE MASTER TO MASTER_HOST='ec2-52-43-127-254.us-west-2.compute.amazonaws.com', MASTER_USER='root', MASTER_PASSWORD='', MASTER_LOG_FILE='mysql_binary_log.000004', MASTER_LOG_POS=290;
Query OK, 0 rows affected (0.01 sec)

mysql> START SLAVE;
Query OK, 0 rows affected (0.00 sec)
```
```
mysql> SHOW SLAVE STATUS \G
*************************** 1. row ***************************
               Slave_IO_State: Connecting to master
                  Master_Host: ec2-52-43-127-254.us-west-2.compute.amazonaws.com
                  Master_User: root
                  Master_Port: 3306
                Connect_Retry: 60
              Master_Log_File: mysql_binary_log.000004
          Read_Master_Log_Pos: 290
               Relay_Log_File: mysqld-relay-bin.000001
                Relay_Log_Pos: 4
        Relay_Master_Log_File: mysql_binary_log.000004
             Slave_IO_Running: Connecting
            Slave_SQL_Running: Yes
              Replicate_Do_DB:
          Replicate_Ignore_DB:
           Replicate_Do_Table:
       Replicate_Ignore_Table:
      Replicate_Wild_Do_Table:
  Replicate_Wild_Ignore_Table:
                   Last_Errno: 0
                   Last_Error:
                 Skip_Counter: 0
          Exec_Master_Log_Pos: 290
              Relay_Log_Space: 107
              Until_Condition: None
               Until_Log_File:
                Until_Log_Pos: 0
           Master_SSL_Allowed: No
           Master_SSL_CA_File:
           Master_SSL_CA_Path:
              Master_SSL_Cert:
            Master_SSL_Cipher:
               Master_SSL_Key:
        Seconds_Behind_Master: NULL
Master_SSL_Verify_Server_Cert: No
                Last_IO_Errno: 2003
                Last_IO_Error: Waiting for master to send event
               Last_SQL_Errno: 0
               Last_SQL_Error:
  Replicate_Ignore_Server_Ids:
             Master_Server_Id: 0
1 row in set (0.00 sec)

mysql>
```
