Map Reduce Example for:

http://hbase.apache.org/book.html#arch.bulk.load

1 ) Export project's JAR to bulk.jar

2 ) Copy file1.txt to hdfs

3 ) Create table using:
	create 'datatsv', {NAME=>'m'}
	
4 ) Run the JAR file using:
hadoop jar $HBASE_HOME/bulk.jar com.cloudera.examples.hbase.bulkimport.Driver /hdfsDirectory/file1.txt /hdfsDirectory/outputname/ tablename

and change hdfsdirectory, outputfilename, and tablename accordingly

5 ) Modify MapReduce job for your needs

-- Paschalis M.