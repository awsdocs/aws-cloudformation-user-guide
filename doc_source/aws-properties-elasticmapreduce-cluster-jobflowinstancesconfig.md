# AWS::EMR::Cluster JobFlowInstancesConfig<a name="aws-properties-elasticmapreduce-cluster-jobflowinstancesconfig"></a>

`JobFlowInstancesConfig` is a property of the `AWS::EMR::Cluster` resource\. `JobFlowInstancesConfig` defines the instance groups or instance fleets that comprise the cluster\. `JobFlowInstancesConfig` must contain either `InstanceFleetConfig` or `InstanceGroupConfig`\. They cannot be used together\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-jobflowinstancesconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-jobflowinstancesconfig-syntax.json"></a>

```
{
  "[AdditionalMasterSecurityGroups](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-additionalmastersecuritygroups)" : [ String, ... ],
  "[AdditionalSlaveSecurityGroups](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-additionalslavesecuritygroups)" : [ String, ... ],
  "[CoreInstanceFleet](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancefleet)" : InstanceFleetConfig,
  "[CoreInstanceGroup](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancegroup)" : InstanceGroupConfig,
  "[Ec2KeyName](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-ec2keyname)" : String,
  "[Ec2SubnetId](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-ec2subnetid)" : String,
  "[Ec2SubnetIds](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-ec2subnetids)" : [ String, ... ],
  "[EmrManagedMasterSecurityGroup](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-emrmanagedmastersecuritygroup)" : String,
  "[EmrManagedSlaveSecurityGroup](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-emrmanagedslavesecuritygroup)" : String,
  "[HadoopVersion](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-hadoopversion)" : String,
  "[KeepJobFlowAliveWhenNoSteps](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-keepjobflowalivewhennosteps)" : Boolean,
  "[MasterInstanceFleet](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancefleet)" : InstanceFleetConfig,
  "[MasterInstanceGroup](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancegroup)" : InstanceGroupConfig,
  "[Placement](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-placement)" : PlacementType,
  "[ServiceAccessSecurityGroup](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-serviceaccesssecuritygroup)" : String,
  "[TerminationProtected](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-terminationprotected)" : Boolean
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-jobflowinstancesconfig-syntax.yaml"></a>

```
  [AdditionalMasterSecurityGroups](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-additionalmastersecuritygroups): 
    - String
  [AdditionalSlaveSecurityGroups](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-additionalslavesecuritygroups): 
    - String
  [CoreInstanceFleet](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancefleet): 
    InstanceFleetConfig
  [CoreInstanceGroup](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancegroup): 
    InstanceGroupConfig
  [Ec2KeyName](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-ec2keyname): String
  [Ec2SubnetId](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-ec2subnetid): String
  [Ec2SubnetIds](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-ec2subnetids): 
    - String
  [EmrManagedMasterSecurityGroup](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-emrmanagedmastersecuritygroup): String
  [EmrManagedSlaveSecurityGroup](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-emrmanagedslavesecuritygroup): String
  [HadoopVersion](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-hadoopversion): String
  [KeepJobFlowAliveWhenNoSteps](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-keepjobflowalivewhennosteps): Boolean
  [MasterInstanceFleet](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancefleet): 
    InstanceFleetConfig
  [MasterInstanceGroup](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancegroup): 
    InstanceGroupConfig
  [Placement](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-placement): 
    PlacementType
  [ServiceAccessSecurityGroup](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-serviceaccesssecuritygroup): String
  [TerminationProtected](#cfn-elasticmapreduce-cluster-jobflowinstancesconfig-terminationprotected): Boolean
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-jobflowinstancesconfig-properties"></a>

`AdditionalMasterSecurityGroups`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-additionalmastersecuritygroups"></a>
A list of additional Amazon EC2 security group IDs for the master node\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AdditionalSlaveSecurityGroups`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-additionalslavesecuritygroups"></a>
A list of additional Amazon EC2 security group IDs for the core and task nodes\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CoreInstanceFleet`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancefleet"></a>
Describes the EC2 instances and instance configurations for the core instance fleet when using clusters with the instance fleet configuration\.  
*Required*: No  
*Type*: [InstanceFleetConfig](aws-properties-elasticmapreduce-cluster-instancefleetconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CoreInstanceGroup`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-coreinstancegroup"></a>
Describes the EC2 instances and instance configurations for core instance groups when using clusters with the uniform instance group configuration\.  
*Required*: No  
*Type*: [InstanceGroupConfig](aws-properties-elasticmapreduce-cluster-instancegroupconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ec2KeyName`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-ec2keyname"></a>
The name of the EC2 key pair that can be used to connect to the master node using SSH as the user called "hadoop\."  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ec2SubnetId`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-ec2subnetid"></a>
Applies to clusters that use the uniform instance group configuration\. To launch the cluster in Amazon Virtual Private Cloud \(Amazon VPC\), set this parameter to the identifier of the Amazon VPC subnet where you want the cluster to launch\. If you do not specify this value and your account supports EC2\-Classic, the cluster launches in EC2\-Classic\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ec2SubnetIds`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-ec2subnetids"></a>
Applies to clusters that use the instance fleet configuration\. When multiple EC2 subnet IDs are specified, Amazon EMR evaluates them and launches instances in the optimal subnet\.  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EmrManagedMasterSecurityGroup`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-emrmanagedmastersecuritygroup"></a>
The identifier of the Amazon EC2 security group for the master node\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EmrManagedSlaveSecurityGroup`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-emrmanagedslavesecuritygroup"></a>
The identifier of the Amazon EC2 security group for the core and task nodes\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HadoopVersion`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-hadoopversion"></a>
Applies only to Amazon EMR release versions earlier than 4\.0\. The Hadoop version for the cluster\. Valid inputs are "0\.18" \(no longer maintained\), "0\.20" \(no longer maintained\), "0\.20\.205" \(no longer maintained\), "1\.0\.3", "2\.2\.0", or "2\.4\.0"\. If you do not set this value, the default of 0\.18 is used, unless the `AmiVersion` parameter is set in the RunJobFlow call, in which case the default version of Hadoop for that AMI version is used\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeepJobFlowAliveWhenNoSteps`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-keepjobflowalivewhennosteps"></a>
Specifies whether the cluster should remain available after completing all steps\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterInstanceFleet`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancefleet"></a>
Describes the EC2 instances and instance configurations for the master instance fleet when using clusters with the instance fleet configuration\.  
*Required*: No  
*Type*: [InstanceFleetConfig](aws-properties-elasticmapreduce-cluster-instancefleetconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterInstanceGroup`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-masterinstancegroup"></a>
Describes the EC2 instances and instance configurations for the master instance group when using clusters with the uniform instance group configuration\.  
*Required*: No  
*Type*: [InstanceGroupConfig](aws-properties-elasticmapreduce-cluster-instancegroupconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Placement`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-placement"></a>
The Availability Zone in which the cluster runs\.  
*Required*: No  
*Type*: [PlacementType](aws-properties-elasticmapreduce-cluster-placementtype.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceAccessSecurityGroup`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-serviceaccesssecuritygroup"></a>
The identifier of the Amazon EC2 security group for the Amazon EMR service to access clusters in VPC private subnets\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TerminationProtected`  <a name="cfn-elasticmapreduce-cluster-jobflowinstancesconfig-terminationprotected"></a>
Specifies whether to lock the cluster to prevent the Amazon EC2 instances from being terminated by API call, user intervention, or in the event of a job\-flow error\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)