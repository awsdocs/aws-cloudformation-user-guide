# AWS::EMR::InstanceGroupConfig<a name="aws-resource-emr-instancegroupconfig"></a>

The `AWS::EMR::InstanceGroupConfig` resource configures a task instance group for an Amazon EMR cluster\.

**Note**  
You can't delete an instance group\. If you remove an instance group, AWS CloudFormation sets the instance count to zero \(`0`\)\.


+ [Syntax](#aws-resource-emr-instancegroupconfig-syntax)
+ [Properties](#w3ab2c21c10d626c11)
+ [Return Values](#w3ab2c21c10d626c13)
+ [Example](#w3ab2c21c10d626c15)

## Syntax<a name="aws-resource-emr-instancegroupconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-emr-instancegroupconfig-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::InstanceGroupConfig",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy)" : AutoScalingPolicy,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-bidprice)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-configurations)" : [ Configuration, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-ebsconfiguration)" : EBSConfiguration,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-instancecount)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-instancerole)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-instancetype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-jobflowid)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-market)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-name)" : String
  }
}
```

### YAML<a name="aws-resource-emr-instancegroupconfig-syntax.yaml"></a>

```
Type: "AWS::EMR::InstanceGroupConfig"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy):
    AutoScalingPolicy
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-bidprice): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-configurations):
    - Configuration
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-ebsconfiguration)" :
    EBSConfiguration
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-instancecount)" : Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-instancerole)" : String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-instancetype)" : String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-jobflowid)": String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-market)" : String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-instancegroupconfig-name)" : String
```

## Properties<a name="w3ab2c21c10d626c11"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [InstanceGroupConfig](http://docs.aws.amazon.com//ElasticMapReduce/latest/API/API_InstanceGroupConfig.html) in the Amazon EMR API Reference\.

`AutoScalingPolicy`  
An automatic scaling policy for a core instance group or task instance group in an Amazon EMR cluster\. An automatic scaling policy defines how an instance group dynamically adds and terminates EC2 instances in response to the value of a CloudWatch metric\. For more information, see [PutAutoScalingPolicy](http://docs.aws.amazon.com//ElasticMapReduce/latest/API/API_PutAutoScalingPolicy.html) in the Amazon EMR API Reference\.   
*Required: *No  
*Type*: [Amazon EMR InstanceGroupConfig AutoScalingPolicy](aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy.md)  
*Update requires*: No interruption

`BidPrice`  
The bid price in USD for each Amazon EC2 instance in the instance group when launching instances \(nodes\) as Spot Instances\.  
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
*Update requires*: No interruption

`InstanceRole`  
The role of the servers in the Amazon EMR cluster, such as `TASK`\. For more information, see [Instance Groups](http://docs.aws.amazon.com//ElasticMapReduce/latest/ManagementGuide/InstanceGroups.html) in the *Amazon EMR Management Guide*\.  
Currently, the only valid value is `TASK`\. You configure the master and core instance groups as part of the [AWS::EMR::Cluster](aws-resource-emr-cluster.md) resource\.
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`InstanceType`  
The EC2 instance type for all instances in the instance group\. For more information, see [Instance Configurations](http://docs.aws.amazon.com//ElasticMapReduce/latest/ManagementGuide/emr-plan-ec2-instances.html) in the *Amazon EMR Management Guide*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`JobFlowId`  
The ID of an Amazon EMR cluster that you want to associate this instance group with\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Market`  
The type of marketplace from which your instances are provisioned into this group, either `ON_DEMAND` or `SPOT`\. For more information, see [Amazon EC2 Purchasing Options](https://aws.amazon.com/ec2/purchasing-options/)\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Name`  
A name for the instance group\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

## Return Values<a name="w3ab2c21c10d626c13"></a>

### Ref<a name="w3ab2c21c10d626c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the instance group ID, such as `ig-ABC12DEF3456`\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d626c15"></a>

The following example adds a task instance group to the `TestCluster` cluster\. The instance group contains two m3\.xlarge instances\.

### JSON<a name="aws-resource-emr-instancegroupconfig-example.json"></a>

```
"TestInstanceGroupConfig": {
  "Type": "AWS::EMR::InstanceGroupConfig",
  "Properties": {
    "InstanceCount": 2,
    "InstanceType": "m3.xlarge",
    "InstanceRole": "TASK",
    "Market": "ON_DEMAND",
    "Name": "cfnTask2",
    "JobFlowId": {
      "Ref": "cluster"
    }
  }
}
```

### YAML<a name="aws-resource-emr-instancegroupconfig-example.yaml"></a>

```
TestInstanceGroupConfig: 
  Type: "AWS::EMR::InstanceGroupConfig"
  Properties: 
    InstanceCount: 2
    InstanceType: "m3.xlarge"
    InstanceRole: "TASK"
    Market: "ON_DEMAND"
    Name: "cfnTask2"
    JobFlowId: 
      Ref: "cluster"
```