# cloud-run-concurrency

1. Create a Pub/Sub topic.
2. Add code in your Cloud Run service to respond to the Pub/Sub messages sent to the topic you created.
3. Create a service account with the required permissions.
4. Create a Pub/Sub subscription and associate it with the service account. This subscription will send to your service any message that is published to the topic.

```
PROJECT=mm-cloud-run-concurrency
REGION=us-central1

gcloud config set project $PROJECT
gcloud config set compute/region $REGION
```