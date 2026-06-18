# apache-Air-Flow-Med
Invoke-WebRequest -Uri 'https://airflow.apache.org/docs/apache-airflow/2.9.0/docker-compose.yaml' -OutFile 'docker-compose.yaml'
New-Item -ItemType Directory -Path "./dags" -Force
New-Item -ItemType Directory -Path "./logs" -Force
New-Item -ItemType Directory -Path "./plugins" -Force
New-Item -ItemType Directory -Path "./config" -Force

connections 
post myuser mypassword mydatabase host.docker.internal
minio ROOTUSER CHANGEME123 host.docker.internal:9000

# Apache Airflow Med

A data engineering project built using Apache Airflow to automate, schedule, and monitor data workflows. This project demonstrates workflow orchestration, task dependencies, scheduling, and pipeline monitoring using Airflow.

## Project Overview

The goal of this project is to:

- Automate data processing workflows
- Schedule recurring jobs using Airflow DAGs
- Monitor task execution and failures
- Implement ETL/data pipeline concepts
- Showcase workflow orchestration skills

## Features

- Apache Airflow DAG implementation
- Automated workflow scheduling
- Task dependency management
- Logging and monitoring
- Modular project structure
- Scalable pipeline design

## Tech Stack

- Python
- Apache Airflow
- SQL
- Docker (if applicable)
- PostgreSQL (if applicable)

## Project Structure

```text
apache-Air-Flow-Med/
│
├── dags/
│   ├── *.py
│
├── plugins/
│
├── logs/
│
├── config/
│
├── requirements.txt
│
└── README.md
```

## Installation

### Clone Repository

```bash
git clone https://github.com/Pabis-code-crafts/apache-Air-Flow-Med.git
cd apache-Air-Flow-Med
```

### Create Virtual Environment

```bash
python -m venv venv
```

Activate:

Windows

```bash
venv\Scripts\activate
```

Linux/Mac

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

## Running Airflow

Initialize database:

```bash
airflow db init
```

Create admin user:

```bash
airflow users create \
--username admin \
--firstname Admin \
--lastname User \
--role Admin \
--email admin@example.com
```

Start webserver:

```bash
airflow webserver
```

Start scheduler:

```bash
airflow scheduler
```

## DAGs

This project contains Airflow DAGs responsible for:

- Data extraction
- Data transformation
- Data loading
- Workflow monitoring

Detailed DAG descriptions can be added here.

## Learning Outcomes

Through this project I gained experience in:

- Workflow orchestration
- DAG development
- Scheduling and automation
- ETL pipeline design
- Airflow monitoring and debugging
- Production-style data engineering concepts

## Future Improvements

- Add Docker support
- Integrate cloud storage
- Add CI/CD pipeline
- Implement alerting and notifications
- Add automated testing

## Author

**Pavithran**

GitHub: https://github.com/Pabis-code-crafts

## License

This project is for educational and portfolio purposes.
