# WheatRust-StreamlitApp

## Build and deploy

Command to build the application. PLease remeber to change the project name and application name
```
gcloud builds submit --tag gcr.io/da21cs154-wheatrust/Wheatrust  --project=da21cs154-wheatrust
```

Command to deploy the application
```
gcloud run deploy --image gcr.io/da21cs154-wheatrust/Wheatrust --platform managed  --project=da21cs154-wheatrust --allow-unauthenticatedst
```