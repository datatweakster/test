# test

**Steps to setup a MLflow Tracking Server**

1. Create EC2 instance
2. sudo apt-get update
3. sudo apt-get install python3 python3-venv python3-pip -y
4. python3 -m venv mlflow_env
5. source mlflow_env/bin/activate
6. pip install mlflow boto3
7. pip list
8. Create S3 bucket
9. Setup IAM Role -> AmazonS3FullAccess -> EC2 MLflow S3 Access
10. sudo apt-get install screen -y
11. screen -S mlflow
12. mlflow server --backend-store-uri=./mlruns --default-artifact-root s3://your-bucket-name --host 0.0.0.0 --port 5000
13. Setup security group
