# apache-Air-Flow-Med
Invoke-WebRequest -Uri 'https://airflow.apache.org/docs/apache-airflow/2.9.0/docker-compose.yaml' -OutFile 'docker-compose.yaml'
New-Item -ItemType Directory -Path "./dags" -Force
New-Item -ItemType Directory -Path "./logs" -Force
New-Item -ItemType Directory -Path "./plugins" -Force
New-Item -ItemType Directory -Path "./config" -Force

connections 
post myuser mypassword mydatabase host.docker.internal
minio ROOTUSER CHANGEME123 host.docker.internal:9000