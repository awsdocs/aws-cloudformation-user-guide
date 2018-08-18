# AWS::ApiGateway::Account<a name="aws-resource-apigateway-account"></a>

The `AWS::ApiGateway::Account` resource specifies the AWS Identity and Access Management \(IAM\) role that Amazon API Gateway \(API Gateway\) uses to write API logs to Amazon CloudWatch Logs \(CloudWatch Logs\)\.

**Important**  
If an API Gateway resource has never been created in your AWS account, you must add a dependency on another API Gateway resource, such as an [AWS::ApiGateway::RestApi](aws-resource-apigateway-restapi.md) or [AWS::ApiGateway::ApiKey](aws-resource-apigateway-apikey.md) resource\.  
If an API Gateway resource has been created in your AWS account, no dependency is required \(even if the resource was deleted\)\.

**Topics**
+ [Syntax](#aws-resource-apigateway-account-syntax)
+ [Properties](#aws-resource-apigateway-account-properties)
+ [Return Value](#aws-resource-apigateway-account-returnvalues)
+ [Example](#aws-resource-apigateway-account-examples)

## Syntax<a name="aws-resource-apigateway-account-syntax"></a>

The syntax for declaring this resource:

### JSON<a name="aws-resource-apigateway-account-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Account",
  "Properties" : {
    "[CloudWatchRoleArn](#cfn-apigateway-account-cloudwatchrolearn)": String
  }
}
```

### YAML<a name="aws-resource-apigateway-account-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::Account"
Properties: 
  [CloudWatchRoleArn](#cfn-apigateway-account-cloudwatchrolearn): String
```

## Properties<a name="aws-resource-apigateway-account-properties"></a>

`CloudWatchRoleArn`  <a name="cfn-apigateway-account-cloudwatchrolearn"></a>
The Amazon Resource Name \(ARN\) of an IAM role that has write access to CloudWatch Logs in your account\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="aws-resource-apigateway-account-returnvalues"></a>

### Ref<a name="w3ab2c21c10c13c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ID of the resource, such as `mysta-accou-01234b567890example`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-apigateway-account-examples"></a>

The following example creates an IAM role that API Gateway can assume to push logs to CloudWatch Logs\. The example associates the role with the `AWS::ApiGateway::Account` resource\.

### JSON<a name="aws-resource-apigateway-account-examples.json"></a>

```
"CloudWatchRole": {
  "Type": "AWS::IAM::Role",
  "Properties": {
    "AssumeRolePolicyDocument": {
      "Version": "2012-10-17",
      "Statement": [{
        "Effect": "Allow",
        "Principal": { "Service": [ "apigateway.amazonaws.com" ] },
        "Action": "sts:AssumeRole"
      }]
    },
    "Path": "/",
    "ManagedPolicyArns": ["arn:aws:iam::aws:policy/service-role/AmazonAPIGatewayPushToCloudWatchLogs"]
  }
},
"Account": {
  "Type": "AWS::ApiGateway::Account",
  "Properties": {
    "CloudWatchRoleArn": { "Fn::GetAtt": ["CloudWatchRole", "Arn"] }
  }
}
```

### YAML<a name="aws-resource-apigateway-account-examples.yaml"></a>

```
CloudWatchRole: 
 Type: "AWS::IAM::Role"
 Properties: 
  AssumeRolePolicyDocument: 
   Version: "2012-10-17"
   Statement: 
    - Effect: Allow
      Principal: 
       Service: 
        - "apigateway.amazonaws.com"
      Action: "sts:AssumeRole"
  Path: "/"
  ManagedPolicyArns: 
   - "arn:aws:iam::aws:policy/service-role/AmazonAPIGatewayPushToCloudWatchLogs"
Account: 
 Type: "AWS::ApiGateway::Account"
 Properties: 
  CloudWatchRoleArn: 
   "Fn::GetAtt": 
    - CloudWatchRole
    - Arn
```