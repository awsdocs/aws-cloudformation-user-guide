# AWS::EMR::Cluster InstanceGroupConfig<a name="aws-properties-elasticmapreduce-cluster-instancegroupconfig"></a>

Use `InstanceGroupConfig` to define instance groups for an EMR cluster\. A cluster can not use both instance groups and instance fleets\. For more information, see [Create a Cluster with Instance Fleets or Uniform Instance Groups](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-instance-group-configuration.html) in the *Amazon EMR Management Guide*\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-instancegroupconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-instancegroupconfig-syntax.json"></a>

```
{
  "[AutoScalingPolicy](#cfn-elasticmapreduce-cluster-instancegroupconfig-autoscalingpolicy)" : AutoScalingPolicy,
  "[BidPrice](#cfn-elasticmapreduce-cluster-instancegroupconfig-bidprice)" : String,
  "[Configurations](#cfn-elasticmapreduce-cluster-instancegroupconfig-configurations)" : [ Configuration, ... ],
  "[EbsConfiguration](#cfn-elasticmapreduce-cluster-instancegroupconfig-ebsconfiguration)" : EbsConfiguration,
  "[InstanceCount](#cfn-elasticmapreduce-cluster-instancegroupconfig-instancecount)" : Integer,
  "[InstanceType](#cfn-elasticmapreduce-cluster-instancegroupconfig-instancetype)" : String,
  "[Market](#cfn-elasticmapreduce-cluster-instancegroupconfig-market)" : String,
  "[Name](#cfn-elasticmapreduce-cluster-instancegroupconfig-name)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-instancegroupconfig-syntax.yaml"></a>

```
  [AutoScalingPolicy](#cfn-elasticmapreduce-cluster-instancegroupconfig-autoscalingpolicy): 
    AutoScalingPolicy
  [BidPrice](#cfn-elasticmapreduce-cluster-instancegroupconfig-bidprice): String
  [Configurations](#cfn-elasticmapreduce-cluster-instancegroupconfig-configurations): 
    - Configuration
  [EbsConfiguration](#cfn-elasticmapreduce-cluster-instancegroupconfig-ebsconfiguration): 
    EbsConfiguration
  [InstanceCount](#cfn-elasticmapreduce-cluster-instancegroupconfig-instancecount): Integer
  [InstanceType](#cfn-elasticmapreduce-cluster-instancegroupconfig-instancetype): String
  [Market](#cfn-elasticmapreduce-cluster-instancegroupconfig-market): String
  [Name](#cfn-elasticmapreduce-cluster-instancegroupconfig-name): String
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-instancegroupconfig-properties"></a>

`AutoScalingPolicy`  <a name="cfn-elasticmapreduce-cluster-instancegroupconfig-autoscalingpolicy"></a>
`AutoScalingPolicy` is a subproperty of the [InstanceGroupConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig.html) property type that specifies the constraints and rules of an automatic scaling policy in Amazon EMR\. The automatic scaling policy defines how an instance group dynamically adds and terminates EC2 instances in response to the value of a CloudWatch metric\. Only core and task instance groups can use automatic scaling policies\. For more information, see [Using Automatic Scaling in Amazon EMR](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-automatic-scaling.html)\.  
*Required*: No  
*Type*: [AutoScalingPolicy](aws-properties-elasticmapreduce-cluster-autoscalingpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BidPrice`  <a name="cfn-elasticmapreduce-cluster-instancegroupconfig-bidprice"></a>
The bid price for each EC2 Spot Instance type as defined by `InstanceType`\. Expressed in USD\. If neither `BidPrice` nor `BidPriceAsPercentageOfOnDemandPrice` is provided, `BidPriceAsPercentageOfOnDemandPrice` defaults to 100%\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Configurations`  <a name="cfn-elasticmapreduce-cluster-instancegroupconfig-configurations"></a>
Amazon EMR releases 4\.x or later\.
The list of configurations supplied for an EMR cluster instance group\. You can specify a separate configuration for each instance group \(master, core, and task\)\.  
*Required*: No  
*Type*: List of [Configuration](aws-properties-elasticmapreduce-cluster-configuration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EbsConfiguration`  <a name="cfn-elasticmapreduce-cluster-instancegroupconfig-ebsconfiguration"></a>
EBS configurations that will be attached to each EC2 instance in the instance group\.  
*Required*: No  
*Type*: [EbsConfiguration](aws-properties-elasticmapreduce-cluster-ebsconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceCount`  <a name="cfn-elasticmapreduce-cluster-instancegroupconfig-instancecount"></a>
Target number of instances for the instance group\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-elasticmapreduce-cluster-instancegroupconfig-instancetype"></a>
The EC2 instance type for all instances in the instance group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Market`  <a name="cfn-elasticmapreduce-cluster-instancegroupconfig-market"></a>
Market type of the EC2 instances used to create a cluster node\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ON_DEMAND | SPOT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-elasticmapreduce-cluster-instancegroupconfig-name"></a>
Friendly name given to the instance group\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)