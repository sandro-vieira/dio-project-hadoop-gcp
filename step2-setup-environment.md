# Preparing the Environment

* Creating a budget notification
    - Menu Billing
        - Budgets & alerts
            - Create Budget
                - Fill Scope, Amount and Actions
* Enabling Service APIs 
    - Menu Compute | Compute Engine
        - VM Instances
            - Click in Enable button (no cost for this action)
* Compute Engine
    - VM Instances
        - Create Instance

```gcloud command line
gcloud compute instances create instance-hadoop --project=citric-expanse-347320 --zone=us-central1-c --machine-type=e2-standard-2 --network-interface=network-tier=PREMIUM,subnet=default --maintenance-policy=MIGRATE --service-account=302350242295-compute@developer.gserviceaccount.com --scopes=https://www.googleapis.com/auth/devstorage.read_only,https://www.googleapis.com/auth/logging.write,https://www.googleapis.com/auth/monitoring.write,https://www.googleapis.com/auth/servicecontrol,https://www.googleapis.com/auth/service.management.readonly,https://www.googleapis.com/auth/trace.append --create-disk=auto-delete=yes,boot=yes,device-name=instance-hadoop,image=projects/ubuntu-os-cloud/global/images/ubuntu-2004-focal-v20220404,mode=rw,size=100,type=projects/citric-expanse-347320/zones/us-central1-c/diskTypes/pd-balanced --no-shielded-secure-boot --shielded-vtpm --shielded-integrity-monitoring --reservation-affinity=any
```

* Active Cloud Shell

List active instances
```
gcloud compute instances list
```
Access to the VM
```
gcloud compute ssh {NAME} --zone={ZONE}

sample: gcloud compute ssh instance-hadoop --zone=us-central1-c
```

