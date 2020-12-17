# AWS::Lambda::Permission<a name="aws-resource-lambda-permission"></a>

The `AWS::Lambda::Permission` resource grants an AWS service or another account permission to use a function\. You can apply the policy at the function level, or specify a qualifier to restrict access to a single version or alias\. If you use a qualifier, the invoker must use the full Amazon Resource Name \(ARN\) of that version or alias to invoke the function\.

To grant permission to another account, specify the account ID as the `Principal`\. For AWS services, the principal is a domain\-style identifier defined by the service, like `s3.amazonaws.com` or `sns.amazonaws.com`\. For AWS services, you can also specify the ARN of the associated resource as the `SourceArn`\. If you grant permission to a service principal without specifying the source, other accounts could potentially configure resources in their account to invoke your Lambda function\.

This resource adds a statement to a resource\-based permission policy for the function\. For more information about function policies, see [Lambda Function Policies](https://docs.aws.amazon.com/lambda/latest/dg/access-control-resource-based.html)\. 

## Syntax<a name="aws-resource-lambda-permission-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-permission-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::Permission",
  "Properties" : {
      "[Action](#cfn-lambda-permission-action)" : String,
      "[EventSourceToken](#cfn-lambda-permission-eventsourcetoken)" : String,
      "[FunctionName](#cfn-lambda-permission-functionname)" : String,
      "[Principal](#cfn-lambda-permission-principal)" : String,
      "[SourceAccount](#cfn-lambda-permission-sourceaccount)" : String,
      "[SourceArn](#cfn-lambda-permission-sourcearn)" : String
    }
}
```

### YAML<a name="aws-resource-lambda-permission-syntax.yaml"></a>

```
Type: AWS::Lambda::Permission
Properties: 
  [Action](#cfn-lambda-permission-action): String
  [EventSourceToken](#cfn-lambda-permission-eventsourcetoken): String
  [FunctionName](#cfn-lambda-permission-functionname): String
  [Principal](#cfn-lambda-permission-principal): String
  [SourceAccount](#cfn-lambda-permission-sourceaccount): String
  [SourceArn](#cfn-lambda-permission-sourcearn): String
```

## Properties<a name="aws-resource-lambda-permission-properties"></a>

`Action`  <a name="cfn-lambda-permission-action"></a>
The action that the principal can use on the function\. For example, `lambda:InvokeFunction` or `lambda:GetFunction`\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `(lambda:[*]|lambda:[a-zA-Z]+|[*])`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EventSourceToken`  <a name="cfn-lambda-permission-eventsourcetoken"></a>
For Alexa Smart Home functions, a token that must be supplied by the invoker\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z0-9._\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FunctionName`  <a name="cfn-lambda-permission-functionname"></a>
The name of the Lambda function, version, or alias\.  

**Name formats**
+  **Function name** \- `my-function` \(name\-only\), `my-function:v1` \(with alias\)\.
+  **Function ARN** \- `arn:aws:lambda:us-west-2:123456789012:function:my-function`\.
+  **Partial ARN** \- `123456789012:function:my-function`\.
You can append a version number or alias to any of the formats\. The length constraint applies only to the full ARN\. If you specify only the function name, it is limited to 64 characters in length\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `140`  
*Pattern*: `(arn:(aws[a-zA-Z-]*)?:lambda:)?([a-z]{2}(-gov)?-[a-z]+-\d{1}:)?(\d{12}:)?(function:)?([a-zA-Z0-9-_]+)(:(\$LATEST|[a-zA-Z0-9-_]+))?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Principal`  <a name="cfn-lambda-permission-principal"></a>
The AWS service or account that invokes the function\. If you specify a service, use `SourceArn` or `SourceAccount` to limit who can invoke the function through that service\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceAccount`  <a name="cfn-lambda-permission-sourceaccount"></a>
For Amazon S3, the ID of the account that owns the resource\. Use this together with `SourceArn` to ensure that the resource is owned by the specified account\. It is possible for an Amazon S3 bucket to be deleted by its owner and recreated by another account\.  
*Required*: No  
*Type*: String  
*Pattern*: `\d{12}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceArn`  <a name="cfn-lambda-permission-sourcearn"></a>
For AWS services, the ARN of the AWS resource that invokes the function\. For example, an Amazon S3 bucket or Amazon SNS topic\.  
*Required*: No  
*Type*: String  
*Pattern*: `arn:(aws[a-zA-Z0-9-]*):([a-zA-Z0-9\-])+:([a-z]{2}(-gov)?-[a-z]+-\d{1})?:(\d{12})?:(.*)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-lambda-permission--examples"></a>



### Cross Account Invoke<a name="aws-resource-lambda-permission--examples--Cross_Account_Invoke"></a>

Grant account 123456789012 permission to invoke a function resource named `function` created in the same template\.

#### YAML<a name="aws-resource-lambda-permission--examples--Cross_Account_Invoke--yaml"></a>

```
  permission:
    Type: AWS::Lambda::Permission
    Properties:
      FunctionName: !GetAtt function.Arn
      Action: lambda:InvokeFunction
      Principal: 123456789012
```

### Amazon S3 Notifications<a name="aws-resource-lambda-permission--examples--Amazon_S3_Notifications"></a>

Grant Amazon S3 permission to invoke a function resource named `function` created in the same template, to process notifications for a bucket resource named `bucket`\.

#### JSON<a name="aws-resource-lambda-permission--examples--Amazon_S3_Notifications--json"></a>

```
"s3Permission": {
    "Type": "AWS::Lambda::Permission",
    "Properties": {
        "FunctionName": {
            "Fn::GetAtt": [
                "function",
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
                "bucket",
                "Arn"
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-lambda-permission--examples--Amazon_S3_Notifications--yaml"></a>

```
s3Permission:
  Type: AWS::Lambda::Permission
  Properties:
    FunctionName: !GetAtt function.Arn
    Action: lambda:InvokeFunction
    Principal: s3.amazonaws.com
    SourceAccount: !Ref 'AWS::AccountId'
    SourceArn: !GetAtt bucket.Arn
```