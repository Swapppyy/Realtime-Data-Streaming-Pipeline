# Realtime Data Streaming Pipeline using Airflow, Kafka, Spark, Zookeeper and Cassandra

## Table of Contents
- [Introduction](#introduction)
- [System Architecture](#system-architecture)
- [Key steps in the project](#Key-steps-in-the-project)
- [Getting Started](#getting-started)

## Introduction

Built an end-to-end data engineering pipeline. It covers each stage from data ingestion to processing and finally to storage, utilizing a robust tech stack that includes Apache Airflow, Python, Apache Kafka, Apache Zookeeper, Apache Spark, and Cassandra. Everything is containerized using Docker for ease of deployment and scalability.

## System Architecture

![System Architecture](https://github.com/Swapppyy/Realtime-Data-Streaming-Pipeline/blob/main/zoo.png)

The project is designed with the following components:

- **Data Source**: Used `randomuser.me` API to generate random user data for our pipeline.
- **Apache Airflow**: Responsible for orchestrating the pipeline and storing fetched data in a PostgreSQL database.
- **Apache Kafka and Zookeeper**: Used for streaming data from PostgreSQL to the processing engine.
- **Control Center and Schema Registry**: Helps in monitoring and schema management of our Kafka streams.
- **Apache Spark**: For data processing with its master and worker nodes.
- **Cassandra**: Where the processed data will be stored.

## Key steps in the project

- Setting up a data pipeline with Apache Airflow
- Real-time data streaming with Apache Kafka
- Distributed synchronization with Apache Zookeeper
- Data processing techniques with Apache Spark
- Data storage solutions with Cassandra and PostgreSQL
- Containerizing entire data engineering setup with Docker

## Getting Started

1. Clone the repository:
    ```bash
    git clone https://github.com/Swapppyy/Realtime-Data-Streaming-Pipeline.git
    ```

2. Navigate to the project directory:
    ```bash
    cd Realtime-Data-Streaming-Pipeline
    ```

3. Run Docker Compose to spin up the services:
    ```bash
    docker-compose build --no-cache
    docker-compose up airflow-init
    docker-compose up -d
    ```
