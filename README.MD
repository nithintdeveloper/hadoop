Hadoop is a widely used open-source software framework that is used for distributed storage and processing of big data sets across clusters of commodity computers. The framework is designed to scale from single servers to thousands of machines, each offering local computation and storage.

Hadoop consists of two primary components: the Hadoop Distributed File System (HDFS) and the MapReduce programming model. HDFS is a distributed file system that allows data to be stored across many different machines, while MapReduce is a programming model that allows developers to write distributed processing jobs that can operate on large data sets.

Hadoop has become a popular tool for big data processing and analysis due to its ability to efficiently process and store large amounts of data across many different machines. It has been widely used in various industries, including finance, healthcare, and telecommunications, among others.

#

Commands Used

git clone https://github.com/big-data-europe/docker-hadoop.git

docker-compose up -d

docker container ls

docker exec -it namenode bash

hdfs dfs -ls /      // This command is used to list all the files

wget https://repo1.maven.org/maven2/org/apache/hadoop/hadoop-mapreduce-examples/2.7.1/hadoop-mapreduce-examples-2.7.1-sources.jar


docker cp  hadoop-mapreduce-examples-2.7.1-sources.jar namenode:/tmp

docker exec -it namenode /bin/bash
hadoop jar hadoop-mapreduce-examples-2.7.1-sources.jar org.apache.hadoop.examples.WordCount input output 
