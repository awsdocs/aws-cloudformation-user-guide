# Amazon EMR Cluster InstanceGroupConfig<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig"></a>

`InstanceGroupConfig` is a property of the `CoreInstanceGroup` and `MasterInstanceGroup` properties of the [job flow instances configuration](aws-properties-emr-cluster-jobflowinstancesconfig.md)\. The `InstanceGroupConfig` property specifies the settings for instances \(nodes\) in the core and master instance groups of an Amazon EMR cluster\.

## Syntax<a name="w3ab2c21c14e1089b5"></a>

### JSON<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-syntax.json"></a>

```
{
  "[AutoScalingPolicy](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy)" : AutoScalingPolicy,
  "[BidPrice](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-bidprice)" : String,
  "[Configurations](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-configurations)" : [ Configuration, ... ],
  "[EbsConfiguration](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-ebsconfiguration)" : EBSConfiguration,
  "[InstanceCount](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-instancecount)" : Integer,
  "[InstanceType](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-instancetype)" : String,
  "[Market](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-market)" : String,
  "[Name](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-name)" : String
}
```

### YAML<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-syntax.yaml"></a>

```
[AutoScalingPolicy](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy): 
  AutoScalingPolicy
[BidPrice](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-bidprice): String
[Configurations](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-configurations):
  - Configuration
[EbsConfiguration](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-ebsconfiguration):
  EBSConfiguration
[InstanceCount](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-instancecount): Integer
[InstanceType](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-instancetype): String
[Market](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-market): String
[Name](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-name): String
```

## Properties<a name="w3ab2c21c14e1089b7"></a>

`AutoScalingPolicy`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy"></a>
An automatic scaling policy for a core instance group or task instance group in an Amazon EMR cluster\. An automatic scaling policy defines how an instance group dynamically adds and terminates EC2 instances in response to the value of a CloudWatch metric\.  
*Required*: No  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
*Type*: [Amazon EMR Cluster AutoScalingPolicy](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy.md)

`BidPrice`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-bidprice"></a>
When launching instances as Spot Instances, the bid price in USD for each EC2 instance in the instance group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Configurations`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-configurations"></a>
A list of configurations to apply to this instance group\. For more information see, [Configuring Applications](http://docs.aws.amazon.com//ElasticMapReduce/latest/ReleaseGuide/emr-configure-apps.html) in the *Amazon EMR Release Guide*\.  
*Required*: No  
*Type*: List of [Amazon EMR Cluster Configurations](aws-properties-emr-cluster-configuration.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EbsConfiguration`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-ebsconfiguration"></a>
Configures Amazon Elastic Block Store \(Amazon EBS\) storage volumes to attach to your instances\.  
*Required*: No  
*Type*: [Amazon EMR EbsConfiguration](aws-properties-emr-ebsconfiguration.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstanceCount`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-instancecount"></a>
The number of instances to launch in the instance group\.  
*Required*: Yes  
*Type*: Integer

`InstanceType`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-instancetype"></a>
The EC2 instance type for all instances in the instance group\. For more information, see [Instance Configurations](http://docs.aws.amazon.com//ElasticMapReduce/latest/ManagementGuide/emr-plan-ec2-instances.html) in the *Amazon EMR Management Guide*\.  
*Required*: Yes  
*Type*: String

`Market`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-market"></a>
The type of marketplace from which your instances are provisioned into this group, either `ON_DEMAND` or `SPOT`\. For more information, see [Amazon EC2 Purchasing Options](https://aws.amazon.com/ec2/purchasing-options/)\.  
*Required*: No  
*Type*: String

`Name`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-name"></a>
A name for the instance group\.  
*Required*: No  
*Type*: String