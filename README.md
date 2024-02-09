# MLflow-Basic-Operation


## For Dagshub:

MLFLOW_TRACKING_URI=https://dagshub.com/atharvac1301/MLflow-Basic-Operation.mlflow \
MLFLOW_TRACKING_USERNAME=atharvac1301 \
MLFLOW_TRACKING_PASSWORD=fcc56715d30099c587b900a8711bff8195c6cc1a \
python script.py


```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/atharvac1301/MLflow-Basic-Operation.mlflow

export MLFLOW_TRACKING_USERNAME=atharvac1301

export MLFLOW_TRACKING_PASSWORD=fcc56715d30099c587b900a8711bff8195c6cc1a


```



# MLflow on AWS

## MLflow on AWS setup:

1. Login to AWS console.
2. Create IAM suer with Admin Access
3. Export the credentials in your AWS CLI by running "aws configure"
4. Create a s3 bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following commands on EC2 machine:
```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install  pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell

## Then set aws credentials
aws configure


# Finally
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-test-23

# open public IPv4 DNS to the port 5000


# set uri in your local terminal and in your code
export MLFLOW_TRACKING_URI=""


```
