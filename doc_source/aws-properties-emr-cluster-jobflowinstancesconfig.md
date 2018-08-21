# Amazon EMR Cluster JobFlowInstancesConfig<a name="aws-properties-emr-cluster-jobflowinstancesconfig"></a>

Use the`JobFlowInstancesConfig`, which is a property of the [AWS::EMR::Cluster](aws-resource-emr-cluster.md) resource, to configure the EC2 instances \(nodes\) that will run jobs in an Amazon EMR cluster\.

**Note**  
When creating your cluster using `EmrManagedMasterSecurityGroup` and `EmrManagedSlaveSecurityGroup`, to avoid a `delete_failed` exception, use security groups created outside of the AWS CloudFormation stack or retain them on deletion\.

## Syntax<a name="w3ab2c21c14e1098b7"></a>

### JSON<a name="aws-properties-emr-cluster-jobflowinstancesconfig-syntax.json"></a>

```
{
  "[AdditionalMasterSecurityGroups](#cfn-emr-cluster-jobflowinstancesconfig-additionalmastersecuritygroups)" : [ String, ... ],
  "[AdditionalSlaveSecurityGroups](#cfn-emr-cluster-jobflowinstancesconfig-additionalslavesecuritygroups)" : [ String, ... ],
  "[CoreInstanceFleet](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancefleet)" : InstanceFleetConfig,
  "[CoreInstanceGroup](#cfn-emr-cluster-jobflowinstancesconfig-coreinstancegroup)" : InstanceGroupConfig,
  "[Ec2KeyName](#cfn-emr-cluster-jobflowinstancesconfig-ec2keyname)" : String,
  "[Ec2SubnetId](#cfn-emr-cluster-jobflowinstancesconfig-ec2subnetid)" : String,
  "[EmrManagedMasterSecurityGroup](#cfn-emr-cluster-jobflowinstancesconfig-emrmanagedmastersecuritygroup)" : String,
  "[EmrManagedSlaveSecurityGroup](#cfn-emr-cluster-jobflowinstancesconfig-emrmanagedslavesecuritygroup)" : String,
  "[HadoopVersion](#cfn-emr-cluster-jobflowinstancesconfig-hadoopversion)" : String,
  "[MasterInstanceFleet](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancefleet)" : InstanceFleetConfig,
  "[MasterInstanceGroup](#cfn-emr-cluster-jobflowinstancesconfig-masterinstancegroup)" : InstanceGroupConfig,
  "[Placement](#cfn-emr-cluster-jobflowinstancesconfig-placement)" : Placement,
  "[ServiceAccessSecurityGroup](#cfn-emr-cluster-jobflowinstancesconfig-serviceaccesssecuritygroup)" : String,
  "[TerminationProtected](#cfn-emr-cluster-jobflowinstancesconfig-terminationprotected)" : Boolean
}
```

### YAML<a name="aws-properties-emr-cluster-jobflowinstancesconfig-syntax.yaml"></a>

```
[AdditionalMasterSecurityGroups](#cfn-emr-cluster-jobflowinstancesconfig-additionalmastersecuritygroups):
  - String
[AdditionalSlaveSecurityGroups](#cfn-emr-cluster-jobflowinstancesconfig-additionalslavesecuritygroups):
  - String
[CoreInstanceFleet](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancefleet):
  InstanceFleetConfig,
[CoreInstanceGroup](#cfn-emr-cluster-jobflowinstancesconfig-coreinstancegroup):
  InstanceGroupConfig
[Ec2KeyName](#cfn-emr-cluster-jobflowinstancesconfig-ec2keyname): String
[Ec2SubnetId](#cfn-emr-cluster-jobflowinstancesconfig-ec2subnetid): String
[EmrManagedMasterSecurityGroup](#cfn-emr-cluster-jobflowinstancesconfig-emrmanagedmastersecuritygroup): String
[EmrManagedSlaveSecurityGroup](#cfn-emr-cluster-jobflowinstancesconfig-emrmanagedslavesecuritygroup): String
[HadoopVersion](#cfn-emr-cluster-jobflowinstancesconfig-hadoopversion): String
[MasterInstanceFleet](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancefleet):
  InstanceFleetConfig
[MasterInstanceGroup](#cfn-emr-cluster-jobflowinstancesconfig-masterinstancegroup):
  InstanceGroupConfig
[Placement](#cfn-emr-cluster-jobflowinstancesconfig-placement):
  Placement
[ServiceAccessSecurityGroup](#cfn-emr-cluster-jobflowinstancesconfig-serviceaccesssecuritygroup): String
[TerminationProtected](#cfn-emr-cluster-jobflowinstancesconfig-terminationprotected): Boolean
```

## Properties<a name="w3ab2c21c14e1098b9"></a>

`AdditionalMasterSecurityGroups`  <a name="cfn-emr-cluster-jobflowinstancesconfig-additionalmastersecuritygroups"></a>
A list of additional EC2 security group IDs to assign to the master instance \(master node\) in your Amazon EMR cluster\. Use this property to supplement the rules specified by the Amazon EMR managed master security group\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`AdditionalSlaveSecurityGroups`  <a name="cfn-emr-cluster-jobflowinstancesconfig-additionalslavesecuritygroups"></a>
A list of additional EC2 security group IDs to assign to the slave instances \(slave nodes\) in your Amazon EMR cluster\. Use this property to supplement the rules specified by the Amazon EMR managed slave security group\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`CoreInstanceFleet`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancefleet"></a>
The instance fleet settings for the core instances in your Amazon EMR cluster\. Use this property with the `MasterInstanceFleet` property\.  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.
*Required*: No  
*Type*: [Amazon EMR Cluster InstanceFleetConfig](aws-properties-elasticmapreduce-cluster-instancefleetconfig.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`CoreInstanceGroup`  <a name="cfn-emr-cluster-jobflowinstancesconfig-coreinstancegroup"></a>
The settings for the core instances in your Amazon EMR cluster\. Use this property with the `MasterInstanceGroup` property\.  
*Required*: No  
*Type*: [Amazon EMR Cluster InstanceGroupConfig](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Ec2KeyName`  <a name="cfn-emr-cluster-jobflowinstancesconfig-ec2keyname"></a>
The name of an Amazon Elastic Compute Cloud \(Amazon EC2\) key pair, which you can use to access the instances in your Amazon EMR cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Ec2SubnetId`  <a name="cfn-emr-cluster-jobflowinstancesconfig-ec2subnetid"></a>
The ID of the subnet where you want to launch your instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EmrManagedMasterSecurityGroup`  <a name="cfn-emr-cluster-jobflowinstancesconfig-emrmanagedmastersecuritygroup"></a>
The ID of an EC2 security group \(managed by Amazon EMR\) that is assigned to the master instance \(master node\) in your Amazon EMR cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EmrManagedSlaveSecurityGroup`  <a name="cfn-emr-cluster-jobflowinstancesconfig-emrmanagedslavesecuritygroup"></a>
The ID of an EC2 security group \(managed by Amazon EMR\) that is assigned to the slave instances \(slave nodes\) in your Amazon EMR cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`HadoopVersion`  <a name="cfn-emr-cluster-jobflowinstancesconfig-hadoopversion"></a>
The Hadoop version for the job flow\. For valid values, see the [HadoopVersion](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_JobFlowInstancesConfig.html) parameter in the *Amazon EMR API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`MasterInstanceFleet`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancefleet"></a>
The instance fleet settings for the master instance \(master node\)\.  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.
You must use either `MasterInstanceFleet` or `MasterInstanceGroup` in your configuration\. If you use `MasterInstanceFleet`, then you may also specify the `CoreInstanceFleet` property\.  
*Required*: No  
*Type*: [Amazon EMR Cluster InstanceFleetConfig](aws-properties-elasticmapreduce-cluster-instancefleetconfig.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`MasterInstanceGroup`  <a name="cfn-emr-cluster-jobflowinstancesconfig-masterinstancegroup"></a>
The settings for the master instance \(master node\)\.  
You must use either `MasterInstanceGroup` or `MasterInstanceFleet` in your configuration\. If you use `MasterInstanceGroup`, then you may also specify the `CoreInstanceGroup` property\.  
*Required*: No  
*Type*: [Amazon EMR Cluster InstanceGroupConfig](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Placement`  <a name="cfn-emr-cluster-jobflowinstancesconfig-placement"></a>
The Availability Zone \(AZ\) in which the job flow runs\.  
*Required*: No  
*Type*: [Amazon EMR Cluster PlacementType](aws-properties-emr-cluster-jobflowinstancesconfig-placementtype.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ServiceAccessSecurityGroup`  <a name="cfn-emr-cluster-jobflowinstancesconfig-serviceaccesssecuritygroup"></a>
The ID of the EC2 security group \(managed by Amazon EMR\) that services use to access clusters in private subnets\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TerminationProtected`  <a name="cfn-emr-cluster-jobflowinstancesconfig-terminationprotected"></a>
Indicates whether to prevent the EC2 instances from being terminated by an API call or user intervention\. If you want to delete a stack with protected instances, update this value to `false` before you delete the stack\. By default, AWS CloudFormation sets this property to `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)