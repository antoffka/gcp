#Deploy
gcloud deployment-manager deployments create gcp303 --config labconfig.yaml

#reset passwords
gcloud compute reset-windows-password vm-bastionhost --user app_admin --zone us-central1-a
gcloud compute reset-windows-password vm-securehost --user app_admin --zone us-central1-a


#DEBUG
gcloud compute instances get-serial-port-output vm-securehost --zone us-central1-a