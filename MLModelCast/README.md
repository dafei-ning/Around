# How to setup the machine learning model

### 1. Download and install Google CLoud SDK

Download [link](https://cloud.google.com/sdk/downloads)


Set a name for your new bucket.
PROJECT_ID=$(gcloud config list project --format "value(core.project)")
BUCKET_NAME=${PROJECT_ID}-mlengine
Check the bucket name that you created.
 	echo $BUCKET_NAME
REGION=us-central1
4 	Create the new bucket:
gsutil mb -l $REGION gs://$BUCKET_NAME
Note: Use the same region where you plan on running Cloud ML Engine jobs.


### 2. Download the sample from the Git repository.

### 3. Install dependencies
