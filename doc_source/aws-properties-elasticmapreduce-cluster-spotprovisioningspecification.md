# AWS::EMR::Cluster SpotProvisioningSpecification<a name="aws-properties-elasticmapreduce-cluster-spotprovisioningspecification"></a>

`SpotProvisioningSpecification` is a subproperty of the `InstanceFleetProvisioningSpecifications` property type\. `SpotProvisioningSpecification` determines the launch specification for Spot instances in the instance fleet, which includes the defined duration and provisioning timeout behavior\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-spotprovisioningspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-spotprovisioningspecification-syntax.json"></a>

```
{
  "[AllocationStrategy](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-allocationstrategy)" : String,
  "[BlockDurationMinutes](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-blockdurationminutes)" : Integer,
  "[TimeoutAction](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-timeoutaction)" : String,
  "[TimeoutDurationMinutes](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-timeoutdurationminutes)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-spotprovisioningspecification-syntax.yaml"></a>

```
  [AllocationStrategy](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-allocationstrategy): String
  [BlockDurationMinutes](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-blockdurationminutes): Integer
  [TimeoutAction](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-timeoutaction): String
  [TimeoutDurationMinutes](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-timeoutdurationminutes): Integer
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-spotprovisioningspecification-properties"></a>

`AllocationStrategy`  <a name="cfn-elasticmapreduce-cluster-spotprovisioningspecification-allocationstrategy"></a>
 Specifies the strategy to use in launching Spot Instance fleets\. Currently, the only option is capacity\-optimized \(the default\), which launches instances from Spot Instance pools with optimal capacity for the number of instances that are launching\.   
*Required*: No  
*Type*: String  
*Allowed values*: `capacity-optimized`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlockDurationMinutes`  <a name="cfn-elasticmapreduce-cluster-spotprovisioningspecification-blockdurationminutes"></a>
The defined duration for Spot Instances \(also known as Spot blocks\) in minutes\. When specified, the Spot Instance does not terminate before the defined duration expires, and defined duration pricing for Spot instances applies\. Valid values are 60, 120, 180, 240, 300, or 360\. The duration period starts as soon as a Spot Instance receives its instance ID\. At the end of the duration, Amazon EC2 marks the Spot Instance for termination and provides a Spot Instance termination notice, which gives the instance a two\-minute warning before it terminates\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutAction`  <a name="cfn-elasticmapreduce-cluster-spotprovisioningspecification-timeoutaction"></a>
The action to take when `TargetSpotCapacity` has not been fulfilled when the `TimeoutDurationMinutes` has expired; that is, when all Spot Instances could not be provisioned within the Spot provisioning timeout\. Valid values are `TERMINATE_CLUSTER` and `SWITCH_TO_ON_DEMAND`\. SWITCH\_TO\_ON\_DEMAND specifies that if no Spot Instances are available, On\-Demand Instances should be provisioned to fulfill any remaining Spot capacity\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SWITCH_TO_ON_DEMAND | TERMINATE_CLUSTER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutDurationMinutes`  <a name="cfn-elasticmapreduce-cluster-spotprovisioningspecification-timeoutdurationminutes"></a>
The spot provisioning timeout period in minutes\. If Spot Instances are not provisioned within this time period, the `TimeOutAction` is taken\. Minimum value is 5 and maximum value is 1440\. The timeout applies only during initial provisioning, when the cluster is first created\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)