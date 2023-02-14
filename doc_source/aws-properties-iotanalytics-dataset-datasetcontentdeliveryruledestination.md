# AWS::IoTAnalytics::Dataset DatasetContentDeliveryRuleDestination<a name="aws-properties-iotanalytics-dataset-datasetcontentdeliveryruledestination"></a>

The destination to which dataset contents are delivered\.

## Syntax<a name="aws-properties-iotanalytics-dataset-datasetcontentdeliveryruledestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-datasetcontentdeliveryruledestination-syntax.json"></a>

```
{
  "[IotEventsDestinationConfiguration](#cfn-iotanalytics-dataset-datasetcontentdeliveryruledestination-ioteventsdestinationconfiguration)" : IotEventsDestinationConfiguration,
  "[S3DestinationConfiguration](#cfn-iotanalytics-dataset-datasetcontentdeliveryruledestination-s3destinationconfiguration)" : S3DestinationConfiguration
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-datasetcontentdeliveryruledestination-syntax.yaml"></a>

```
  [IotEventsDestinationConfiguration](#cfn-iotanalytics-dataset-datasetcontentdeliveryruledestination-ioteventsdestinationconfiguration): 
    IotEventsDestinationConfiguration
  [S3DestinationConfiguration](#cfn-iotanalytics-dataset-datasetcontentdeliveryruledestination-s3destinationconfiguration): 
    S3DestinationConfiguration
```

## Properties<a name="aws-properties-iotanalytics-dataset-datasetcontentdeliveryruledestination-properties"></a>

`IotEventsDestinationConfiguration`  <a name="cfn-iotanalytics-dataset-datasetcontentdeliveryruledestination-ioteventsdestinationconfiguration"></a>
Configuration information for delivery of dataset contents to AWS IoT Events\.  
*Required*: No  
*Type*: [IotEventsDestinationConfiguration](aws-properties-iotanalytics-dataset-ioteventsdestinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3DestinationConfiguration`  <a name="cfn-iotanalytics-dataset-datasetcontentdeliveryruledestination-s3destinationconfiguration"></a>
Configuration information for delivery of dataset contents to Amazon S3\.  
*Required*: No  
*Type*: [S3DestinationConfiguration](aws-properties-iotanalytics-dataset-s3destinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)