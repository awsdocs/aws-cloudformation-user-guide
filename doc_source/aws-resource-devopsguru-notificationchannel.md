# AWS::DevOpsGuru::NotificationChannel<a name="aws-resource-devopsguru-notificationchannel"></a>

 Adds a notification channel to DevOps Guru\. A notification channel is used to notify you about important DevOps Guru events, such as when an insight is generated\. 

If you use an Amazon SNS topic in another account, you must attach a policy to it that grants DevOps Guru permission to it notifications\. DevOps Guru adds the required policy on your behalf to send notifications using Amazon SNS in your account\. For more information, see [Permissions for cross account Amazon SNS topics](https://docs.aws.amazon.com/devops-guru/latest/userguide/sns-required-permissions.html)\.

If you use an Amazon SNS topic that is encrypted by an AWS Key Management Service customer\-managed key \(CMK\), then you must add permissions to the CMK\. For more information, see [Permissions for AWS KMS–encrypted Amazon SNS topics](https://docs.aws.amazon.com/devops-guru/latest/userguide/sns-kms-permissions.html)\.

## Syntax<a name="aws-resource-devopsguru-notificationchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-devopsguru-notificationchannel-syntax.json"></a>

```
{
  "Type" : "AWS::DevOpsGuru::NotificationChannel",
  "Properties" : {
      "[Config](#cfn-devopsguru-notificationchannel-config)" : NotificationChannelConfig
    }
}
```

### YAML<a name="aws-resource-devopsguru-notificationchannel-syntax.yaml"></a>

```
Type: AWS::DevOpsGuru::NotificationChannel
Properties: 
  [Config](#cfn-devopsguru-notificationchannel-config): 
    NotificationChannelConfig
```

## Properties<a name="aws-resource-devopsguru-notificationchannel-properties"></a>

`Config`  <a name="cfn-devopsguru-notificationchannel-config"></a>
 A `NotificationChannelConfig` object that contains information about configured notification channels\.   
*Required*: Yes  
*Type*: [NotificationChannelConfig](aws-properties-devopsguru-notificationchannel-notificationchannelconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-devopsguru-notificationchannel-return-values"></a>

### Ref<a name="aws-resource-devopsguru-notificationchannel-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns Amazon Resource Name \(ARN\) of the `NotificationChannel`\. For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

### Fn::GetAtt<a name="aws-resource-devopsguru-notificationchannel-return-values-fn--getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-devopsguru-notificationchannel-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the notification channel\. 

## Examples<a name="aws-resource-devopsguru-notificationchannel--examples"></a>

### Create one notification channel<a name="aws-resource-devopsguru-notificationchannel--examples--Create_one_notification_channel"></a>

#### JSON<a name="aws-resource-devopsguru-notificationchannel--examples--Create_one_notification_channel--json"></a>

```
{
  "Resources": {
    "MyNotificationChannel": {
      "Type": "AWS::DevOpsGuru::NotificationChannel",
      "Properties": {
        "Config": {
          "Sns": {
            "TopicArn": "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-devopsguru-notificationchannel--examples--Create_one_notification_channel--yaml"></a>

```
Resources:
  MyNotificationChannel:
    Type: AWS::DevOpsGuru::NotificationChannel
    Properties:
      Config:
        Sns:
          TopicArn: arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel
```

### Create two notification channels<a name="aws-resource-devopsguru-notificationchannel--examples--Create_two_notification_channels"></a>

#### JSON<a name="aws-resource-devopsguru-notificationchannel--examples--Create_two_notification_channels--json"></a>

```
{
  "Resources": {
    "MyNotificationChannel1": {
      "Type": "AWS::DevOpsGuru::NotificationChannel",
      "Properties": {
        "Config": {
          "Sns": {
            "TopicArn": "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel"
          }
        }
      }
    },
    "MyNotificationChannel2": {
      "Type": "AWS::DevOpsGuru::NotificationChannel",
      "Properties": {
        "Config": {
          "Sns": {
            "TopicArn": "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel2"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-devopsguru-notificationchannel--examples--Create_two_notification_channels--yaml"></a>

```
Resources:
  MyNotificationChannel1:
    Type: AWS::DevOpsGuru::NotificationChannel
    Properties:
      Config:
        Sns:
          TopicArn: arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel
  MyNotificationChannel2:
    Type: AWS::DevOpsGuru::NotificationChannel
    Properties:
      Config:
        Sns:
          TopicArn: arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel2
```