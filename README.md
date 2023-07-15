# large-scale-movie-recommender-systems-via-hadoop

This project aims to develop and evaluate various recommendation algorithms for a recommendation system under the hood of Hadopp/Spark. The project includes implementations of matrix factorization, memory-based collaborative filtering, hybrid systems, linear models, decision trees, and K-means clustering combined with collaborative filtering.

## Architecture

The project leverages the following components for distributed computing:

- **Hadoop Distributed File System (HDFS):** HDFS is used for storing and managing large-scale datasets across a cluster of machines. The `data.txt` file can be stored in HDFS for efficient data processing.

- **YARN (Yet Another Resource Negotiator):** YARN is the resource management framework in Hadoop. It allows for efficient allocation of computational resources across the cluster, enabling parallel processing of tasks.

- **Apache Spark:** Spark is a fast and distributed data processing framework that provides high-level APIs for distributed computing. It can be used in conjunction with Hadoop and YARN for scalable and parallel processing of recommendation algorithms.

## Usage

1. Set up HDFS and YARN on your cluster to ensure distributed storage and resource management capabilities.

2. Clone the repository to your local machine or the cluster nodes.

3. Install Apache Spark on your cluster and configure it to work with Hadoop and YARN.

5. Install the necessary dependencies and libraries mentioned in each notebook or script.

6. Open the desired notebook or script in Jupyter Notebook or any compatible Python environment on the Spark cluster.

7. Follow the instructions provided within each notebook or script to run the code, leveraging the distributed capabilities of Spark.


## Important notice

The proposed methods, such as memory based collaborative filtering and auto encoders, are not fully distributed under the hood of Hadoop/Spark. While Hadoop and Spark are powerful distributed computing frameworks, the specific algorithms and methods used in recommendation systems may not be inherently designed to leverage their full distributed capabilities.

For instance, collaborative filtering algorithms from the distributed processing capabilities of Hadoop/Spark. The data can be partitioned across nodes for parallel processing, and the similarity calculations and recommendation generation can be performed in a distributed manner. However, the core computations for collaborative filtering, such as computing similarity scores or calculating recommendations, are often performed locally on each node and then combined to generate the final recommendations.

Also, the AutoRec model code is not inherently designed to fully leverage the distributed processing capabilities of Hadoop/Spark. To achieve full distribution, alternative approaches and frameworks that explicitly support distributed computing, such as TensorFlow with Spark integration, would need to be employed.

In summary, while Hadoop/Spark enable distributed processing and can improve the scalability and performance of recommendation algorithms, the algorithms themselves may still involve operations that are performed on a single machine or node. The distributed aspect comes into play during the parallelization of computations and the aggregation of results across multiple nodes, rather than the algorithms being fully distributed from end to end.

I would greatly appreciate your professional feedback on the provided code. If you have any suggestions, improvements, or modifications that could enhance its functionality or make it more efficient, please kindly share them. Your insights and expertise are valuable in refining the code and ensuring its optimal performance. Thank you for your contribution.