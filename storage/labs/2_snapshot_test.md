su - hdfs

hadoop fs -mkdir /user/Victor2806/precious

wget https://github.com/Victor2806/SEBC/archive/master.zip

mv master.zip SEBC_Victor2806.zip

hadoop fs -put SEBC_Victor2806.zip /user/Victor2806/precious/

exit

su - hdfs

hdfs dfsadmin -allowSnapshot /user/Victor2806/precious/

hdfs dfs -createSnapshot /user/Victor2806/precious/ sebc-hdfs-test

hadoop fs -rm -r /user/Victor2806/precious

hadoop fs -rm -r /user/Victor2806/precious/SEBC_Victor2806.zip

hadoop fs -cp /user/Victor2806/precious/.snapshot/sebc-hdfs-test/SEBC_Victor2806.zip /user/Victor2806/precious/

 