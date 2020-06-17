# Coding challenge for DevOps Engineer

## Purpose
Aim of these tests are to,

- evaluate your DevOps engineering capability
- benchmark your technical experience and maturity
- understand how you design and implement your solution

## How you will be judged
You will be scored on,

- solution design - structure and quality (20%)
- infrastructure provisioning and configuration (40%)
- continuous integration and continuous delivery (20%)
- use of source control and documentation (20%)

## Instructions

Develop Infrastructure as a code for following two scenorios,

## Challenge - Bootstrap Jenkins Server

You are suppose to create a set of automation scripts to setup a Jenkins server,

### Requirements
- An Amazon EC2 instance (`t2.micro`) using Amazon Linux
- Elastic IP and Detachable EBS volumes (one for OS, another for Jenkins Home)
- Install Jenkins on the server and ensure Jenkins home is set to attached EBS 
- Secure your server using EC2 security groups and map a CNAME on IP address
- Install Nginx web server and add Let's Encrypt SSL Certificate for CNAME
- Create a secure Amazon S3 Bucket to store Jenkins build artificats
- Assigne IAM role to Jenkins EC2 Instance to upload and download the build artificats
- Install necessery Jenkins Plugin to make the Jenkins setup functional (S3 Plugin, Pipeline Plugin, etc.)

For testing your code, please create a new AWS account to avial [free tier](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc) which gives access to a range of AWS resources for a 12 months period.

## Challenge - Continuous Delivery Workflow

You are suppose to create a Jenkins Continuous Delivery Workflow using [`Docker`](https://jenkins.io/doc/book/pipeline/docker/) and [`Jenkinsfile`](https://jenkins.io/doc/book/pipeline/jenkinsfile/) ,

- Create another S3 bucket for hosting the static website (you can create this manually)
- Clone the Bootstrap Git repository using SSH endpoint (`git@github.com:twbs/bootstrap.git`)
- Install Ruby 2.0, Ruby Gem, Jekyll, etc. as container
- Add the build step Execute shell command `jekyll build` in root directory
- Build step will create a new folder `_gh_pages`
- Drop a `version.txt` file in the `_gh_pages` which includes jenkins job name and build number
- Add a Post-build action `Publish artifacts to S3 Bucket` 
- Create a Amazon S3 Bucket, enable static website hosting and add appropriate bucket policy
- `Publish artifacts to S3 Bucket` should copy content of the `_gh_pages` to your S3 bucket
- Run the build job and you should see a Bootstrap static website similar to [this](http://getbootstrap.com/) on your S3 bucket URL


## Finally
Once you finished the test, either send us a pull request or URL for your Github repository.
