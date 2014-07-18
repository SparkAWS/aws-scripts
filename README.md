aws-scripts
===========

Usage
=====
Usage: awsserver start|stop|status|ssh [username]

- `awsserver start` starts the server
- `awsserver stop` stops the server
- `awsserver status` check is server is running
- `awsserver ssh <username>` ssh into your server


Operate an instance in your AWS VPC with pre-defined launch configuration and attach a public IP address.
To ssh to the instance use "awsserver ssh" - this assumes that you have already set up your keys.


Dependencies
====
Assuming you already set up your AWS account, you will also need the following:
- jq
- AWS command-line client
- Autoscaling group setup
- Elastic IP

Configuration
====
You can run conf/awsserver.conf to setup environment variables. Set ASG and EIP in this config file:
- `export AWS_SERVER_ASG=YOUR_ASG_NAME`
- `export AWS_SERVER_EIP=YOUR_IP_ADDRESS`
