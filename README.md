# workshop2023

## How to run pre-packaged teck stacks:
Quick links: List of tech stacks https://hub.docker.com/u/ilab247 

Cloud Guru offers sand boxes and cloud servers for running the above docker images (tech stacks):

###### 1.	Create your own machine (Only for first time)

1. Login to acloud.guru or navigate to link ```https://learn.acloud.guru/cloud-playground/cloud-servers```
2. Create new server – options: Distribution = Cloud Native Kubernetes, Zone =North America (or any other), Size = Large, Tag = AIML (or any other name).  Click create server.  (This will take 2-3 mins)
3. Open terminal – username <cloud_user>, password <listed in the page>  change it to desired name (during first login)
4. Congratulations.  You have a sandbox ready for running our tech stacks.
  Just run below two commands to create our workspaces folder.
  ```mkdir /home/cloud_user/workspaces```
	
  ```chmod +777 /home/cloud_user/workspaces```

###### 2.	Run our prepackaged aiml tech stacks:

1. ```docker run -it --network=host -v /home/cloud_user/workspaces:/workspaces ilab247/aimlstack:0.03``` (replace aimlstack:0.01 with desired stack name)
	
2. This above will automatically runs vs code server. if not run it manually.
	a. Change user :  ```su - ilab247user```
	b. Change working directory: ```cd /workspaces```
	c. Run Code-Server : ```code-server --bind-addr 0.0.0.0:8005 --auth none --user-data-dir /home/ilab247user/data --extensions-dir /home/ilab247user/extensionsCache```
	d. Run Jupyter Lab : ```jupyter lab --ip=0.0.0.0 --port=8002```
	
3. Navigate to the URL with port mentioned to access your VS Code environment
