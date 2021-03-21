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

### Python Script (Work in Progress))

You can use the python script [onboard_oc_1.py](onboard_oc_1.py) to onboard or remove an OpenShift cluster to and from CloudGuard.

```bash 
# Install requirements
pip3 install -r requirements.txt
# Execute script
python3 onboard_oc_1.py onboard

```

For cluster onboarding you will need to provide:

1. Your Cluster Name (e.g. my_cluster)
2. Namespace (e.g. checkpoint)
3. CloudGuard API Key (you can export environment variable CHKP_CLOUDGUARD_ID and script will detect it)
4. CloudGUard API Secret (you can export environment variable CHKP_CLOUDGUARD_SECRET and script will detect it)


For cluster removal you will need to provide:

1. The path to the yaml file that was generated during onboarding. The script will try to find a yaml file in the current directory.
2. CloudGuard API Key (Alternatively, can export environment variable CHKP_CLOUDGUARD_ID and the script will detect it)
3. CloudGUard API Secret (you can also export environment. variable CHKP_CLOUDGUARD_SECRET and the script will detect it.)

---

## Verififcation 

Log onto CloudGuard native and wait for the initial sync process to be completed. 


  
![header image](img/cg.png)  
