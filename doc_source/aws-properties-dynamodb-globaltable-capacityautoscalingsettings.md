# AWS::DynamoDB::GlobalTable CapacityAutoScalingSettings<a name="aws-properties-dynamodb-globaltable-capacityautoscalingsettings"></a>

Configures a scalable target and an autoscaling policy for a table or global secondary index's read or write capacity\.

## Syntax<a name="aws-properties-dynamodb-globaltable-capacityautoscalingsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-capacityautoscalingsettings-syntax.json"></a>

```
{
  "[MaxCapacity](#cfn-dynamodb-globaltable-capacityautoscalingsettings-maxcapacity)" : Integer,
  "[MinCapacity](#cfn-dynamodb-globaltable-capacityautoscalingsettings-mincapacity)" : Integer,
  "[SeedCapacity](#cfn-dynamodb-globaltable-capacityautoscalingsettings-seedcapacity)" : Integer,
  "[TargetTrackingScalingPolicyConfiguration](#cfn-dynamodb-globaltable-capacityautoscalingsettings-targettrackingscalingpolicyconfiguration)" : TargetTrackingScalingPolicyConfiguration
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-capacityautoscalingsettings-syntax.yaml"></a>

```
  [MaxCapacity](#cfn-dynamodb-globaltable-capacityautoscalingsettings-maxcapacity): Integer
  [MinCapacity](#cfn-dynamodb-globaltable-capacityautoscalingsettings-mincapacity): Integer
  [SeedCapacity](#cfn-dynamodb-globaltable-capacityautoscalingsettings-seedcapacity): Integer
  [TargetTrackingScalingPolicyConfiguration](#cfn-dynamodb-globaltable-capacityautoscalingsettings-targettrackingscalingpolicyconfiguration): 
    TargetTrackingScalingPolicyConfiguration
```

## Properties<a name="aws-properties-dynamodb-globaltable-capacityautoscalingsettings-properties"></a>

`MaxCapacity`  <a name="cfn-dynamodb-globaltable-capacityautoscalingsettings-maxcapacity"></a>
The maximum provisioned capacity units for the global table\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinCapacity`  <a name="cfn-dynamodb-globaltable-capacityautoscalingsettings-mincapacity"></a>
The minimum provisioned capacity units for the global table\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SeedCapacity`  <a name="cfn-dynamodb-globaltable-capacityautoscalingsettings-seedcapacity"></a>
When switching billing mode from `PAY_PER_REQUEST` to `PROVISIONED`, DynamoDB requires you to specify read and write capacity unit values for the table and for each global secondary index\. These values will be applied to all replicas\. The table will use these provisioned values until CloudFormation creates the autoscaling policies you configured in your template\. CloudFormation cannot determine what capacity the table and its global secondary indexes will require in this time period, since they are application\-dependent\.  
If you want to switch a table's billing mode from `PAY_PER_REQUEST` to `PROVISIONED`, you must specify a value for this property for each autoscaled resource\. If you specify different values for the same resource in different regions, CloudFormation will use the highest value found in either the `SeedCapacity` or `ReadCapacityUnits` properties\. For example, if your global secondary index `myGSI` has a `SeedCapacity` of 10 in us\-east\-1 and a fixed `ReadCapacityUnits` of 20 in eu\-west\-1, CloudFormation will initially set the read capacity for `myGSI` to 20\. Note that if you disable `ScaleIn` for `myGSI` in us\-east\-1, its read capacity units might not be set back to 10\.  
You must also specify a value for `SeedCapacity` when you plan to switch a table's billing mode from `PROVISIONED` to `PAY_PER_REQUEST`, because CloudFormation might need to roll back the operation \(reverting the billing mode to `PROVISIONED`\) and this cannot succeed without specifying a value for `SeedCapacity`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTrackingScalingPolicyConfiguration`  <a name="cfn-dynamodb-globaltable-capacityautoscalingsettings-targettrackingscalingpolicyconfiguration"></a>
Defines a target tracking scaling policy\.  
*Required*: Yes  
*Type*: [TargetTrackingScalingPolicyConfiguration](aws-properties-dynamodb-globaltable-targettrackingscalingpolicyconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)