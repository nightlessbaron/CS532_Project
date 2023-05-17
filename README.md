# CS 532 Project: Harnessing the Power of Big Data: A Big Data Analysis of E-commerce Reviews using PySpark

### Team members: Kartik Gupta, Shreya Gupta, Varad Pimpalkhute

This project aims to develop a sentiment classification system for customer reviews using PySpark, SparkML, and natural language processing (NLP) techniques. The system will enable businesses to gain valuable insights into customer satisfaction levels and preferences, aiding in decision-making regarding product/service enhancements and marketing strategies.

The project utilizes the Amazon Review Dataset, a comprehensive collection of customer reviews from various product categories. The dataset is stored in MongoDB to ensure scalability and high performance, leveraging features such as data distribution and replication.

The pipeline consists of data collection, pre-processing, feature extraction, model training, and sentiment classification stages. The customer reviews are pre-processed using techniques like tokenization, stop-word removal, stemming, and lemmatization. Feature extraction is performed using methods such as Bag of Words, TF-IDF, and Word2Vec.

Multiple machine learning algorithms, including Support Vector Machines (SVM), Random Forest, and Naive Bayes, are experimented with to build the sentiment classification model. PySpark's SparkML library is utilized for efficient model training and evaluation.

The performance of the sentiment classification model is evaluated using metrics such as accuracy, precision, recall, and F1-score. Additionally, the pipeline's performance in terms of latency and throughput is assessed.

By leveraging PySpark, MongoDB, and NLP techniques, this project aims to provide businesses with an automated system for analyzing and classifying customer reviews, ultimately leading to improved decision-making and enhanced customer satisfaction.

The project's code and documentation can be found in this GitHub repository, providing a comprehensive guide for understanding and replicating the sentiment classification system for customer reviews.

To run the sentiment classification system for customer reviews, follow these steps:

1. Clone the GitHub repository to your local machine:
   ```
   git clone <repository-url>
   ```
2. Ensure you have the required dependencies installed. You can install them using pip:
   ```
   apt-get update
   apt-get install openjdk-8-jdk-headless -qq > /dev/null
   wget -q http://archive.apache.org/dist/spark/spark-3.3.1/spark-3.3.1-bin-hadoop3.tgz
   tar xf spark-3.3.1-bin-hadoop3.tgz
   pip install -q findspark
   ```
3. Download the Amazon Review Dataset (https://cseweb.ucsd.edu/~jmcauley/datasets.html#amazon_reviews) and place it in the project directory.
   ```
   # Download and extract the data
   !wget https://jmcauley.ucsd.edu/data/amazon_v2/categoryFiles/Magazine_Subscriptions.json.gz --no-check-certificate
   # !wget https://datarepo.eng.ucsd.edu/mcauley_group/data/amazon_v2/categoryFiles/All_Beauty.json.gz --no-check-certificate
   !gzip -d Magazine_Subscriptions.json.gz
   ```
4. Open the config.py file and modify the configuration settings according to your setup
5. Run the run.py file to start the sentiment classification system:
   ```
   python run.py
   ```
6. The system will perform data preprocessing, feature extraction, model training, and sentiment classification on the customer reviews.

Please note that running the sentiment classification system may require substantial computational resources, especially when working with large datasets. It is recommended to have sufficient memory and processing power to ensure optimal performance.
   
