# Setup Jupyter lab on cloud 9 
1. mkdir delab
2. cd delab
3.  python3 -m venv delab-venv
4.  ls -ltr delab-venv
5.  source delab-venv/bin/activate
6.  pip install jupyterlab
7.  jupyter lab --ip 0.0.0.0 --> this command will start the jupyter lab 
8.  To access it , we have to open the port 8888 on security groups using the myip 
9.  Copy the public DNS, add 8888 on it 
10.  Give the token from cloud9 terminal 
11.  Below commnad can check which python version is used to invoke the jupyter lab 
12.  from platform import python_version
13.  python_version()

# BOTO3
## AWS SDK for python to create , configure , manage AWS services like Ec2 , S3
  import boto3
  s3_boto = boto3.client('s3')
  response= s3_boto.get_object(Bucket = '<Bucketname>' , Key-'<Keyname>')
  print(response['Body'].read().decode())

  
# configparser
  ## This module provides ConfigParser class which implements basic configuration language having a structure similar to what is found in windows ini file
  Class = ConfigParser()
  Functions:
  1. read_string(<string>)
  2. read_dict(<dict>)
  3. read(<filename>)
  2. get()
  
This module has class ConfigParser()
  config = configparser.ConfigParser()
  config.read_string(<string obj>)
  config.get
  
# Library - sys
  When submitting the proram command used : python <script.py> <param1> <param2>
  1. print (sys.argv[1]). --> output: <param1>
  2. print (sys.argv[2]). --> output: <param2>
  

