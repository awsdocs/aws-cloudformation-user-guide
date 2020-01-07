# AWS::IoTAnalytics::Dataset DatasetContentDeliveryRule<a name="aws-properties-iotanalytics-dataset-datasetcontentdeliveryrule"></a>

When data set contents are created they are delivered to destination specified here\.

## Syntax<a name="aws-properties-iotanalytics-dataset-datasetcontentdeliveryrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-datasetcontentdeliveryrule-syntax.json"></a>

```
{
  "[Destination](#cfn-iotanalytics-dataset-datasetcontentdeliveryrule-destination)" : [DatasetContentDeliveryRuleDestination](aws-properties-iotanalytics-dataset-datasetcontentdeliveryruledestination.md),
  "[EntryName](#cfn-iotanalytics-dataset-datasetcontentdeliveryrule-entryname)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-datasetcontentdeliveryrule-syntax.yaml"></a>

```
  [Destination](#cfn-iotanalytics-dataset-datasetcontentdeliveryrule-destination): 
    [DatasetContentDeliveryRuleDestination](aws-properties-iotanalytics-dataset-datasetcontentdeliveryruledestination.md)
  [EntryName](#cfn-iotanalytics-dataset-datasetcontentdeliveryrule-entryname): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-datasetcontentdeliveryrule-properties"></a>

`Destination`  <a name="cfn-iotanalytics-dataset-datasetcontentdeliveryrule-destination"></a>
The destination to which data set contents are delivered\.  
*Required*: Yes  
*Type*: [DatasetContentDeliveryRuleDestination](aws-properties-iotanalytics-dataset-datasetcontentdeliveryruledestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntryName`  <a name="cfn-iotanalytics-dataset-datasetcontentdeliveryrule-entryname"></a>
The name of the data set content delivery rules entry\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)