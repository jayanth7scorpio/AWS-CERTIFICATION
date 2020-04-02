#AWS Solution Architect Associate
##AWS S3 Buckets
- are **Private** by default
    - Give Permissions and Make Public (individual files)
    
- Versioning
    - Go to Properties and enable Versioning
        - Enable
        - Suspend (no turn off)
    - Want to upload new version of file?
    - You want to keep the older version as well
    - keep track
    - If you upload a new version of an existing file - it does not inherit the same properties as previous one
    - If you upload a file without versioning turned on - your version is null
    
- Encryption
    - Server side Encryption
    - Properties -> Default Encryption (choose Algo option)
    - can do for individual files and S3 Bucket profiles

- LifeCycle Policies
    
##AWS CLI
- aws s3 ls
- aws s3 ls <bucket_name>
- Downloading Files from S3 Bucket
    - aws s3 cp s3://<bucket_name>/<folder>/<file_name> ~/Desktop/<file_name>
- Uploading file to S3 Bucket
    - aws s3 cp ~/Desktop/<file_name> s3://<bucket_name>/<folder>/<file_name>
- PreSigned URL
    - are for temporary access
    - you want to give temp access to someone
    - it is a URL which is signed with your credentials
    - aws s3 presign s3://<bucket_name>/<file_name> --expires-in 300   
    