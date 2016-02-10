# SPDO

### Obtain the distance oracles
To generate the distance oracles, please go to see 
[ASDO](https://github.com/shangfu/ASDO).

We also provide the demo distance oracles of the New York road network
in `http://s3.amazonaws.com/oracleusa1114/nyspark` for all nodes of the DO-tree
and `http://s3.amazonaws.com/oracleusa1114/nyspark_ac` for all leaves of the DO-tree.
These two files are public and their format are the SequenceFile in Apache Spark. You can use the AWS Command Line Interface (CLI) commands to download these two files.




First, you need to download the IndexedRDD package from [here](http://spark-packages.org/package/amplab/spark-indexedrdd) and you can see the examples about using this package [here](https://github.com/amplab/spark-indexedrdd).
After you have the indexedRDD, you can start the Spark shell like this
> ./bin/spark-shell --driver-memory 8g --executor-memory 8g --jars spark-indexedrdd-0.1.jar,guava-18.0.jar

guava-18.0.jar is a widely used package for HashMap data structure.


### Load distance oracles in Spark
