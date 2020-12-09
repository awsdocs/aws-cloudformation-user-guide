# Uploading local artifacts to an S3 bucket<a name="using-cfn-cli-package"></a>

For some resource properties that require an Amazon S3 location \(a bucket name and filename\), you can specify local references instead\. For example, you might specify the S3 location of your AWS Lambda function's source code or an Amazon API Gateway REST API's OpenAPI \(formerly Swagger\) file\. Instead of manually uploading the files to an S3 bucket and then adding the location to your template, you can specify local references, called local artifacts, in your template and then use the `package` command to quickly upload them\. A local artifact is a path to a file or folder that the `package` command uploads to Amazon S3\. For example, an artifact can be a local path to your AWS Lambda function's source code or an Amazon API Gateway REST API's OpenAPI file\.

If you specify a file, the command directly uploads it to the S3 bucket\. After uploading the artifacts, the command returns a copy of your template, replacing references to local artifacts with the S3 location where the command uploaded the artifacts\. Then, you can use the returned template to create or update a stack\.

If you specify a folder, the command creates a \.zip file for the folder, and then uploads the \.zip file\. If you don’t specify a path, the command creates a \.zip file for the working directory, and uploads it\. You can specify an absolute or relative path, where the relative path is relative to your template’s location\.

You can use local artifacts only for resource properties that the `package` command supports\. For more information about this command and a list of the supported resource properties, see the `aws cloudformation package` command in the [AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/index.html)\.

The following template specifies the local artifact for a Lambda function's source code\. The source code is stored in the user's `/home/user/code/lambdafunction` folder\.

**Original template**

```
AWSTemplateFormatVersion: '2010-09-09'
Transform: 'AWS::Serverless-2016-10-31'
Resources:
  MyFunction:
    Type: 'AWS::Serverless::Function'
    Properties:
      Handler: index.handler
      Runtime: nodejs8.10
      CodeUri: /home/user/code/lambdafunction
```

The following command creates a \.zip file containing the function's source code folder, and then uploads the \.zip file to the root folder of the `my-bucket` bucket\.

**Package command**

```
aws cloudformation package --template /path_to_template/template.json --s3-bucket mybucket --output json > packaged-template.json
```

The command saves the template that it generates to the path specified by the `--output` option\. The command replaces the artifact with the S3 location, as shown in the following example:

**Resulting template**

```
AWSTemplateFormatVersion: '2010-09-09'
Transform: 'AWS::Serverless-2016-10-31'
Resources:
  MyFunction:
    Type: 'AWS::Serverless::Function'
    Properties:
      Handler: index.handler
      Runtime: nodejs8.10
      CodeUri: s3://mybucket/lambdafunction.zip
```