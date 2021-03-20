# How to Automate Onboarding an Openshift cluster to Check Point CloudGuard Native

![header image](img/opens.png)                            ![header image](img/cg.png) 

This tutorial is details how to onboard Openshift cluster to CloudGuard native using automation scripts. 

(Manual onboarding guide is [here](https://github.com/jaydenaung/cloudguard-OpenShift). The original repo is forked from [Dean Houari's Repo](https://github.com/chkp-dhouari/cloudguard-OpenShift).

## Prerequisites 

* Register for a CloudGuard native account. https://secure.dome9.com/v2/register/invite
* Generate CloudGuard API key and secret here https://secure.dome9.com/v2/settings/credentials 


### Run the following command:
```
git clone https://github.com/jaydenaung/cloudguard-onboard-openshift
```

## Using automation scripts to automate the onboarding process 

### Bash Shell

1. Make sure that [uid1000.json](uid1000.json) and [cp-cloudguard-openshift.yaml](cp-cloudguard-openshift.yaml) are in the same directory as [onboard-1.sh](onboard-1.sh). 
2. Edit variables and run [onboard-1.sh](onboard-1.sh) to onboard the cluster. 

``` chmod +x onboard-1.sh
    ./onboard-1.sh
```

Alternatively, you can follow the instructions below and execute command lines manually. 

### Python Script (to be added)

---

## Verififcation 

Log onto CloudGuard native and wait for the initial sync process to be completed. 


  
![header image](img/cg.png)  
