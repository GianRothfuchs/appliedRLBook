# Connect from local machine to GC (Google Cloud)
## first time share 
0. get yourself a [username]
1. create rsa key: 
    * enter2console: ssh-keygen -t rsa -f ~/.ssh/[nameofkey] -C [username] 
    *  ... and provide password
2. show key cd to key & enter2console: vi [nameofkey]
3. got to VM settings on GC and got to ssh section
4. go to VPC networks: set the external ip of VM to be static  
5. note down the statidc Ip for later use = [ipfromgooglecloudserviceVM]

## Add Firewall Rule
Change the following entries:
 - Target: all network instances
 - IP Range set to: 0.0.0.0/0
 - enable tcp equal to: 8888
 Hit 'Save'

## Connect 
### Connect from local
enter2console: ssh -i gc_rsa [username]@[ipfromgooglecloudserviceVM]

### Run online Hit SSH button on VM Overview

## Run Jupyter Notebook
 - enter2console: jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser &
 - Note token
 - go to browser: input [ipfromgooglecloudserviceVM]:8888 to browser 
 


