# AWS::Config::DeliveryChannel<a name="aws-resource-config-deliverychannel"></a>

The `AWS::Config::DeliveryChannel` resource describes where AWS Config sends notifications and updated configuration states for AWS resources\. 

When you create the delivery channel, you can specify the following: 
+ How often AWS Config delivers configuration snapshots to your Amazon S3 bucket \(for example, 24 hours\)
+ The S3 bucket to which AWS Config sends configuration snapshots and configuration history files
+ The Amazon SNS topic to which AWS Config sends notifications about configuration changes, such as updated resources, AWS Config rule evaluations, and when AWS Config delivers the configuration snapshot to your S3 bucket\.

For more information, see [Deliver Configuration Items](http://docs.aws.amazon.com/config/latest/developerguide/how-does-config-work.html#delivery-channel) in the *AWS Config Developer Guide*\.

**Note**  
To enable AWS Config, you must create a configuration recorder and a delivery channel\. If you want to create the resources separately, you must create a configuration recorder before you can create a delivery channel\. AWS Config uses the configuration recorder to capture configuration changes to your resources\. For more information, see [AWS::Config::ConfigurationRecorder](aws-resource-config-configurationrecorder.md)\. 

For more information, see [Managing the Delivery Channel](http://docs.aws.amazon.com/config/latest/developerguide/manage-delivery-channel.html) in the *AWS Config Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-config-deliverychannel-syntax)
+ [Properties](#w3ab2c21c10d316c19)
+ [Return Values](#w3ab2c21c10d316c21)
+ [Example](#w3ab2c21c10d316c23)

## Syntax<a name="aws-resource-config-deliverychannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-deliverychannel-syntax.json"></a>

```
{
  "Type" : "AWS::Config::DeliveryChannel",
  "Properties" : {
    "[ConfigSnapshotDeliveryProperties](#cfn-config-deliverychannel-configsnapshotdeliveryproperties)" : Config snapshot delivery properties,
    "[Name](#cfn-config-deliverychannel-name)" : String,
    "[S3BucketName](#cfn-config-deliverychannel-s3bucketname)" : String,
    "[S3KeyPrefix](#cfn-config-deliverychannel-s3keyprefix)" : String,
    "[SnsTopicARN](#cfn-config-deliverychannel-snstopicarn)" : String
  }
}
```

### YAML<a name="aws-resource-config-deliverychannel-syntax.yaml"></a>

```
Type: "AWS::Config::DeliveryChannel"
Properties:
  [ConfigSnapshotDeliveryProperties](#cfn-config-deliverychannel-configsnapshotdeliveryproperties):
    Config snapshot delivery properties
  [Name](#cfn-config-deliverychannel-name): String
  [S3BucketName](#cfn-config-deliverychannel-s3bucketname): String
  [S3KeyPrefix](#cfn-config-deliverychannel-s3keyprefix): String
  [SnsTopicARN](#cfn-config-deliverychannel-snstopicarn): String
```

## Properties<a name="w3ab2c21c10d316c19"></a>

`ConfigSnapshotDeliveryProperties`  <a name="cfn-config-deliverychannel-configsnapshotdeliveryproperties"></a>
Provides options for how AWS Config delivers configuration snapshots to the S3 bucket in your delivery channel\.  
*Required*: No  
*Type*: [AWS Config DeliveryChannel ConfigSnapshotDeliveryProperties](aws-properties-config-deliverychannel-configsnapshotdeliveryproperties.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-config-deliverychannel-name"></a>
A name for the delivery channel\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the delivery channel name\. For more information, see [Name Type](aws-properties-name.md)\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\. To change the name, you must run two separate updates\. In the first update, delete this resource, and then recreate it with a new name in the second update\.

`S3BucketName`  <a name="cfn-config-deliverychannel-s3bucketname"></a>
The name of an S3 bucket where you want to store configuration history for the delivery channel\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`S3KeyPrefix`  <a name="cfn-config-deliverychannel-s3keyprefix"></a>
A key prefix \(folder\) for the specified S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SnsTopicARN`  <a name="cfn-config-deliverychannel-snstopicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Simple Notification Service \(Amazon SNS\) topic that AWS Config delivers notifications to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d316c21"></a>

### Ref<a name="w3ab2c21c10d316c21b2"></a>

When you pass the logical ID of an `AWS::Config::DeliveryChannel` resource to the intrinsic `Ref` function, the function returns the delivery channel name, such as `default`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d316c23"></a>

The following example creates a delivery channel that sends notifications to the specified Amazon SNS topic\. The delivery channel also sends configuration changes and snapshots to the specified S3 bucket\.

### JSON<a name="aws-resource-config-deliverychannel-example.json"></a>

```
"DeliveryChannel": {
  "Type": "AWS::Config::DeliveryChannel",
  "Properties": {
    "ConfigSnapshotDeliveryProperties": {
      "DeliveryFrequency": "Six_Hours"
    },
    "S3BucketName": {"Ref": "ConfigBucket"},
    "SnsTopicARN": {"Ref": "ConfigTopic"}
  }
}
```

### YAML<a name="aws-resource-config-deliverychannel-example.yaml"></a>

```
DeliveryChannel: 
  Type: "AWS::Config::DeliveryChannel"
  Properties: 
    ConfigSnapshotDeliveryProperties: 
      DeliveryFrequency: "Six_Hours"
    S3BucketName: 
      Ref: ConfigBucket
    SnsTopicARN: 
      Ref: ConfigTopic
```