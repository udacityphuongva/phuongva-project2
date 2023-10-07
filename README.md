# CD12352 - Infrastructure as Code Project Solution
# [Phuongva]

## Project Scenario
Your company is creating an Instagram clone called Udagram, and the requirement is to deploy this new application to the AWS infrastructure using Infrastructure as Code.

You have been tasked with provisioning the required infrastructure and deploying a dummy application, along with the necessary supporting software.

Since the underlying network infrastructure will be maintained by a separate team, you must create independent stacks for the network infrastructure and the application itself.

Infrastructure spin up and tear down needs to be automated so that each team can create and discard testing environments on demand.

## Solution
Network resources: VPC, subnets, Internet Gateway, NAT Gateways

EC2 resources: Autoscaling group with EC2 instances, Load Balancer, Security Groups

Static Content: S3 bucket

# Usage:
Deploy:./run.sh deploy us-east-1 udagram-infra udagram.yml udagram-parameters.json

Delete:./run.sh delete us-east-1 udagram-infra

LoadBanlancerEndpoint:  
http://udagra-WebAp-bf46wTOgODbh-867598092.us-east-1.elb.amazonaws.com