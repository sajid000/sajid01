## AWS CLI 
---

### create s3 bucket  

```
aws s3api create-bucket \
    --bucket my-bucket \
    --region us-east-1
```


### remove s3 bucket 

`aws s3 rm  s3://<bucket_path>/ --recursive`

### list buckets  

`aws s3api list-buckets`

### list bucket contents

`aws s3 ls /<BUCKET_NAME>/`

### get head object of bucket/key item  

`aws s3api head-object --bucket <BUCKET_NAME> --key <path/to/key>`


### copy s3 bucket  

```  

aws s3 mb s3://[new-bucket]
aws s3 sync s3://[old-bucket] s3://[new-bucket]
aws s3 rb --force s3://[old-bucket]  

```

## DynamoDB 

Delete Table

`aws dynamodb delete-table --table-name <TABLE_NAME>`

Put Item 
```  
aws dynamodb put-item \
    --table-name <TABLE_NAME>  \
    --item \
        '{"unique_key": {"S": "id_field"}, "field1_date": {"S": "2020-01-01"}, "field2_date": {"S": "2022-12-31"}}'
```
