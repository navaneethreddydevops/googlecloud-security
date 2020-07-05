### Virtual Machines


# Google cloud CLI

```
gcloud compute zones list

gcloud compute zones list | grep us-central1

gcloud config set compute/zone us-central1-c

gcloud compute instances create "testing-instance" \
    --machine-type "n1-standard-1" \
    --image-project "debian-cloud" \
    --image "debian-9-stretch-v20190918" \
    --subnet "default"

```

# Google Cloud Shell:

```
ssh testing-instance
```