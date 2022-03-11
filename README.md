# learning-apache-airflow-again
## Installation
Here are the steps that I found useful installing apache airflow

1. I used pyenv to install `python 3.10.0` on the local folder using `pyenv local 3.10.0`
2. Created a virtual environment using `python -m venv venv`
3. activated the virtual environment using `source venv/bin/activate`. I am using mac.
4. Setting up the home directory for airflow using `export AIRFLOW_HOME=`pwd`/airflow`
5. Setting up the airflow version you want to install using `AIRFLOW_VERSION=2.2.4`
5. Installing airflow using `pip install "apache-airflow==${AIRFLOW_VERSION}" `

## Running airflow
1. I opened two terminals and activated the vertial environments as shown above.
2. I setup airflow home directory for each of the terminals using `export AIRFLOW_HOME=`pwd`/airflow`
3. In the first terminal, I initialised the database using `airflow db init`
3. Then in the same terminal, I setup airflow admin using 
`airflow users create --username admin --firstname FIRST_NAME --lastname LAST_NAME  --role Admin --email admin@example.org`
4. I was propted to enter password and confirm it forthe admin and the admin was created
5. Then still in the same terminal I started the webserver using `airflow webserver --port 8080`
6. In the next terminal I started the scheduler using `airflow scheduler`
6. Both servers were running and I could access airflow ui from `http://0.0.0.0:8080/home`