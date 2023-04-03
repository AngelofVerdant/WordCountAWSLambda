# WordCountAWSLambda
A Lambda Function that counts number of words in an uploaded Text File 

This is a Python code that counts the number of words in a file stored in an Amazon S3 bucket and then publishes the word count to an Amazon SNS topic.

## Prerequisites
- AWS account with required permissions to create an S3 bucket, SNS topic, and IAM roles.
- Python 3.x
- Boto3 library
- AWS CLI configuration with valid access and secret access keys.
- Installation and Configuration
- Clone or download this repository to your local machine.
- Create an S3 bucket in your AWS account and replace the bucket_name variable in the code with the name of your bucket.
- Create an SNS topic in your AWS account and replace the sns_topic_arn variable in the code with the ARN of your SNS topic.
- Ensure that the AWS CLI is configured with valid access and secret access keys.
- Install the Boto3 library by running pip install boto3 in your terminal.
## Usage
- Upload a file to your S3 bucket that you want to count the number of words.
- Create a Lambda function in your AWS account and copy the code into the Lambda function.
- Set the Lambda function's trigger to the S3 bucket's upload events.
- Save and test the Lambda function.
## How it works
The Lambda function is triggered when a file is uploaded to the S3 bucket.
The function extracts the name of the file and retrieves the contents of the file using the s3.get_object() function.
The function then counts the number of words in the file contents and stores the result in the word_count variable.
A message containing the file name and word count is published to the specified SNS topic using the sns.publish() function.
The function returns the word count as the output of the Lambda function.
Conclusion
This code is a simple example of integrating AWS services to perform a specific task. It demonstrates how to count the number of words in
a file stored in S3 and publish the result to an SNS topic. With some modifications, this code can be used as a template for other similar use cases.
