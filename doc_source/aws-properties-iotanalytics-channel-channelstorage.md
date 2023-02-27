# AWS::IoTAnalytics::Channel ChannelStorage<a name="aws-properties-iotanalytics-channel-channelstorage"></a>

Where channel data is stored\. You may choose one of `serviceManagedS3`, `customerManagedS3` storage\. If not specified, the default is `serviceManagedS3`\. This can't be changed after creation of the channel\.

## Syntax<a name="aws-properties-iotanalytics-channel-channelstorage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-channel-channelstorage-syntax.json"></a>

```
{
  "[CustomerManagedS3](#cfn-iotanalytics-channel-channelstorage-customermanageds3)" : CustomerManagedS3,
  "[ServiceManagedS3](#cfn-iotanalytics-channel-channelstorage-servicemanageds3)" : Json
}
```

### YAML<a name="aws-properties-iotanalytics-channel-channelstorage-syntax.yaml"></a>

```
  [CustomerManagedS3](#cfn-iotanalytics-channel-channelstorage-customermanageds3): 
    CustomerManagedS3
  [ServiceManagedS3](#cfn-iotanalytics-channel-channelstorage-servicemanageds3): Json
```

## Properties<a name="aws-properties-iotanalytics-channel-channelstorage-properties"></a>

`CustomerManagedS3`  <a name="cfn-iotanalytics-channel-channelstorage-customermanageds3"></a>
Used to store channel data in an S3 bucket that you manage\. If customer managed storage is selected, the `retentionPeriod` parameter is ignored\. You can't change the choice of S3 storage after the data store is created\.  
*Required*: No  
*Type*: [CustomerManagedS3](aws-properties-iotanalytics-channel-customermanageds3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceManagedS3`  <a name="cfn-iotanalytics-channel-channelstorage-servicemanageds3"></a>
Used to store channel data in an S3 bucket managed by AWS IoT Analytics\. You can't change the choice of S3 storage after the data store is created\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)