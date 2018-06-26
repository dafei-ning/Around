# How to setup the machine learning model

### 1. Download and install Google CLoud SDK

Download [link](https://cloud.google.com/sdk/downloads) https://cloud.google.com/sdk/downloads


### 2. Build the machine learning model

Or download the sample from the Git repository.

### 3. Install dependencies

拿cloudml-samples举例在cloudml-samples-master/flowers/requirements.txt
```
apache-beam[gcp]==2.3.0
pillow==4.0.0
tensorflow==1.4.1
```
terminal/console install 
```
sudo pip install -r requirements.txt
```

Enable following APIs

* Cloud Machine Learning Engine
* Compute Engine
* Dataflow

```

### 4. Set up a cloud storage bucket

Set a name for a new bucket.
```
	PROJECT_ID=$(gcloud config list project --format "value(core.project)")
	BUCKET_NAME=${PROJECT_ID}-mlengine
```
Check the bucket name
```
 	echo $BUCKET_NAME
```
Set region where it runs Cloud ML Engine jobs.
```
	REGION=us-central1
```
Create the new bucket:
```
	gsutil mb -l $REGION gs://$BUCKET_NAME
```
