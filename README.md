# Stock Market Kafka Streaming with AWS

Stream and analyze stock market data using Apache Kafka on AWS EC2, further processed and visualized through various AWS services.

## 📌 Overview

This project focuses on real-time streaming and analysis of stock market data, including columns such as Index, Date, Open, High, Low, Close, Adjusted Close, and CloseUSD.

![Kafka Project Architecture](Kafka-project-archiecture.jpg)

## 🛠 Prerequisites

- AWS EC2 instance (with public IPv4).
- Java 1.8 or newer.
- Apache Kafka.
- boto3 (AWS SDK for Python).
- AWS permissions (S3, Glue, Athena, Quicksight).

## 🚀 Setup

 **Kafka Installation**:
  bash:
   wget https://downloads.apache.org/kafka/3.5.1/kafka_2.12-3.5.1.tgz
   tar -xvf kafka_2.12-3.5.1.tgz

**Java Setup**:
  bash:
    java -version
    sudo yum install -y java-1.8.0-amazon-corretto-devel
  
**Zookeeper & Kafka**:
  Navigate to Kafka directory.
  Start Zookeeper and Kafka server.
  Update server.properties for public IP.

**Topic Creation**:
  bash:
    Copy code
    bin/kafka-topics.sh --create --topic demo_test --bootstrap-server <Public IPv4 address>:9092

**Producer & Consumer**: Start both in separate consoles.

## 📊 Architecture
Data flow: boto3 -> Producer -> Kafka (EC2) -> Consumer -> S3 -> Crawler -> Glue -> Athena -> Quicksight

## 📄 Dataset
The dataset captures real-time stock market metrics, detailing columns like Index, Date, Open, High, Low, Close, Adjusted Close, and CloseUSD.


