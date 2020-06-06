# Connect form local machine to GC (Google Cloud)
## first time share 
 - create rsa key: 
	enter2console: ssh-keygen -t rsa -f ~/.ssh/<nameofkey> -C <username>
	& password
 - show key cd to key & enter2console: vi <nameofkey>
 - got to VM settings on GC and got to ssh section
 - go to VPC networks: set the external ip of VM to be static 

## Add Firewall Rule
 - Target: all network instances
 - IP Range set to: 0.0.0.0/0
 - enable tcp equal to: 8888

## Connect 
### Connect from local
enter2console: ssh -i gc_rsa <username>@<ipfromgooglecloudserviceVM>

### Run online Hit SSH button on VM Overview

## Run Jupyter Notebook
 - enter2console: jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser &
 - Note token
 - go to browser: input <external ip>:8888 to browser 
 -


