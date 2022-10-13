# BOTO3
AWS SDK for python to create , configure , manage AWS services like Ec2 , S3

import boto3
\n s3_boto = boto3.client('s3')
response= s3_boto.get_object(Bucket = '<Bucketname>' , Key-'<Keyname>')
print(response['Body'].read().decode())
