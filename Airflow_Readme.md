###Airflow Docker 

mkdir airflow-docker
cd airflow-docker 

curl -LfO "https://airflow.apache.org/docs/apache-airflow/stable/docker-compose.yaml"

ymanan@88665a102c35 airflow-docker % mkdir ./dags ./plugins ./logs
ymanan@88665a102c35 airflow-docker % echo -e "AIRFLOW_UID=$(id -u)\nAIRFLOW_GID=0" >.env
ymanan@88665a102c35 airflow-docker % docker-compose up airflow-init
docker-compose up 
docker ps 

# Access the docker command line interface 
docker exec < container-id> airflow version

# Interact via api 
curl -X GET "http://localhost:8080/api/v1/dags"
create below env variable in docker compose file 

AIRFLOW__API__AUTH_BACKEND: 'airflow.api.auth.backend.basic_auth'

###Airflow-Direct

Create a virtual env in python which comes preinstalled with venv
  1. python3 -m venv /Users/ymanan/Documents/ProjectVirtualenv/airflowtest
  2. Enabled the env 
  	source  /Users/ymanan/Documents/ProjectVirtualenv/airflowtest/bin/activate
  3. pip install apache-airflow
  4. Initilise sql lite db 
  	airflow db init
  5. set airflow home variable to be current working directory(/Users/ymanan/airflow/)
  	export AIRFLOW_HOME=$PWD

Setting the 
export AIRFLOW__API__AUTH_BACKEND="airflow.api.auth.backend.basic_auth"
