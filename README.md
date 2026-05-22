# IoT Data Aggregation and Analysis

This project implements a containerized IoT data aggregation system using Flask, SQLite, Docker, and Hadoop Streaming.

## Project Overview

The system collects measurements from multiple virtual IoT sensors. Each sensor sends data to a Flask API, which stores the data in a relational SQLite database. The stored measurements can be retrieved through API endpoints and processed using Hadoop Streaming to compute statistical summaries such as average, minimum, and maximum values.

## Main Features

- Flask API for sensor data ingestion and retrieval
- Relational SQLite database with primary and foreign keys
- Dockerized virtual sensors
- Hadoop Streaming for batch data processing
- MapReduce-based calculation of min, max, and average values
- Distributed Hadoop workload across multiple containers
- Support for multiple sensor types such as temperature, pressure, air quality, and CO2

## Technologies Used

- Python
- Flask
- SQLite
- Docker
- Hadoop Streaming
- MapReduce
- REST API
- Linux basics

## Example API Endpoints

```text
/store?sensor_id=1&lat=59.3293&lon=18.0686&type=Temperature Sensor&timestamp=2025-02-24 12:34&value=13.9
/retrieve?sensor_id=1&start_time=2025-02-24 12:00&end_time=2025-02-24 13:00
/fetch?type=Temperature Sensor
