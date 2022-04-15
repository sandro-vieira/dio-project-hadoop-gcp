# Dataproc

* Creating Dataproc Cluster
    - Menu Analytics | Dataproc
        - Enable Cloud Dataproc API (if required)
        - Create Cluster
            Set up cluster:

                - Cluster type: Standard
                - Image Type and Version: 2.0-debian10
                - Enable component gateway
                - Components:
                    - Jupyter Notebook
                    - Zeppelin Notebook
                    - Zookeeper
            
            Configure nodes
                - Master node:

                    - Keep default options
                - Worker nodes:
                
                    - Number of worker nodes: 3
    - Console
```
gcloud dataproc clusters create cluster-desafio-dataproc-sv --enable-component-gateway --region us-central1 --subnet default --zone us-central1-a --master-machine-type n1-standard-4 --master-boot-disk-size 500 --num-workers 3 --worker-machine-type n1-standard-4 --worker-boot-disk-size 500 --image-version 2.0-debian10 --optional-components JUPYTER,ZEPPELIN,ZOOKEEPER --project citric-expanse-347320
```    

* Creating a storage
    - Menu Storage | Cloud Storage
        - Create Bucket
