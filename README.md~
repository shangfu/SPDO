# SPDO

### Obtain the distance oracles
To generate the distance oracles, please go to see 
[ASDO](https://github.com/shangfu/ASDO).

We also provide the demo distance oracles of the New York road network
in `http://s3.amazonaws.com/oracleusa1114/nyspark` for all nodes of the DO-tree
and `http://s3.amazonaws.com/oracleusa1114/nyspark_ac` for all leaves of the DO-tree.
These two files are public and their format are the SequenceFile in Apache Spark. You can use the AWS Command Line Interface (CLI) commands to download these two files.

In addtion, if you generate the distance oracles by yourself using ASDO codes, `src/expand/` shows how to transfer the  distance oracles to Spark distance oracles that include all nodes of DO-tree.


### Start Spark with IndexedRDD

First, you need to download the IndexedRDD package from [here](http://spark-packages.org/package/amplab/spark-indexedrdd) and you can see the examples about using this package [here](https://github.com/amplab/spark-indexedrdd).
After you have the indexedRDD, you can start the Spark shell such as the following commend
> ./bin/spark-shell --driver-memory 8g --executor-memory 8g --jars spark-indexedrdd-0.1.jar,guava-18.0.jar

where guava-18.0.jar is a widely used package for HashMap data structure.


### Load distance oracles in Spark

Here we only provide the Basic and BS solutions. The WP solution in our paper is for commercial use now. We provide the load scripts `src/load/load_Basic.scalar` and `src/load/load_BS.scalar` for Basic and BS respectively. 
You can specify the number of partitions you want. Spark will evenly assign the partitions to the slave nodes.


### Functions for shortest distances retrieval in Spark
We provide the function scripts `src/function/function_Basic.scalar` and `src/function/function_BS.scalar` for Basic and BS respectively. You can load them in the Spark shell. Here we only provide the setting numbers for the New York road network. If you want to know how to specify the setting numbers for your own road networks, please read the [ASDO](https://github.com/shangfu/ASDO).

### Query examples in Spark
We provide how to retrieve the shortest distances in `src/query/`. It is easy to answer a batch of source-target queries using the functions in `src/function/`. Here each source-target query includes 4 doubles, e.g., latitude #1, longitude #1, latidue #2, and longitude #2. On top of it, people can develop further functions such as the heat map in our SPDO paper.


### Heat map generation
To generate the spatial heat map, we borrow the codes from `https://github.com/jeffkaufman/apartment_prices`. 
We put our heat map generation and html fushion in `src/heatmap`.

