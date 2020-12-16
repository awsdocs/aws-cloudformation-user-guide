# AWS::FMS::NotificationChannel<a name="aws-resource-fms-notificationchannel"></a>

Designates the IAM role and Amazon Simple Notification Service \(SNS\) topic that AWS Firewall Manager uses to record SNS logs\.

To perform this action outside of the console, you must configure the SNS topic to allow the Firewall Manager role `AWSServiceRoleForFMS` to publish SNS logs\. For more information, see [Firewall Manager required permissions for API actions](https://docs.aws.amazon.com/waf/latest/developerguide/fms-api-permissions-ref.html) in the *AWS Firewall Manager Developer Guide*\.

## Syntax<a name="aws-resource-fms-notificationchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-fms-notificationchannel-syntax.json"></a>

```
{
  "Type" : "AWS::FMS::NotificationChannel",
  "Properties" : {
      "[SnsRoleName](#cfn-fms-notificationchannel-snsrolename)" : String,
      "[SnsTopicArn](#cfn-fms-notificationchannel-snstopicarn)" : String
    }
}
```

### YAML<a name="aws-resource-fms-notificationchannel-syntax.yaml"></a>

```
Type: AWS::FMS::NotificationChannel
Properties: 
  [SnsRoleName](#cfn-fms-notificationchannel-snsrolename): String
  [SnsTopicArn](#cfn-fms-notificationchannel-snstopicarn): String
```

## Properties<a name="aws-resource-fms-notificationchannel-properties"></a>

`SnsRoleName`  <a name="cfn-fms-notificationchannel-snsrolename"></a>
The Amazon Resource Name \(ARN\) of the IAM role that allows Amazon SNS to record AWS Firewall Manager activity\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnsTopicArn`  <a name="cfn-fms-notificationchannel-snstopicarn"></a>
The Amazon Resource Name \(ARN\) of the SNS topic that collects notifications from AWS Firewall Manager\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-fms-notificationchannel-return-values"></a>

### Ref<a name="aws-resource-fms-notificationchannel-return-values-ref"></a>

The `Ref` for this resource returns the `SnsTopicArn`\. This is the Amazon Resource Name \(ARN\) that uniquely identifies the Amazon Simple Notification Service \(Amazon SNS\) topic\. For example, `arn:aws:sns:us-west-2:111122223333:MyTopic`\. For more information about SNS, see [Amazon Simple Notification Service Resource Type Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_SNS.html)\.

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-fms-notificationchannel--examples"></a>



### Create a Firewall Manager notification channel<a name="aws-resource-fms-notificationchannel--examples--Create_a_Firewall_Manager_notification_channel"></a>

The following shows an example SNS notification channel for Firewall Manager\. 

#### YAML<a name="aws-resource-fms-notificationchannel--examples--Create_a_Firewall_Manager_notification_channel--yaml"></a>

```
NotificationChannel:
    Type: AWS::FMS::NotificationChannel
    Properties:
      SnsRoleName: !Sub arn:aws:iam::${AWS::AccountId}:role/aws-service-role/fms.amazonaws.com/AWSServiceRoleForFMS
      SnsTopicArn: !Ref SnsTopic
```

#### JSON<a name="aws-resource-fms-notificationchannel--examples--Create_a_Firewall_Manager_notification_channel--json"></a>

```
"NotificationChannel": {
    "Type": "AWS::FMS::NotificationChannel",
    "Properties": {
        "SnsRoleName": {
            "Fn::Sub": "arn:aws:iam::${AWS::AccountId}:role/aws-service-role/fms.amazonaws.com/AWSServiceRoleForFMS"
        },
        "SnsTopicArn": {
            "Ref": "SnsTopic"
        }
    }
}
```