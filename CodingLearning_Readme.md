# BOTO3
AWS SDK for python to create , configure , manage AWS services like Ec2 , S3

import boto3
s3_boto = boto3.client('s3')
response= s3_boto.get_object(Bucket = '<Bucketname>' , Key-'<Keyname>')
print(response['Body'].read().decode())
  
  
#configparser
  ##This module provides ConfigParser class which implements basic configuration language having a structure similar to what is found in windows ini file
  Class = ConfigParser()
  Functions:
  1. read_string()
  2. get()
  
This module has class ConfigParser()
  config = configparser.ConfigParser()
  config.read_string()
  config.get
  

