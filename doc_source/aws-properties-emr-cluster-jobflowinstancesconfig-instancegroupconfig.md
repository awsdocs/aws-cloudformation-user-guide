# Amazon EMR Cluster InstanceGroupConfig<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig"></a>

`InstanceGroupConfig` is a property of the `CoreInstanceGroup` and `MasterInstanceGroup` properties of the job flow instances configuration\. The `InstanceGroupConfig` property specifies the settings for instances \(nodes\) in the core and master instance groups of an Amazon EMR cluster\.

## Syntax<a name="w3ab2c21c14d898b5"></a>

### JSON<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy)" : AutoScalingPolicy,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-bidprice)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-configurations)" : [ Configuration, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-ebsconfiguration)" : EBSConfiguration,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-instancecount)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-instancetype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-market)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-name)" : String
}
```

### YAML<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy): 
  AutoScalingPolicy
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-bidprice): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-configurations):
  - Configuration
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-ebsconfiguration):
  EBSConfiguration
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-instancecount): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-instancetype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-market): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-name): String
```

## Properties<a name="w3ab2c21c14d898b7"></a>

`AutoScalingPolicy`  
An automatic scaling policy for a core instance group or task instance group in an Amazon EMR cluster\. An automatic scaling policy defines how an instance group dynamically adds and terminates EC2 instances in response to the value of a CloudWatch metric\.  
*Required: *No  
*Update requires*: No interruption  
*Type*: [Amazon EMR Cluster AutoScalingPolicy](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy.md)

`BidPrice`  
When launching instances as Spot Instances, the bid price in USD for each EC2 instance in the instance group\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Configurations`  
A list of configurations to apply to this instance group\. For more information see, [Configuring Applications](http://docs.aws.amazon.com//ElasticMapReduce/latest/ReleaseGuide/emr-configure-apps.html) in the *Amazon EMR Release Guide*\.  
*Required: *No  
*Type*: List of [Amazon EMR Cluster Configurations](aws-properties-emr-cluster-configuration.md)  
*Update requires*: Replacement

`EbsConfiguration`  
Configures Amazon Elastic Block Store \(Amazon EBS\) storage volumes to attach to your instances\.  
*Required: *No  
*Type*: [Amazon EMR EbsConfiguration](aws-properties-emr-ebsconfiguration.md)  
*Update requires*: Replacement

`InstanceCount`  
The number of instances to launch in the instance group\.  
*Required: *Yes  
*Type*: Integer

`InstanceType`  
The EC2 instance type for all instances in the instance group\. For more information, see [Instance Configurations](http://docs.aws.amazon.com//ElasticMapReduce/latest/ManagementGuide/emr-plan-ec2-instances.html) in the *Amazon EMR Management Guide*\.  
*Required: *Yes  
*Type*: String

`Market`  
The type of marketplace from which your instances are provisioned into this group, either `ON_DEMAND` or `SPOT`\. For more information, see [Amazon EC2 Purchasing Options](https://aws.amazon.com/ec2/purchasing-options/)\.  
*Required: *No  
*Type*: String

`Name`  
A name for the instance group\.  
*Required: *No  
*Type*: String