Tecnologías para el Tratamiendo de Datos Masivos
================================================

Working draft...





## Tecnologías Big Data (Hadoop, Spark, Hive, Rspark, Sparklyr)

Introducción a los conceptos básicos del ecosistema Hadoop

Descargar Spark de https://spark.apache.org/downloads.html
y disponer al menos de Java 7

```
tar -xzf spark-1.5.2-bin-hadoop2.6.tgz
sudo mv spark-1.5.2-bin-hadoop2.6 /opt/spark
export SPARK_HOME=/opt/spark
export PATH=$SPARK_HOME/bin:$PATH
```

Ejecutar pyspark o sparkshell para saber si está correctamente instalado.


```
spark-submit --class org.apache.spark.examples.SparkPi --master local $SPARK_HOME/examples/jars/spark-examples*.jar 10

Pi is roughly 3.140576

```

<!-- https://rpubs.com/wendyu/sparkr -->


Set system environment by pointing R session to the installed SparkR.


```r
Sys.setenv(SPARK_HOME = "/home/gltaboada/spark/")
.libPaths(c(file.path(Sys.getenv("SPARK_HOME"), "R", "lib"), .libPaths()))
library(SparkR)
```

Initialize Spark context and SQL context


```r
sc <- sparkR.session(master = "local",sparkEnvir = list(spark.driver.memory="2g"))
sqlContext <- sparkR.session(sc)
```


## Visualización y Generación de Cuadros de Mando



## Introducción al Análisis de Datos Masivos


