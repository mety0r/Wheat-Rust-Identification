# WheatRust Identification

## What do I need to get started?

* A [Google Cloud account](https://cloud.google.com/gcp) and a [Google Cloud Project](https://cloud.google.com/resource-manager/docs/creating-managing-projects)
* [Google Cloud SDK installed](https://cloud.google.com/sdk/docs/install) (gcloud CLI utitly)
* Trained [Machine Learning Model](app.py), our app uses an image classification model trained on a number of different classes of wheat rust
* [Docker installed](https://docs.docker.com/get-docker/)

## Build and deploy

Command to build the application. 
```
gcloud builds submit --tag gcr.io/da21cs154-wheatrust/Wheatrust  --project=da21cs154-wheatrust
```

Command to deploy the application
```
gcloud run deploy --image gcr.io/da21cs154-wheatrust/Wheatrust --platform managed  --project=da21cs154-wheatrust --allow-unauthenticatedst
```
