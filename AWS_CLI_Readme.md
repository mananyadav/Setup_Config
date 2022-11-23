# Account Configure 
       To create a new configuration:

          $ aws configure
          AWS Access Key ID [None]: accesskey
          AWS Secret Access Key [None]: secretkey
          Default region name [None]: us-west-2
          Default output format [None]:

       To update just the region name:

          $ aws configure
          AWS Access Key ID [****]:
          AWS Secret Access Key [****]:
          Default region name [us-west-1]: us-west-2
          Default output format [None]:


# Copy Commands
## To copy all JSON Reference data to same location:
aws s3 cp . s3://manan-de-on-youtube-raw-dev/youtube/raw_statistics_reference_data/ --recursive --exclude "*" --include "*.json"

## To copy all data files to its own location, following Hive-style patterns:
aws s3 cp CAvideos.csv s3://manan-de-on-youtube-raw-dev/youtube/raw_statistics/region=ca/

## scp cpmmand 
scp -i /Users/ymanan/Documents/PersonalDocuments/CertificationLearning//DemoKeyPair.pem hadoop@ec2-13-234-29-27.ap-south-1.compute.amazonaws.com:/usr/lib/spark/jars/spark-core_2.11-2.4.8-amzn-2.jar /Users/ymanan/IdeaProjects/jarRep/EMRSpark/

## ssh command 
ssh -i /Users/ymanan/Documents/PersonalDocuments/CertificationLearning//DemoKeyPair.pem hadoop@ec2-13-234-29-27.ap-south-1.compute.amazonaws.com


#  DATASYNC
## Execute datasync with filtering enabled 
aws datasync start-task-execution --task-arn 'arn:aws:datasync:ap-south-1:677597669914:task/task-0d0f356d1ea2a708a' --includes FilterType=SIMPLE_PATTERN,Value='/sd/*|/dpYear=2022/dpMonth=11/dpDay=5'

# EMR Serverless

# Maven 
## locally push the jar in .m2 local repo cache
mvn install:install-file \
-DgroupId=groupEMRSpark \
-DartifactId=artifactEMRSpark \
-Dpackaging=jar \
-Dversion=1.0.1B \
-Dfile=spark-core_2.12-2.4.4.jar \
-DgeneratePom=true

