# Realtime Data Streaming | End-to-End Data Engineering Project
This is a cloned project. Credit to CodeWithYu

## Table of Contents
- [Introduction](#introduction)
- [System Architecture](#system-architecture)
- [What You'll Learn](#what-youll-learn)
- [Technologies](#technologies)
- [Getting Started](#getting-started)
- [Watch the Video Tutorial](#watch-the-video-tutorial)

## Introduction

This project serves as a comprehensive guide to building an end-to-end data engineering pipeline. It covers each stage from data ingestion to processing and finally to storage, utilizing a robust tech stack that includes Apache Airflow, Python, Apache Kafka, Apache Zookeeper, Apache Spark, and Cassandra. Everything is containerized using Docker for ease of deployment and scalability.

## System Architecture

![System Architecture](https://github.com/airscholar/e2e-data-engineering/blob/main/Data%20engineering%20architecture.png)

The project is designed with the following components:

- **Data Source**: We use `randomuser.me` API to generate random user data for our pipeline.
- **Apache Airflow**: Responsible for orchestrating the pipeline and storing fetched data in a PostgreSQL database.
- **Apache Kafka and Zookeeper**: Used for streaming data from PostgreSQL to the processing engine.
- **Control Center and Schema Registry**: Helps in monitoring and schema management of our Kafka streams.
- **Apache Spark**: For data processing with its master and worker nodes.
- **Cassandra**: Where the processed data will be stored.

## What You'll Learn

- Setting up a data pipeline with Apache Airflow
- Real-time data streaming with Apache Kafka
- Distributed synchronization with Apache Zookeeper
- Data processing techniques with Apache Spark
- Data storage solutions with Cassandra and PostgreSQL
- Containerizing your entire data engineering setup with Docker

## Technologies

- Apache Airflow
- Python
- Apache Kafka
- Apache Zookeeper
- Apache Spark
- Cassandra
- PostgreSQL
- Docker

## Getting Started

I am using Windows for this project :

Airflow requires vscode (windows) to run with wsl mode

1. Setting up the enviroment for Windows:
   Using linux distribution : Ubuntu
   
   a. Installing ubuntu
        ```
        wsl --install
        ``` 
   
   b. Change the default Linux distribution installed
        ```
        wsl --install -d <Distribution Name>
        ```
      OR ```
      wsl --set-default <DistributionName>
         ```

   Replace ```<Distribution Name>``` with the name of the distribution you would like to install.
   
   [Official WSL Documentation](https://learn.microsoft.com/en-us/windows/wsl/install)

3. Setup Visual Studio Code:
   
   [Download VS Code Official](https://code.visualstudio.com/)

   After installation :
   - Create a folder whereby you will be storing your project
   - Make sure you are in your working directory
   - Right click any empty space and open in terminal or powershell
   - enter wsl mode ```wsl```
   - Create VS code in WSL :  ```code .```
   
4. Setting up venv in VS code:
   Click terminal and open terminal
   
   ```bash
   python3 -m ven .venv
   ```
   
5. Installing dependancy
   - apache airflow
   ```bash
   pip install apache-airflow
   ```
   - kafka
   ```bash
   pip install kafka-python
   ```
   - cassandra
   ```bash
   pip install cassandra-driver
   ``` 
6. Run Docker Compose to spin up the services:
    ```bash
    docker-compose up
    ```

For more detailed instructions, please check out the video tutorial linked below.

## Watch the Video Tutorial

For a complete walkthrough and practical demonstration, check out his [YouTube Video Tutorial](https://www.youtube.com/watch?v=GqAcTrqKcrY).
