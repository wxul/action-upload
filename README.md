# AWS S3 Sync Action

Sync files to s3

## Inputs

## Example usage

``` yml
uses: surreal-ai/action-upload@master
env:
  AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}  ## AWS_ACCESS_KEY_ID
  AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }} ## AWS_ACCESS_KEY_ID
  AWS_REGION: us-east-1  ## AWS_REGION
with:
  aws_bucket_name: '' ## required, s3 bucket
  aws_bucket_dir: '' ## dir in s3
  source: 'xxxx.txt'  ## required
  acl: private ## s3 acl, default is private. see https://docs.aws.amazon.com/en_us/AmazonS3/latest/userguide/acl-overview.html
  compare: true  ## default: true, only upload different files
```
