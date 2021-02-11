pythonfile.py

```python
from pyspark.sql import SparkSession
spark = SparkSession.builder.appName("appName").getOrCreate()
sc = spark.sparkContext
rdd = sc.parallelize([1,2,3,4,5,6,7])
print(rdd.count())
```

Run the above program with configurations you want : eg :

```bash
YOUR_SPARK_HOME/bin/spark-submit --master yourSparkMaster --num-executors 20 --executor-memory 1G --executor-cores 2 --driver-memory 1G pythonfile.py
```

