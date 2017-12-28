# AWS::Lambda::Permission<a name="aws-resource-lambda-permission"></a>

The `AWS::Lambda::Permission` resource associates a policy statement with a specific AWS Lambda \(Lambda\) function's access policy\. The function policy grants a specific AWS service or application permission to invoke the function\. For more information, see [AddPermission](http://docs.aws.amazon.com/lambda/latest/dg/API_AddPermission.html) in the *AWS Lambda Developer Guide*\.


+ [Syntax](#aws-resource-lambda-permission-syntax)
+ [Properties](#w3ab2c21c10d810b9)
+ [Example](#w3ab2c21c10d810c11)

## Syntax<a name="aws-resource-lambda-permission-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-permission-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::Permission",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-action)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-eventsourcetoken)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-functionname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-principal)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-sourceaccount)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-sourcearn)" : String
  }
}
```

### YAML<a name="aws-resource-lambda-permission-syntax.yaml"></a>

```
Type: "AWS::Lambda::Permission"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-action): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-eventsourcetoken): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-functionname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-principal): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-sourceaccount): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-lambda-permission-sourcearn): String
```

## Properties<a name="w3ab2c21c10d810b9"></a>

For more information and current valid values, see [AddPermission](http://docs.aws.amazon.com/lambda/latest/dg/API_AddPermission.html) in the *AWS Lambda Developer Guide*\.

`Action`  
The Lambda actions that you want to allow in this statement\. For example, you can specify `lambda:CreateFunction` to specify a certain action, or use a wildcard \(`lambda:*`\) to grant permission to all Lambda actions\. For a list of actions, see [Actions and Condition Context Keys for AWS Lambda](http://docs.aws.amazon.com/IAM/latest/UserGuide/list_lambda.html) in the *IAM User Guide*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`EventSourceToken`  
A unique token that must be supplied by the principal invoking the function\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`FunctionName`  
The name \(physical ID\), Amazon Resource Name \(ARN\), or alias ARN of the Lambda function that you want to associate with this statement\. Lambda adds this statement to the function's access policy\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Principal`  
The entity for which you are granting permission to invoke the Lambda function\. This entity can be any valid AWS service principal, such as `s3.amazonaws.com` or `sns.amazonaws.com`, or, if you are granting cross\-account permission, an AWS account ID\. For example, you might want to allow a custom application in another AWS account to push events to Lambda by invoking your function\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`SourceAccount`  
The AWS account ID \(without hyphens\) of the source owner\. For example, if you specify an S3 bucket in the `SourceArn` property, this value is the bucket owner's account ID\. You can use this property to ensure that all source principals are owned by a specific account\.  
This property is not supported by all event sources\. For more information, see the `SourceAccount` parameter for the [AddPermission](http://docs.aws.amazon.com/lambda/latest/dg/API_AddPermission.html) action in the *AWS Lambda Developer Guide*\.
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`SourceArn`  
The ARN of a resource that is invoking your function\. When granting Amazon Simple Storage Service \(Amazon S3\) permission to invoke your function, specify this property with the bucket ARN as its value\. This ensures that events generated only from the specified bucket, not just any bucket from any AWS account that creates a mapping to your function, can invoke the function\.  
This property is not supported by all event sources\. For more information, see the `SourceArn` parameter for the [AddPermission](http://docs.aws.amazon.com/lambda/latest/dg/API_AddPermission.html) action in the *AWS Lambda Developer Guide*\.
*Required: *No  
*Type*: String  
*Update requires*: Replacement

## Example<a name="w3ab2c21c10d810c11"></a>

The following example grants an S3 bucket permission to invoke a Lambda function\.

### JSON<a name="aws-resource-lambda-permission-example.json"></a>

```
"LambdaInvokePermission": {
	"Type": "AWS::Lambda::Permission",
	"Properties": {
		"FunctionName": {
			"Fn::GetAtt": [
				"MyLambdaFunction",
				"Arn"
			]
		},
		"Action": "lambda:InvokeFunction",
		"Principal": "s3.amazonaws.com",
		"SourceAccount": {
			"Ref": "AWS::AccountId"
		},
		"SourceArn": {
			"Fn::GetAtt": [
				"MyBucket",
				"Arn"
			]
		}
	}
}
```

### YAML<a name="aws-resource-lambda-permission-example.yaml"></a>

```
LambdaInvokePermission:
  Type: 'AWS::Lambda::Permission'
  Properties:
    FunctionName: !GetAtt 
      - MyLambdaFunction
      - Arn
    Action: 'lambda:InvokeFunction'
    Principal: s3.amazonaws.com
    SourceAccount: !Ref 'AWS::AccountId'
    SourceArn: !GetAtt 
      - MyBucket
      - Arn
```