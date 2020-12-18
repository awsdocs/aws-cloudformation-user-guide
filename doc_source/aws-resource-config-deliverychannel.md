# AWS::Config::DeliveryChannel<a name="aws-resource-config-deliverychannel"></a>

Specifies a delivery channel object to deliver configuration information to an Amazon S3 bucket and Amazon SNS topic\.

Before you can create a delivery channel, you must create a configuration recorder\.

You can use this action to change the Amazon S3 bucket or an Amazon SNS topic of the existing delivery channel\. To change the Amazon S3 bucket or an Amazon SNS topic, call this action and specify the changed values for the S3 bucket and the SNS topic\. If you specify a different value for either the S3 bucket or the SNS topic, this action will keep the existing value for the parameter that is not changed\.

**Note**  
You can have only one delivery channel per region in your account\.

When you create the delivery channel, you can specify; how often AWS Config delivers configuration snapshots to your Amazon S3 bucket \(for example, 24 hours\), the S3 bucket to which AWS Config sends configuration snapshots and configuration history files, and the Amazon SNS topic to which AWS Config sends notifications about configuration changes, such as updated resources, AWS Config rule evaluations, and when AWS Config delivers the configuration snapshot to your S3 bucket\. For more information, see [Deliver Configuration Items](https://docs.aws.amazon.com/config/latest/developerguide/how-does-config-work.html#delivery-channel) in the AWS Config Developer Guide\. 

**Note**  
To enable AWS Config, you must create a configuration recorder and a delivery channel\. If you want to create the resources separately, you must create a configuration recorder before you can create a delivery channel\. AWS Config uses the configuration recorder to capture configuration changes to your resources\. For more information, see [AWS::Config::ConfigurationRecorder](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-configurationrecorder.html)\. 

For more information, see [Managing the Delivery Channel](https://docs.aws.amazon.com/config/latest/developerguide/manage-delivery-channel.html) in the AWS Config Developer Guide\. 

## Syntax<a name="aws-resource-config-deliverychannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-deliverychannel-syntax.json"></a>

```
{
  "Type" : "AWS::Config::DeliveryChannel",
  "Properties" : {
      "[ConfigSnapshotDeliveryProperties](#cfn-config-deliverychannel-configsnapshotdeliveryproperties)" : ConfigSnapshotDeliveryProperties,
      "[Name](#cfn-config-deliverychannel-name)" : String,
      "[S3BucketName](#cfn-config-deliverychannel-s3bucketname)" : String,
      "[S3KeyPrefix](#cfn-config-deliverychannel-s3keyprefix)" : String,
      "[SnsTopicARN](#cfn-config-deliverychannel-snstopicarn)" : String
    }
}
```

### YAML<a name="aws-resource-config-deliverychannel-syntax.yaml"></a>

```
Type: AWS::Config::DeliveryChannel
Properties: 
  [ConfigSnapshotDeliveryProperties](#cfn-config-deliverychannel-configsnapshotdeliveryproperties): 
    ConfigSnapshotDeliveryProperties
  [Name](#cfn-config-deliverychannel-name): String
  [S3BucketName](#cfn-config-deliverychannel-s3bucketname): String
  [S3KeyPrefix](#cfn-config-deliverychannel-s3keyprefix): String
  [SnsTopicARN](#cfn-config-deliverychannel-snstopicarn): String
```

## Properties<a name="aws-resource-config-deliverychannel-properties"></a>

`ConfigSnapshotDeliveryProperties`  <a name="cfn-config-deliverychannel-configsnapshotdeliveryproperties"></a>
The options for how often AWS Config delivers configuration snapshots to the Amazon S3 bucket\.  
*Required*: No  
*Type*: [ConfigSnapshotDeliveryProperties](aws-properties-config-deliverychannel-configsnapshotdeliveryproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-config-deliverychannel-name"></a>
A name for the delivery channel\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the delivery channel name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.   
Updates are not supported\. To change the name, you must run two separate updates\. In the first update, delete this resource, and then recreate it with a new name in the second update\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3BucketName`  <a name="cfn-config-deliverychannel-s3bucketname"></a>
The name of the Amazon S3 bucket to which AWS Config delivers configuration snapshots and configuration history files\.  
If you specify a bucket that belongs to another AWS account, that bucket must have policies that grant access permissions to AWS Config\. For more information, see [Permissions for the Amazon S3 Bucket](https://docs.aws.amazon.com/config/latest/developerguide/s3-bucket-policy.html) in the AWS Config Developer Guide\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3KeyPrefix`  <a name="cfn-config-deliverychannel-s3keyprefix"></a>
The prefix for the specified Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnsTopicARN`  <a name="cfn-config-deliverychannel-snstopicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to which AWS Config sends notifications about configuration changes\.  
If you choose a topic from another account, the topic must have policies that grant access permissions to AWS Config\. For more information, see [Permissions for the Amazon SNS Topic](https://docs.aws.amazon.com/config/latest/developerguide/sns-topic-policy.html) in the AWS Config Developer Guide\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-config-deliverychannel-return-values"></a>

### Ref<a name="aws-resource-config-deliverychannel-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the delivery channel name, such as default\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-config-deliverychannel--examples"></a>



### Delivery Channel<a name="aws-resource-config-deliverychannel--examples--Delivery_Channel"></a>

The following example creates a delivery channel that sends notifications to the specified Amazon SNS topic\. The delivery channel also sends configuration changes and snapshots to the specified S3 bucket\. 

#### JSON<a name="aws-resource-config-deliverychannel--examples--Delivery_Channel--json"></a>

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

#### YAML<a name="aws-resource-config-deliverychannel--examples--Delivery_Channel--yaml"></a>

```
DeliveryChannel: 
  Type: AWS::Config::DeliveryChannel
  Properties: 
    ConfigSnapshotDeliveryProperties: 
      DeliveryFrequency: "Six_Hours"
    S3BucketName: 
      Ref: ConfigBucket
    SnsTopicARN: 
      Ref: ConfigTopic
```