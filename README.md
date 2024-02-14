# Apache airflow quick start in docker

### Setting the right Airflow user
```bash
echo -e "AIRFLOW_UID=$(id -u)" > .env
```


### Initialize the database
```bash
docker compose up airflow-init
```


After initialization is complete, you should see a message like this:
```bash
airflow-init_1       | Upgrades done
airflow-init_1       | Admin user airflow created
airflow-init_1       | 2.8.1
start_airflow-init_1 exited with code 0
```

### Running Airflow
```bash
docker compose up -d
```

### To stop and delete containers, delete volumes with database data and download images, run:
```bash
docker compose down --volumes --rmi all
```

## Links:
* [Running Airflow in Docker](https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html)

