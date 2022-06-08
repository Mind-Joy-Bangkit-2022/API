# API-Documentation
### Deploy Backend Login/Regist & Quiz
URL : https://fabled-variety-351411.dt.r.appspot.com
<br />
end point : 
* /regist
parameter (username,name,password)
* /login (username,password)
* /quiz (gender,age,feeling,sadness,low_time,activities,capabilities,supported,<br /> frequently,kondisi,abuse,time_spend,appointment,self_feel,
comfortable)
#### We use APP Engine and Cloud SQL for deploying API. Here is the following workflow:
1. Make a database for registration and quiz data in Cloud SQL.
2. Connecting API in Visual Code Studio to CLoud SQL, we use IP address, databases name, and the same password in Cloud SQL.
3. Connecting APP Engine to Cloud SQL.

### Deploy Machine Learning Model

URL Deploy Image:
https://getprediction-avpq3ri45q-as.a.run.app
<br />
URL Deploy Quiz:
https://getresultquiz-avpq3ri45q-as.a.run.app
<br />
#### We use Cloud Run and Cloud SDK for deploying Machine Learning Model. Here is the following workflow:
1. Prepare model and make a Dockerfile.
2. Deploying the model using this code:

* Deploying Image Model
1. gcloud builds submit --tag gcr.io/fabled-variety-351411/emotionreq
2. gcloud run deploy --image gcr.io/fabled-variety-351411/emotionreq --platform managed

* Deploying Quiz Model
1. gcloud builds submit --tag gcr.io/fabled-variety-351411/mentalhealthreq
2. gcloud run deploy  gcr.io/fabled-variety-351411/mentalhealthreq --image platform managed
