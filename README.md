# Distributed-system
The purpose of this project is to processe Amazon review data by building a distributed system on AWS. The pipeline includes automating data extraction from S3 to MongoDB and clustering books on Amazon based on the review data using pyspark ML.

Our method is to get the feature vectors of each book by applying TFIDF to collections of the texts of corresponding books and use these feature vectors to cluster the books. Once we get the clusters, we would have some sense of book similarities. We can even try calculating distances between every two books in one cluster.  

The large scale of dataset makes this pipeline and approach impractical to implement on the local machine due to the limit of memory and computing performances. Consequently, we built a data pipeline with the distributed system. Amazon Web Services (AWS) provides high availability and scalability and makes its components including storage and processing engines to be compatible. Thus, for this project, we selected it as the primary platform to store data in the data lake(S3), load data into the distributed database (MongoDB on EC2) and apply machine learning algorithms (Spark on EMR).
