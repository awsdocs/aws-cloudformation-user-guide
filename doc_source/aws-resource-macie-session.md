# AWS::Macie::Session<a name="aws-resource-macie-session"></a>

The `AWS::Macie::Session` resource represents the Amazon Macie service and configuration settings for an account\. A `Session` is created for each AWS Region in which you enable Macie\. 

You must create a `Session` for an account before you can create an `AWS::Macie::FindingsFilter` or `AWS::Macie::CustomDataIdentifier` resource\. Use a [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to ensure that the `Session` is created before the other resources\. For example, `"DependsOn: Session"`\.

## Syntax<a name="aws-resource-macie-session-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-macie-session-syntax.json"></a>

```
{
  "Type" : "AWS::Macie::Session",
  "Properties" : {
      "[FindingPublishingFrequency](#cfn-macie-session-findingpublishingfrequency)" : String,
      "[Status](#cfn-macie-session-status)" : String
    }
}
```

### YAML<a name="aws-resource-macie-session-syntax.yaml"></a>

```
Type: AWS::Macie::Session
Properties: 
  [FindingPublishingFrequency](#cfn-macie-session-findingpublishingfrequency): String
  [Status](#cfn-macie-session-status): String
```

## Properties<a name="aws-resource-macie-session-properties"></a>

`FindingPublishingFrequency`  <a name="cfn-macie-session-findingpublishingfrequency"></a>
The frequency with which Amazon Macie publishes updates to policy findings for an account\. This includes publishing updates to AWS Security Hub and Amazon EventBridge \(formerly called Amazon CloudWatch Events\)\. Valid values are:  
+ FIFTEEN\_MINUTES
+ ONE\_HOUR
+ SIX\_HOURS
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-macie-session-status"></a>
The `MacieStatus` of the `Session`\. Valid values include `ENABLED` and `PAUSED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-macie-session-return-values"></a>

### Ref<a name="aws-resource-macie-session-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the AWS Account ID for the account in which the Macie session is created\. For example, `{ "Ref": "Session" }`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-macie-session-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-macie-session-return-values-fn--getatt-fn--getatt"></a>

`AwsAccountId`  <a name="AwsAccountId-fn::getatt"></a>
The account ID for the AWS account in which the `Session` is created\.

`ServiceRole`  <a name="ServiceRole-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the service\-linked role that allows Amazon Macie to monitor and analyze data in AWS resources for the account\.

## Examples<a name="aws-resource-macie-session--examples"></a>

The following example demonstrates how to declare an `AWS::Macie::Session` resource\.

### Creating a Macie Session<a name="aws-resource-macie-session--examples--Creating_a_Macie_Session"></a>

This example enables Amazon Macie for an account\. It also configures Macie to publish updated findings every hour for the account\.

#### JSON<a name="aws-resource-macie-session--examples--Creating_a_Macie_Session--json"></a>

```
{
    "Type": "AWS::Macie::Session",
    "Properties": {
        "FindingPublishingFrequency": "ONE_HOUR",
        "Status": "ENABLED"
    }
}
```

#### YAML<a name="aws-resource-macie-session--examples--Creating_a_Macie_Session--yaml"></a>

```
Type: AWS::Macie::Session
Properties:
    FindingPublishingFrequency: ONE_HOUR
    Status: ENABLED
```