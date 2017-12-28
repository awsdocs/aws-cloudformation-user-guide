# Amazon EMR Cluster JobFlowInstancesConfig<a name="aws-properties-emr-cluster-jobflowinstancesconfig"></a>

Use the`JobFlowInstancesConfig`, which is a property of the [AWS::EMR::Cluster](aws-resource-emr-cluster.md) resource, to configure the EC2 instances \(nodes\) that will run jobs in an Amazon EMR cluster\.

**Note**  
When creating your cluster using `EmrManagedMasterSecurityGroup` and `EmrManagedSlaveSecurityGroup`, to avoid a `delete_failed` exception, use security groups created outside of the AWS CloudFormation stack or retain them on deletion\.

## Syntax<a name="w3ab2c21c14d907b7"></a>

### JSON<a name="aws-properties-emr-cluster-jobflowinstancesconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-additionalmastersecuritygroups)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-additionalslavesecuritygroups)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancefleet)" : InstanceFleetConfig,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-coreinstancegroup)" : InstanceGroupConfig,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-ec2keyname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-ec2subnetid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-emrmanagedmastersecuritygroup)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-emrmanagedslavesecuritygroup)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-hadoopversion)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancefleet)" : InstanceFleetConfig,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-masterinstancegroup)" : InstanceGroupConfig,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-placement)" : Placement,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-serviceaccesssecuritygroup)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-terminationprotected)" : Boolean
}
```

### YAML<a name="aws-properties-emr-cluster-jobflowinstancesconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-additionalmastersecuritygroups):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-additionalslavesecuritygroups):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancefleet):
  InstanceFleetConfig,
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-coreinstancegroup):
  InstanceGroupConfig
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-ec2keyname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-ec2subnetid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-emrmanagedmastersecuritygroup): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-emrmanagedslavesecuritygroup): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-hadoopversion): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancefleet):
  InstanceFleetConfig
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-masterinstancegroup):
  InstanceGroupConfig
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-placement):
  Placement
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-serviceaccesssecuritygroup): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-terminationprotected): Boolean
```

## Properties<a name="w3ab2c21c14d907b9"></a>

`AdditionalMasterSecurityGroups`  
A list of additional EC2 security group IDs to assign to the master instance \(master node\) in your Amazon EMR cluster\. Use this property to supplement the rules specified by the Amazon EMR managed master security group\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: Replacement

`AdditionalSlaveSecurityGroups`  
A list of additional EC2 security group IDs to assign to the slave instances \(slave nodes\) in your Amazon EMR cluster\. Use this property to supplement the rules specified by the Amazon EMR managed slave security group\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: Replacement

`CoreInstanceFleet`  
The instance fleet settings for the core instances in your Amazon EMR cluster\. Use this property with the `MasterInstanceFleet` property\.  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.
*Required: *No  
*Type*: [Amazon EMR Cluster InstanceFleetConfig](aws-properties-elasticmapreduce-cluster-instancefleetconfig.md)  
*Update requires*: Replacement

`CoreInstanceGroup`  
The settings for the core instances in your Amazon EMR cluster\. Use this property with the `MasterInstanceGroup` property\.  
*Required: *No  
*Type*: [Amazon EMR Cluster InstanceGroupConfig](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig.md)  
*Update requires*: Replacement

`Ec2KeyName`  
The name of an Amazon Elastic Compute Cloud \(Amazon EC2\) key pair, which you can use to access the instances in your Amazon EMR cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Ec2SubnetId`  
The ID of the subnet where you want to launch your instances\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`EmrManagedMasterSecurityGroup`  
The ID of an EC2 security group \(managed by Amazon EMR\) that is assigned to the master instance \(master node\) in your Amazon EMR cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`EmrManagedSlaveSecurityGroup`  
The ID of an EC2 security group \(managed by Amazon EMR\) that is assigned to the slave instances \(slave nodes\) in your Amazon EMR cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`HadoopVersion`  
The Hadoop version for the job flow\. For valid values, see the [HadoopVersion](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_JobFlowInstancesConfig.html) parameter in the *Amazon EMR API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`MasterInstanceFleet`  
The instance fleet settings for the master instance \(master node\)\.  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.
You must use either `MasterInstanceFleet` or `MasterInstanceGroup` in your configuration\. If you use `MasterInstanceFleet`, then you may also specify the `CoreInstanceFleet` property\.  
*Required: *No  
*Type*: [Amazon EMR Cluster InstanceFleetConfig](aws-properties-elasticmapreduce-cluster-instancefleetconfig.md)  
*Update requires*: Replacement

`MasterInstanceGroup`  
The settings for the master instance \(master node\)\.  
You must use either `MasterInstanceGroup` or `MasterInstanceFleet` in your configuration\. If you use `MasterInstanceGroup`, then you may also specify the `CoreInstanceGroup` property\.  
*Required: *No  
*Type*: [Amazon EMR Cluster InstanceGroupConfig](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig.md)  
*Update requires*: Replacement

`Placement`  
The Availability Zone \(AZ\) in which the job flow runs\.  
*Required: *No  
*Type*: [Amazon EMR Cluster PlacementType](aws-properties-emr-cluster-jobflowinstancesconfig-placementtype.md)  
*Update requires*: Replacement

`ServiceAccessSecurityGroup`  
The ID of the EC2 security group \(managed by Amazon EMR\) that services use to access clusters in private subnets\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`TerminationProtected`  
Indicates whether to prevent the EC2 instances from being terminated by an API call or user intervention\. If you want to delete a stack with protected instances, update this value to `false` before you delete the stack\. By default, AWS CloudFormation sets this property to `false`\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption