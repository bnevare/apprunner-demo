# App Runner Demo

``` add my own banner``` 

## What is AWS App Runner?
[AWS App Runner](https://aws.amazon.com/apprunner/) is a fully managed service that makes it easy for developers to quickly deploy containerized website applications and APIs at scale.

This is an example web service for AWS App Runner. You can use this repo to deploy the web application two ways.


## Deploy to App Runner

### Option 1: From Source

1. Fork this Repository:

	- Press the Fork button in the upper right. This will create an exact copy of the repository (and all of its branches) under your own username.

2. Open the AWS Console and browse to the [AWS App Runner service](https://console.aws.amazon.com/apprunner/home?region=us-east-1#/services).
      - Select 	`"Create a service"`
      -  Repository Type: `Source code repository`
      -  Connect To Github:
	 		
			 connection name example: apprunner-conn
			 repository: apprunner-demo
			 branch: main
      
	 - Deployment settings: `Manual`
	 - Build settings:
	
		**Option 1:** `Use a configuration file`. App Runner looks for the `apprunner.yaml` in your source repository.
		
		**Option 2:**  Manually type the web application configurations.
		
		    Runtime: Nodejs12
		    Build command: npm install
		    Start command: node node.js	
		    Port: 3000
	
	- Service name:`simple-webapp`
	- Everything else can be left as default. Select `"Create & deploy"`

### Option 2: From container

	
		
		
