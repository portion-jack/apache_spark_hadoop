## RDD

### 분산처리

```
baseline
from pyspark import SparkContext
sc = SparkContext('local')
```

```
transform function => return rdd
action function => return value
```

```
rdd.take(n) <=> df.head(n)

rdd.map(lambda)
rdd.sortBy(lambda)
rdd.map(lambda).countByValues()

weightrdd.map(lambda x:x.split(',')).zipWithIndex().collect()
```
