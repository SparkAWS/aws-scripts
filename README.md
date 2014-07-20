aws-scripts
===========

This is a script you can use to learn AWS command-line utility. If you want to build tool and have more control in other programming languages, you probably want to use the language specific API. For example, check out: https://github.com/SparkAWS

Usage
=====
Usage: awsserver start|stop|status|ssh [username]

- `awsserver start` starts the server
- `awsserver stop` stops the server
- `awsserver status` check is server is running
- `awsserver ssh <username>` ssh into your server


Operate an instance in your AWS VPC with pre-defined launch configuration and attach a public IP address.
To ssh to the instance use "awsserver ssh" - this assumes that you have already set up your keys.


Prerequisites
====
Assuming you already set up your AWS account, you will also need the following:
- AWS command-line client
- jq

You also need to make sure you have dedicated:
- One Autoscaling group setup
- One Elastic IP

Configuration
====
You can run conf/awsserver.conf to setup environment variables. Set ASG and EIP in this config file:
- `export AWS_SERVER_ASG=YOUR_ASG_NAME`
- `export AWS_SERVER_EIP=YOUR_IP_ADDRESS`
