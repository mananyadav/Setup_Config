## Account Configure 
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


## Copy Commands
# To copy all JSON Reference data to same location:
aws s3 cp . s3://manan-de-on-youtube-raw-dev/youtube/raw_statistics_reference_data/ --recursive --exclude "*" --include "*.json"

# To copy all data files to its own location, following Hive-style patterns:
aws s3 cp CAvideos.csv s3://manan-de-on-youtube-raw-dev/youtube/raw_statistics/region=ca/
