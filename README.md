# learning-apache-airflow-again

Here are the steps that Ifound useful instlling apache airflow

1. I used pyenv to install python 3.10.0 n the local folder using `pyenv local 3.10.0`
2. Created a virtual environment using `python -m venv venv`
3. activated the virtual environment using `source venv/bin/activate`. I am using mac.
4. Setting up the home directory for airflow using `export AIRFLOW_HOME=``pwd``/airflow`
5. Setting up the airflow version you want to install using `AIRFLOW_VERSION=2.2.4`
5. Installing airflow using `pip install "apache-airflow==${AIRFLOW_VERSION}" `