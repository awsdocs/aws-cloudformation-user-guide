# AWS::ApiGateway::Account<a name="aws-resource-apigateway-account"></a>

The `AWS::ApiGateway::Account` resource specifies the IAM role that Amazon API Gateway uses to write API logs to Amazon CloudWatch Logs\.

**Important**  
If an API Gateway resource has never been created in your AWS account, you must add a dependency on another API Gateway resource, such as an [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html) or [AWS::ApiGateway::ApiKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-apikey.html) resource\.  
If an API Gateway resource has been created in your AWS account, no dependency is required \(even if the resource was deleted\)\.

## Syntax<a name="aws-resource-apigateway-account-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-account-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Account",
  "Properties" : {
      "[CloudWatchRoleArn](#cfn-apigateway-account-cloudwatchrolearn)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-account-syntax.yaml"></a>

```
Type: AWS::ApiGateway::Account
Properties: 
  [CloudWatchRoleArn](#cfn-apigateway-account-cloudwatchrolearn): String
```

## Properties<a name="aws-resource-apigateway-account-properties"></a>

`CloudWatchRoleArn`  <a name="cfn-apigateway-account-cloudwatchrolearn"></a>
The Amazon Resource Name \(ARN\) of an IAM role that has write access to CloudWatch Logs in your account\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-account-return-values"></a>

### Ref<a name="aws-resource-apigateway-account-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the resource, such as `mysta-accou-01234b567890example`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-account--examples"></a>



### Associate account with IAM role<a name="aws-resource-apigateway-account--examples--Associate_account_with_IAM_role"></a>

The following example creates an IAM role that API Gateway can assume to push logs to CloudWatch Logs\. The example associates the role with the `AWS::ApiGateway::Account resource`\.

#### JSON<a name="aws-resource-apigateway-account--examples--Associate_account_with_IAM_role--json"></a>

```
{
    "CloudWatchRole": {
        "Type": "AWS::IAM::Role",
        "Properties": {
            "AssumeRolePolicyDocument": {
                "Version": "2012-10-17",
                "Statement": [
                    {
                        "Effect": "Allow",
                        "Principal": {
                            "Service": [
                                "apigateway.amazonaws.com"
                            ]
                        },
                        "Action": "sts:AssumeRole"
                    }
                ]
            },
            "Path": "/",
            "ManagedPolicyArns": [
                "arn:aws:iam::aws:policy/service-role/AmazonAPIGatewayPushToCloudWatchLogs"
            ]
        }
    },
    "Account": {
        "Type": "AWS::ApiGateway::Account",
        "Properties": {
            "CloudWatchRoleArn": {
                "Fn::GetAtt": [
                    "CloudWatchRole",
                    "Arn"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-account--examples--Associate_account_with_IAM_role--yaml"></a>

```
CloudWatchRole:
  Type: 'AWS::IAM::Role'
  Properties:
    AssumeRolePolicyDocument:
      Version: 2012-10-17
      Statement:
        - Effect: Allow
          Principal:
            Service:
              - apigateway.amazonaws.com
          Action: 'sts:AssumeRole'
    Path: /
    ManagedPolicyArns:
      - >-
        arn:aws:iam::aws:policy/service-role/AmazonAPIGatewayPushToCloudWatchLogs
Account:
  Type: 'AWS::ApiGateway::Account'
  Properties:
    CloudWatchRoleArn: !GetAtt 
      - CloudWatchRole
      - Arn
```

## See also<a name="aws-resource-apigateway-account--seealso"></a>
+ [account:update](https://docs.aws.amazon.com/apigateway/api-reference/resource/account/) in the *Amazon API Gateway REST API Reference*

