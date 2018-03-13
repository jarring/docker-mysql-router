# docker-mysql-router

## mysql-binary-log-file-position
###  master: 
#####   1、CREATE USER 'repl'@'%' IDENTIFIED BY 'password';
#####    2、GRANT REPLICATION SLAVE ON *.* TO 'repl'@'%';
#####    3、FLUSH TABLES WITH READ LOCK;
#####    4、-- copy data from master to slave
#####    5、SHOW MASTER STATUS;
#####    8、UNLOCK TABLES;
###  slave:
#####    6、CHANGE MASTER TO MASTER_HOST='master_host_name',  MASTER_USER='replication_user_name（repl）',  MASTER_PASSWORD='replication_password（password）', MASTER_LOG_FILE='recorded_log_file_name（5.File）', MASTER_LOG_POS=recorded_log_position（5.Position）;
#####    7、start slave;

    
