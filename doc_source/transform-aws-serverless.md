# AWS::Serverless Transform<a name="transform-aws-serverless"></a>

Use a transform to simplify template authoring for serverless applications\. For example, the following template uses AWS SAM syntax to simplify the declaration of a Lambda function and its execution role\.

```
Transform: AWS::Serverless-2016-10-31
Resources:
  MyServerlessFunctionLogicalID:
    Type: AWS::Serverless::Function
    Properties:
      Handler: index.handler
      Runtime: nodejs4.3
      CodeUri: 's3://testBucket/mySourceCode.zip'
```

When the template is submitted, AWS CloudFormation expands the AWS SAM syntax, as defined by the transform\. The processed template expands the `AWS::Serverless::Function` resource, declaring an Lambda function and an execution role\.

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
        "Runtime": "nodejs4.3"
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

AWS CloudFormation uses the processed template to create or update a stack\. If you don't specify a transform value, AWS CloudFormation doesn't process your template, and the AWS SAM syntax fails template validation\.

## Syntax<a name="w3ab2c17c15c23c21c13"></a>

The value for the transform declaration must be a literal string\. You cannot use a parameter or function to specify a transform value\. The following snippet is an example of a transform declaration:

### JSON<a name="transform-section-structure-syntax.json"></a>

```
"Transform" : "AWS::Serverless-2016-10-31"
```

### YAML<a name="transform-section-structure-syntax.yaml"></a>

```
Transform: "AWS::Serverless-2016-10-31"
```

## Template Stage<a name="transform-section-structure-template-stage"></a>

The stage of a template indicates whether the template is the original user\-submitted template or one where AWS CloudFormation has processed the transforms\. The original template is the one that users submitted to create or update the stack\. The processed template is the template AWS CloudFormation used to create or update the stack after processing the transform\(s\)\. Use the processed template for troubleshooting stack issues\. If a stack doesn't include transforms, the original and processed templates are identical\.

You can use the AWS CloudFormation [console](cfn-console-view-stack-data-resources.md) or [AWS CLI](using-cfn-get-template.md) to see the stage of a stack's template\.

## Working with Stacks That Contain Transforms<a name="transform-section-structure-change-set"></a>

To create or update a stack with transforms, you must create a [change set](cfn-console-create-stacks-changesets.md), and then execute it\. A change set describes the actions AWS CloudFormation will take based on the processed template\. During processing, AWS CloudFormation translates AWS SAM syntax into syntax that is defined by the transform\. Processing can add multiples resources that you might not be aware of\. For example, the specialized `AWS::Serverless::Function` resource adds an AWS Identity and Access Management \(IAM\) execution role and a Lambda function\.

To ensure that you're aware of all of the changes introduced by transforms, AWS CloudFormation requires you to use change sets\. After you review the change set, execute it to apply the changes or create another one\.

**Note**  
A transform can add IAM resources to your template\. For these resources, AWS CloudFormation requires you to [acknowledge their capabilities](using-iam-template.md#using-iam-capabilities)\. Because AWS CloudFormation can't know which resources are added before processing your template, you might need to acknowledge IAM capabilities when you create the change set, depending on whether your transforms contain IAM resources\. That way, when you execute the change set, AWS CloudFormation has the necessary capabilities when creating IAM resources\.

If you use the AWS CLI, you can use the `package` and `deploy` commands to reduce the number of steps for launching stacks with transforms\. For more information, see [Deploying Lambda\-based Applications](http://docs.aws.amazon.com/lambda/latest/dg/deploying-lambda-apps.html) in the *AWS Lambda Developer Guide*\.