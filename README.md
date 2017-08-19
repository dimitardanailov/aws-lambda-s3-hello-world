# Cloud Conf Varna - Cloud application with AWS lambda functions 

## Presentation, Screen Record and Repo

- [Google Drive: Cloud Conf Varna - Cloud application with AWS lambda functions ](https://docs.google.com/presentation/d/1STeF6diIrMsSLTgdyNmyjno7cwbjsoYGtbof6svzvB4/edit#slide=id.g24ed2c6bca_0_9)
- [Slideshare](https://www.slideshare.net/dimityrdanailov/cloud-conf-varna-cloud-application-with-aws-lambda-functions)
- [Youtube - Cloud Conf Varna - Cloud Application with AWS Lambda functions](https://www.youtube.com/watch?v=z6mS1DgL7dY)
- [Github: AWS Lambda and S3](https://github.com/dimitardanailov/aws-lambda-s3-hello-world)

## Materials

- [15 Top Paying IT Certifications In 2016: AWS Certified Solutions Architect Leads At $125K](https://www.forbes.com/sites/louiscolumbus/2016/02/21/15-top-paying-it-certifications-in-2016-aws-certified-solutions-architect-leads-at-125k/#49f4d3347978)
- [Configuring the AWS CLI](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html#cli-quick-configuration)
- [AWS December 2015 Webinar Series - Build Mobile Backends with AWS Lambda](https://www.youtube.com/watch?v=7RYApg4Wd8M )
- [Build Mobile Backends with AWS Lambda - Architecture Diagram](https://s3.amazonaws.com/awslambda-reference-architectures/mobile-backend/lambda-refarch-mobilebackend.pdf)

## Commands

#### `aws`

[aws s3: mb command](http://docs.aws.amazon.com/cli/latest/reference/s3/mb.html)

The following `mb` command creates a S3 bucket
```bash
aws s3 mb s3://cloud-conf-varna-lambda-lab
aws s3 mb s3://cloud-conf-varna-lambda-lab --region eu-central-1
```

[aws s3: ls command](http://docs.aws.amazon.com/cli/latest/reference/s3/ls.html)

List S3 objects and common prefixes under a prefix or all S3 buckets.

```bash
aws s3 ls s3://cloud-conf-varna-lambda-lab
```

[aws s3: cp command](http://docs.aws.amazon.com/cli/latest/reference/s3/cp.html)

Copies a local file or S3 object to another location locally or in S3

```bash
aws s3 cp sample.csv s3://cloud-conf-varna-lambda-lab
```

[aws s3: rm command](http://docs.aws.amazon.com/cli/latest/reference/s3/rm.html)

Deletes an S3 object

```
aws s3 rm s3://cloud-conf-varna-lambda-lab
```

[aws s3: rb command](http://docs.aws.amazon.com/cli/latest/reference/s3/rb.html)

Deletes an empty S3 bucket. A bucket must be completely empty of objects and versioned objects before it can be deleted.

```
aws s3 rb s3://cloud-conf-varna-lambda-lab
```

[aws lamba: update-function-code command](http://docs.aws.amazon.com/cli/latest/reference/lambda/update-function-code.html)

Updates the code for the specified Lambda function. This operation must only be used on an existing Lambda function and cannot be used to update the function configuration.

```bash
aws lambda update-function-code --zip-file=fileb://csv_parse.zip --function_name cloud-conf-varna-s3-hello-world --region eu-central-1
```

[aws lamba: update-function-configuration](http://docs.aws.amazon.com/cli/latest/reference/lambda/update-function-configuration.html)

```bash
aws lambda update-function-configuration --function-name cloud-conf-varna-s3-hello-world --handler csv_read.handler --region eu-central-1
```
