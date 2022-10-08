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
  aws_bucket_name: 'xxx' ## required, s3 bucket
  aws_bucket_dir: 'assets/image' ## dir in s3, default is empty
  aws_cloudfront_distribution_id: '' ## cloudfront_distribution_id, if set, will create invalidation (make sure your aws account has invalidation permissions)
  source: 'name1.txt'  ## required
  acl: private ## s3 acl, default is private. see https://docs.aws.amazon.com/en_us/AmazonS3/latest/userguide/acl-overview.html
  compare: true  ## default: true, only upload different files
  filename: 'name2.txt' ## rename, default is empty
```
