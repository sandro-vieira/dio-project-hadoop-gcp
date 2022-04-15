# Running from panel

- Menu Analytics | Dataproc
- Clusters
    - Submit Job
        - Job type:
        Spark

- Main class or jar:
    
    > org.apache.spark.examples.SparkPi
        
- Jar files: 
        
    > file:///usr/lib/spark/examples/jars/spark-examples.jar

- Arguments

    > 1000

- Job result
    
    > Pi is roughly 3.141645391416454
    

# Running from console

  - Open cloud shell
    
    > gcloud dataproc jobs submit spark \
    > --cluster=cluster-desafio-dataproc-sv \
    > --region="us-central1" \
    > --class=org.apache.spark.examples.SparkPi \
    > --jars=file://usr/lib/spark/examples/jars/spark-examples.jar \
    > -- 1000

- Job result
    
    > Pi is roughly 3.141645391416454
