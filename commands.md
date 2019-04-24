###Most used commands
```
docker-compose -f docker-compose-local.yml up -d
```

```
docker-compose -f docker-compose-local.yml kill
```

```
docker-compose -f docker-compose-local.yml rm -f
```

```
docker exec -it namenode sh
```

```
hadoop fs -mkdir /<username>
```

```
hadoop fs -touchz /test/miPrimerArchivo.txt
```

```
hadoop fs -ls /
```

```
hadoop fs -lsr /user/hadoop/dir
```

```
hadoop fs -cat /<username>/<folder>/xyz.csv
```

```
hadoop fs -tail /<username>/<folder>/xyz.csv
```

```
hadoop fs -mv /<username>/<folder>/xyz.csv /user/<folder>/results/xyz.csv
```

```
hadoop fs -cp /<username>/<folder>/xyz.csv /user/<folder>/results/xyz.csv
```

```
hadoop fs - put /tmp/xyz.csv /user/<folder>/xyz.csv
```

```
hadoop fs -moveFromLocal /tmp/xyz.csv /user/<folder>/xyz.csv
```

```
hadoop fs -get /<username>/<folder>/xyz.csv /tmp/xyz.csv
```

```
hadoop fs -moveToLocal /<username>/<folder>/xyz.csv /tmp/xyz.csv
```

```
hadoop fs -rm /<username>/<folder>/results/xyz.csv
```

```
hadoop fs -rmr /<username>/<folder>/result
```

```
hadoop fs -chmod -R 777 /<username>/<folder>/results
```

```
hadoop fs -chown -R hdfs /<username>/<folder>/results
```
