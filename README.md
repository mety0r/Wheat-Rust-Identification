# WheatRust Identification Web App
This project is a web application that identifies wheat crop health based on an uploaded image. The app utilizes a pre-trained deep learning model to classify the image into categories like ```healthy```, ```leaf rust```, or ```stem rust```. The model is deployed using Streamlit, a framework for building interactive web applications.

## Dependencies

* A [Google Cloud account](https://cloud.google.com/gcp) and a [Google Cloud Project](https://cloud.google.com/resource-manager/docs/creating-managing-projects)
* [Google Cloud SDK installed](https://cloud.google.com/sdk/docs/install) (gcloud CLI utitly)
* Trained [Machine Learning Model](app.py), our app uses an image classification model trained on a number of different classes of wheat rust
* [Docker installed](https://docs.docker.com/get-docker/)

## Build and deploy
### 1. Getting the app running

1. Clone this repo
```
git clone https://github.com/mety0r/Wheat-Rust-Identification.git
```
2. Create and activate a virtual environment 
```
pip install virtualenv
virtualenv <ENV-NAME>
source <ENV-NAME>/bin/activate
```
4. Install the required dependencies
```
pip install -r requirements.txt
```
5. Activate Streamlit and run `app.py`
```
streamlit run app.py
``` 


Command to build the application in GCP.
```
gcloud builds submit --tag gcr.io/da21cs154-wheatrust/Wheatrust  --project=da21cs154-wheatrust
```

Command to deploy the application
```
gcloud run deploy --image gcr.io/da21cs154-wheatrust/Wheatrust --platform managed  --project=da21cs154-wheatrust --allow-unauthenticatedst
```
