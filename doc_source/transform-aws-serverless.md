# AWS::Serverless transform<a name="transform-aws-serverless"></a>

The `AWS::Serverless` transform, which is a macro hosted by CloudFormation, takes an entire template written in the AWS Serverless Application Model \(AWS SAM\) syntax and transforms and expands it into a compliant CloudFormation template\. For more information about serverless applications and AWS SAM, see [Deploying Lambda\-based applications](https://docs.aws.amazon.com/lambda/latest/dg/deploying-lambda-apps.html) in the *AWS Lambda Developer Guide* and [AWS SAM resource and property reference](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/sam-specification-resources-and-properties.html) in the AWS Serverless Application Model Developer Guide\.

In the following example, the template uses AWS SAM syntax to simplify the declaration of a Lambda function and its execution role\.

```
Transform: AWS::Serverless-2016-10-31
Resources:
  MyServerlessFunctionLogicalID:
    Type: AWS::Serverless::Function
    Properties:
      Handler: index.handler
      Runtime: nodejs18.x
      CodeUri: 's3://testBucket/mySourceCode.zip'
```

When creating a change set from the template, CloudFormation expands the AWS SAM syntax, as defined by the transform\. The processed template expands the `AWS::Serverless::Function` resource, declaring an AWS Lambda function and an execution role\.

```
{
  "Resources": {
    "MyServerlessFunctionLogicalID": {
      "Type": "AWS::Lambda::Function",
      "Properties": {
        "Handler": "index.handler",
        "Code": {
          "S3Bucket": "testBucket",
          "S3Key": "mySourceCode.zip"
        },
        "Role": {
          "Fn::GetAtt": ["FunctionNameRole", "Arn"]
        },
        "Runtime": "nodejs18.x"
      }
    },
    "FunctionNameRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "ManagedPolicyArns": ["arn:aws:iam::aws:policy/service-role/AWSLambdaBasicExecutionRole"],
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [{
            "Action": ["sts:AssumeRole"],
            "Effect": "Allow",
            "Principal": {
              "Service": ["lambda.amazonaws.com"]
            }
          }]
        }
      }
    }
  }
}
```

## Syntax<a name="transform-section-structure-syntax"></a>

The value for the transform declaration must be a literal string\. You can't use a parameter or function to specify a transform value\. The following snippet is an example of a transform declaration:

### JSON<a name="transform-section-structure-syntax.json"></a>

```
"Transform" : "AWS::Serverless-2016-10-31"
```

### YAML<a name="transform-section-structure-syntax.yaml"></a>

```
Transform: "AWS::Serverless-2016-10-31"
```