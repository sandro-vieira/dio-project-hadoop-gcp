# dio-project-hadoop-gcp
Fully Managed Hadoop Ecosystem with Google Cloud Dataproc

## Dataproc GCP Challenge

The challenge is part of the course on the Digital Innovation One platform:

__*Creating a fully managed Hadoop ecosystem with Google Cloud Platform*__

The challenge is to perform data processing using the Dataproc product from GCP. This processing will count the words of a book and inform how many times each word appears in it.

---

### Challenge Steps

1. Create a bucket in Cloud Storage
1. Update the ```contador.py``` file with the name of the Bucket created in the lines that contain ```{YOUR_BUCKET}```.
1. Upload the ```contador.py``` and ```livro.txt``` files to the created bucket

1. Use the code in a Dataproc cluster, running a PySpark Job calling ```gs://{YOUR_BUCKET}/contador.py```
1. The Job will generate a folder in the bucket called ```result```. Inside this folder the file ```part-00000``` will contain the word list and how many times it is repeated throughout the book.
