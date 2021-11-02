# Firebase Emulator for development

2021 Nov 3 updated
## step 1
First create GCP project and initialize firebase.

## step 2
Go to IAM page in GCP and select service account page. Then select or create your service account and download key. Rename json file as `sa.json` that you downloaded and put that file in root.

## step 3
create file `src/firebase/.firebaserc` and paste below. Set your project id to `YOUR_PROJECT_ID`.
```
{
  "projects": {
    "default": "YOUR_PROJECT_ID"
  }
}

```
## step 4
run `docker-compose up --build`
After that enter inside the container `docker exec -it firebase-emulator sh`
Then run command `firebase login --no-localhost`

## step 5
init firebase `firebase init`

## step 6
run emulator `firebase emulators:start`
Access to `http://localhost:4000/`

# note
After initialized emulator, it is not recommend to push `src/firebase/` directory to public repository in GitHub.
