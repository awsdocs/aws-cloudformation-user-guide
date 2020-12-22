# AWS::Lambda::Function Code<a name="aws-properties-lambda-function-code"></a>

The deployment package for a Lambda function\. To deploy a function defined as a container image, you specify the location of a container image in the Amazon ECR registry\. For a \.zip file deployment package, you can specify the location of an object in Amazon S3\. For Node\.js and Python functions, you can specify the function code inline in the template\.

Changes to a deployment package in Amazon S3 are not detected automatically during stack updates\. To update the function code, change the object key or version in the template\.

## Syntax<a name="aws-properties-lambda-function-code-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-function-code-syntax.json"></a>

```
{
  "[ImageUri](#cfn-lambda-function-code-imageuri)" : String,
  "[S3Bucket](#cfn-lambda-function-code-s3bucket)" : String,
  "[S3Key](#cfn-lambda-function-code-s3key)" : String,
  "[S3ObjectVersion](#cfn-lambda-function-code-s3objectversion)" : String,
  "[ZipFile](#cfn-lambda-function-code-zipfile)" : String
}
```

### YAML<a name="aws-properties-lambda-function-code-syntax.yaml"></a>

```
  [ImageUri](#cfn-lambda-function-code-imageuri): String
  [S3Bucket](#cfn-lambda-function-code-s3bucket): String
  [S3Key](#cfn-lambda-function-code-s3key): String
  [S3ObjectVersion](#cfn-lambda-function-code-s3objectversion): String
  [ZipFile](#cfn-lambda-function-code-zipfile): String
```

## Properties<a name="aws-properties-lambda-function-code-properties"></a>

`ImageUri`  <a name="cfn-lambda-function-code-imageuri"></a>
URI of a container image in the Amazon ECR registry\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Bucket`  <a name="cfn-lambda-function-code-s3bucket"></a>
An Amazon S3 bucket in the same AWS Region as your function\. The bucket can be in a different AWS account\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `^[0-9A-Za-z\.\-_]*(?<!\.)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Key`  <a name="cfn-lambda-function-code-s3key"></a>
The Amazon S3 key of the deployment package\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3ObjectVersion`  <a name="cfn-lambda-function-code-s3objectversion"></a>
For versioned objects, the version of the deployment package object to use\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ZipFile`  <a name="cfn-lambda-function-code-zipfile"></a>
\(Node\.js and Python\) The source code of your Lambda function\. If you include your function source inline with this parameter, AWS CloudFormation places it in a file named `index` and zips it to create a [deployment package](https://docs.aws.amazon.com/lambda/latest/dg/deployment-package-v2.html)\. For the `Handler` property, the first part of the handler identifier must be `index`\. For example, `index.handler`\.  
Your source code can contain up to 4096 characters\. For JSON, you must escape quotes and special characters such as newline \(`\n`\) with a backslash\.  
If you specify a function that interacts with an AWS CloudFormation custom resource, you don't have to write your own functions to send responses to the custom resource that invoked the function\. AWS CloudFormation provides a response module \([cfn\-response](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-lambda-function-code-cfnresponsemodule.html)\) that simplifies sending responses\. See [Using AWS Lambda with AWS CloudFormation](https://docs.aws.amazon.com/lambda/latest/dg/services-cloudformation.html) for details\.   
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-function-code--examples"></a>

### Inline Function<a name="aws-properties-lambda-function-code--examples--Inline_Function"></a>

Inline Node\.js function that uses the cfn\-response library\.

#### YAML<a name="aws-properties-lambda-function-code--examples--Inline_Function--yaml"></a>

```
      Code:
        ZipFile: |
          var aws = require('aws-sdk')
          var response = require('cfn-response')
          exports.handler = function(event, context) {
              console.log("REQUEST RECEIVED:\n" + JSON.stringify(event))
              // For Delete requests, immediately send a SUCCESS response.
              if (event.RequestType == "Delete") {
                  response.send(event, context, "SUCCESS")
                  return
              }
              var responseStatus = "FAILED"
              var responseData = {}
              var functionName = event.ResourceProperties.FunctionName
              var lambda = new aws.Lambda()
              lambda.invoke({ FunctionName: functionName }, function(err, invokeResult) {
                  if (err) {
                      responseData = {Error: "Invoke call failed"}
                      console.log(responseData.Error + ":\n", err)
                  }
                  else responseStatus = "SUCCESS"
                  response.send(event, context, responseStatus, responseData)
              })
          }
```