# AWS::DynamoDB::GlobalTable ReadProvisionedThroughputSettings<a name="aws-properties-dynamodb-globaltable-readprovisionedthroughputsettings"></a>

Allows you to specify the read capacity settings for a replica table or a replica global secondary index when the `BillingMode` is set to `PROVISIONED`\. You must specify a value for either `ReadCapacityUnits` or `ReadCapacityAutoScalingSettings`, but not both\. You can switch between fixed capacity and auto scaling\.

## Syntax<a name="aws-properties-dynamodb-globaltable-readprovisionedthroughputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-readprovisionedthroughputsettings-syntax.json"></a>

```
{
  "[ReadCapacityAutoScalingSettings](#cfn-dynamodb-globaltable-readprovisionedthroughputsettings-readcapacityautoscalingsettings)" : CapacityAutoScalingSettings,
  "[ReadCapacityUnits](#cfn-dynamodb-globaltable-readprovisionedthroughputsettings-readcapacityunits)" : Integer
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-readprovisionedthroughputsettings-syntax.yaml"></a>

```
  [ReadCapacityAutoScalingSettings](#cfn-dynamodb-globaltable-readprovisionedthroughputsettings-readcapacityautoscalingsettings): 
    CapacityAutoScalingSettings
  [ReadCapacityUnits](#cfn-dynamodb-globaltable-readprovisionedthroughputsettings-readcapacityunits): Integer
```

## Properties<a name="aws-properties-dynamodb-globaltable-readprovisionedthroughputsettings-properties"></a>

`ReadCapacityAutoScalingSettings`  <a name="cfn-dynamodb-globaltable-readprovisionedthroughputsettings-readcapacityautoscalingsettings"></a>
Specifies auto scaling settings for the replica table or global secondary index\.  
*Required*: No  
*Type*: [CapacityAutoScalingSettings](aws-properties-dynamodb-globaltable-capacityautoscalingsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadCapacityUnits`  <a name="cfn-dynamodb-globaltable-readprovisionedthroughputsettings-readcapacityunits"></a>
Specifies a fixed read capacity for the replica table or global secondary index\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)