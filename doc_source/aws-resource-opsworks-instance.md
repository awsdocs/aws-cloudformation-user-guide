# AWS::OpsWorks::Instance<a name="aws-resource-opsworks-instance"></a>

Creates an instance in a specified stack\. For more information, see [Adding an Instance to a Layer](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-add.html)\.

 **Required Permissions**: To use this action, an IAM user must have a Manage permissions level for the stack, or an attached policy that explicitly grants permissions\. For more information on user permissions, see [Managing User Permissions](https://docs.aws.amazon.com/opsworks/latest/userguide/opsworks-security-users.html)\.

## Syntax<a name="aws-resource-opsworks-instance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-instance-syntax.json"></a>

```
{
  "Type" : "AWS::OpsWorks::Instance",
  "Properties" : {
      "[AgentVersion](#cfn-opsworks-instance-agentversion)" : String,
      "[AmiId](#cfn-opsworks-instance-amiid)" : String,
      "[Architecture](#cfn-opsworks-instance-architecture)" : String,
      "[AutoScalingType](#cfn-opsworks-instance-autoscalingtype)" : String,
      "[AvailabilityZone](#cfn-opsworks-instance-availabilityzone)" : String,
      "[BlockDeviceMappings](#cfn-opsworks-instance-blockdevicemappings)" : [ BlockDeviceMapping, ... ],
      "[EbsOptimized](#cfn-opsworks-instance-ebsoptimized)" : Boolean,
      "[ElasticIps](#cfn-opsworks-instance-elasticips)" : [ String, ... ],
      "[Hostname](#cfn-opsworks-instance-hostname)" : String,
      "[InstallUpdatesOnBoot](#cfn-opsworks-instance-installupdatesonboot)" : Boolean,
      "[InstanceType](#cfn-opsworks-instance-instancetype)" : String,
      "[LayerIds](#cfn-opsworks-instance-layerids)" : [ String, ... ],
      "[Os](#cfn-opsworks-instance-os)" : String,
      "[RootDeviceType](#cfn-opsworks-instance-rootdevicetype)" : String,
      "[SshKeyName](#cfn-opsworks-instance-sshkeyname)" : String,
      "[StackId](#cfn-opsworks-instance-stackid)" : String,
      "[SubnetId](#cfn-opsworks-instance-subnetid)" : String,
      "[Tenancy](#cfn-opsworks-instance-tenancy)" : String,
      "[TimeBasedAutoScaling](#cfn-opsworks-instance-timebasedautoscaling)" : TimeBasedAutoScaling,
      "[VirtualizationType](#cfn-opsworks-instance-virtualizationtype)" : String,
      "[Volumes](#cfn-opsworks-instance-volumes)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-opsworks-instance-syntax.yaml"></a>

```
Type: AWS::OpsWorks::Instance
Properties: 
  [AgentVersion](#cfn-opsworks-instance-agentversion): String
  [AmiId](#cfn-opsworks-instance-amiid): String
  [Architecture](#cfn-opsworks-instance-architecture): String
  [AutoScalingType](#cfn-opsworks-instance-autoscalingtype): String
  [AvailabilityZone](#cfn-opsworks-instance-availabilityzone): String
  [BlockDeviceMappings](#cfn-opsworks-instance-blockdevicemappings): 
    - BlockDeviceMapping
  [EbsOptimized](#cfn-opsworks-instance-ebsoptimized): Boolean
  [ElasticIps](#cfn-opsworks-instance-elasticips): 
    - String
  [Hostname](#cfn-opsworks-instance-hostname): String
  [InstallUpdatesOnBoot](#cfn-opsworks-instance-installupdatesonboot): Boolean
  [InstanceType](#cfn-opsworks-instance-instancetype): String
  [LayerIds](#cfn-opsworks-instance-layerids): 
    - String
  [Os](#cfn-opsworks-instance-os): String
  [RootDeviceType](#cfn-opsworks-instance-rootdevicetype): String
  [SshKeyName](#cfn-opsworks-instance-sshkeyname): String
  [StackId](#cfn-opsworks-instance-stackid): String
  [SubnetId](#cfn-opsworks-instance-subnetid): String
  [Tenancy](#cfn-opsworks-instance-tenancy): String
  [TimeBasedAutoScaling](#cfn-opsworks-instance-timebasedautoscaling): 
    TimeBasedAutoScaling
  [VirtualizationType](#cfn-opsworks-instance-virtualizationtype): String
  [Volumes](#cfn-opsworks-instance-volumes): 
    - String
```

## Properties<a name="aws-resource-opsworks-instance-properties"></a>

`AgentVersion`  <a name="cfn-opsworks-instance-agentversion"></a>
The default AWS OpsWorks Stacks agent version\. You have the following options:  
+  `INHERIT` \- Use the stack's default agent version setting\.
+  *version\_number* \- Use the specified agent version\. This value overrides the stack's default setting\. To update the agent version, edit the instance configuration and specify a new version\. AWS OpsWorks Stacks then automatically installs that version on the instance\.
The default setting is `INHERIT`\. To specify an agent version, you must use the complete version number, not the abbreviated number shown on the console\. For a list of available agent version numbers, call [DescribeAgentVersions](https://docs.aws.amazon.com/goto/WebAPI/opsworks-2013-02-18/DescribeAgentVersions)\. AgentVersion cannot be set to Chef 12\.2\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AmiId`  <a name="cfn-opsworks-instance-amiid"></a>
A custom AMI ID to be used to create the instance\. The AMI should be based on one of the supported operating systems\. For more information, see [Using Custom AMIs](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-custom-ami.html)\.  
If you specify a custom AMI, you must set `Os` to `Custom`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Architecture`  <a name="cfn-opsworks-instance-architecture"></a>
The instance architecture\. The default option is `x86_64`\. Instance types do not necessarily support both architectures\. For a list of the architectures that are supported by the different instance types, see [Instance Families and Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `i386 | x86_64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoScalingType`  <a name="cfn-opsworks-instance-autoscalingtype"></a>
For load\-based or time\-based instances, the type\. Windows stacks can use only time\-based instances\.  
*Required*: No  
*Type*: String  
*Allowed values*: `load | timer`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AvailabilityZone`  <a name="cfn-opsworks-instance-availabilityzone"></a>
The Availability Zone of the AWS OpsWorks instance, such as `us-east-2a`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BlockDeviceMappings`  <a name="cfn-opsworks-instance-blockdevicemappings"></a>
An array of `BlockDeviceMapping` objects that specify the instance's block devices\. For more information, see [Block Device Mapping](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/block-device-mapping-concepts.html)\. Note that block device mappings are not supported for custom AMIs\.  
*Required*: No  
*Type*: List of [BlockDeviceMapping](aws-properties-opsworks-instance-blockdevicemapping.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EbsOptimized`  <a name="cfn-opsworks-instance-ebsoptimized"></a>
Whether to create an Amazon EBS\-optimized instance\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ElasticIps`  <a name="cfn-opsworks-instance-elasticips"></a>
A list of Elastic IP addresses to associate with the instance\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Hostname`  <a name="cfn-opsworks-instance-hostname"></a>
The instance host name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstallUpdatesOnBoot`  <a name="cfn-opsworks-instance-installupdatesonboot"></a>
Whether to install operating system and package updates when the instance boots\. The default value is `true`\. To control when updates are installed, set this value to `false`\. You must then update your instances manually by using [CreateDeployment](https://docs.aws.amazon.com/goto/WebAPI/opsworks-2013-02-18/CreateDeployment) to run the `update_dependencies` stack command or by manually running `yum` \(Amazon Linux\) or `apt-get` \(Ubuntu\) on the instances\.   
We strongly recommend using the default value of `true` to ensure that your instances have the latest security updates\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-opsworks-instance-instancetype"></a>
The instance type, such as `t2.micro`\. For a list of supported instance types, open the stack in the console, choose **Instances**, and choose **\+ Instance**\. The **Size** list contains the currently supported types\. For more information, see [Instance Families and Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html)\. The parameter values that you use to specify the various types are in the **API Name** column of the **Available Instance Types** table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LayerIds`  <a name="cfn-opsworks-instance-layerids"></a>
An array that contains the instance's layer IDs\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Os`  <a name="cfn-opsworks-instance-os"></a>
The instance's operating system, which must be set to one of the following\.  
+ A supported Linux operating system: An Amazon Linux version, such as `Amazon Linux 2018.03`, `Amazon Linux 2017.09`, `Amazon Linux 2017.03`, `Amazon Linux 2016.09`, `Amazon Linux 2016.03`, `Amazon Linux 2015.09`, or `Amazon Linux 2015.03`\.
+ A supported Ubuntu operating system, such as `Ubuntu 16.04 LTS`, `Ubuntu 14.04 LTS`, or `Ubuntu 12.04 LTS`\.
+  `CentOS Linux 7` 
+  `Red Hat Enterprise Linux 7` 
+ A supported Windows operating system, such as `Microsoft Windows Server 2012 R2 Base`, `Microsoft Windows Server 2012 R2 with SQL Server Express`, `Microsoft Windows Server 2012 R2 with SQL Server Standard`, or `Microsoft Windows Server 2012 R2 with SQL Server Web`\.
+ A custom AMI: `Custom`\.
For more information about the supported operating systems, see [AWS OpsWorks Stacks Operating Systems](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-os.html)\.  
The default option is the current Amazon Linux version\. If you set this parameter to `Custom`, you must use the [CreateInstance](https://docs.aws.amazon.com/goto/WebAPI/opsworks-2013-02-18/CreateInstance) action's AmiId parameter to specify the custom AMI that you want to use\. Block device mappings are not supported if the value is `Custom`\. For more information about supported operating systems, see [Operating Systems](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-os.html)For more information about how to use custom AMIs with AWS OpsWorks Stacks, see [Using Custom AMIs](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-custom-ami.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RootDeviceType`  <a name="cfn-opsworks-instance-rootdevicetype"></a>
The instance root device type\. For more information, see [Storage for the Root Device](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ComponentsAMIs.html#storage-for-the-root-device)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ebs | instance-store`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SshKeyName`  <a name="cfn-opsworks-instance-sshkeyname"></a>
The instance's Amazon EC2 key\-pair name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackId`  <a name="cfn-opsworks-instance-stackid"></a>
The stack ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-opsworks-instance-subnetid"></a>
The ID of the instance's subnet\. If the stack is running in a VPC, you can use this parameter to override the stack's default subnet ID value and direct AWS OpsWorks Stacks to launch the instance in a different subnet\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tenancy`  <a name="cfn-opsworks-instance-tenancy"></a>
The instance's tenancy option\. The default option is no tenancy, or if the instance is running in a VPC, inherit tenancy settings from the VPC\. The following are valid values for this parameter: `dedicated`, `default`, or `host`\. Because there are costs associated with changes in tenancy options, we recommend that you research tenancy options before choosing them for your instances\. For more information about dedicated hosts, see [Dedicated Hosts Overview](http://aws.amazon.com/ec2/dedicated-hosts/) and [Amazon EC2 Dedicated Hosts](http://aws.amazon.com/ec2/dedicated-hosts/)\. For more information about dedicated instances, see [Dedicated Instances](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/dedicated-instance.html) and [Amazon EC2 Dedicated Instances](http://aws.amazon.com/ec2/purchasing-options/dedicated-instances/)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TimeBasedAutoScaling`  <a name="cfn-opsworks-instance-timebasedautoscaling"></a>
The time\-based scaling configuration for the instance\.  
*Required*: No  
*Type*: [TimeBasedAutoScaling](aws-properties-opsworks-instance-timebasedautoscaling.md)  
*Allowed values*: `load | timer`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VirtualizationType`  <a name="cfn-opsworks-instance-virtualizationtype"></a>
The instance's virtualization type, `paravirtual` or `hvm`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Volumes`  <a name="cfn-opsworks-instance-volumes"></a>
A list of AWS OpsWorks volume IDs to associate with the instance\. For more information, see [AWS::OpsWorks::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-volume.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-opsworks-instance-return-values"></a>

### Ref<a name="aws-resource-opsworks-instance-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myInstance1" }` 

For the AWS OpsWorks instance *myInstance1*, `Ref` returns the AWS OpsWorks instance ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-opsworks-instance-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-opsworks-instance-return-values-fn--getatt-fn--getatt"></a>

`AvailabilityZone`  <a name="AvailabilityZone-fn::getatt"></a>
The Availability Zone of the AWS OpsWorks instance, such as `us-east-2a`\.

`PrivateDnsName`  <a name="PrivateDnsName-fn::getatt"></a>
The private DNS name of the AWS OpsWorks instance\.

`PrivateIp`  <a name="PrivateIp-fn::getatt"></a>
The private IP address of the AWS OpsWorks instance, such as `192.0.2.0`\.

`PublicDnsName`  <a name="PublicDnsName-fn::getatt"></a>
The public DNS name of the AWS OpsWorks instance\.

`PublicIp`  <a name="PublicIp-fn::getatt"></a>
The public IP address of the AWS OpsWorks instance, such as `192.0.2.0`\.  
Use this attribute only when the AWS OpsWorks instance is in an AWS OpsWorks layer that auto\-assigns public IP addresses\.

## Examples<a name="aws-resource-opsworks-instance--examples"></a>

### Create Basic AWS OpsWorks Instances<a name="aws-resource-opsworks-instance--examples--Create_Basic_AWS_OpsWorks_Instances"></a>

The following example creates two AWS OpsWorks instances that are associated with the `myStack` AWS OpsWorks stack and the `myLayer` AWS OpsWorks layer:

#### JSON<a name="aws-resource-opsworks-instance--examples--Create_Basic_AWS_OpsWorks_Instances--json"></a>

```
"myInstance1" : {
  "Type" : "AWS::OpsWorks::Instance",
  "Properties" : {
    "StackId" : {"Ref":"myStack"},
    "LayerIds" : [{"Ref":"myLayer"}],
    "InstanceType" : "m1.small"
  }
},
 
"myInstance2" : {
  "Type" : "AWS::OpsWorks::Instance",
  "Properties" : {
    "StackId" : {"Ref":"myStack"},
    "LayerIds" : [{"Ref":"myLayer"}],
    "InstanceType" : "m1.small"
  }
}
```

#### YAML<a name="aws-resource-opsworks-instance--examples--Create_Basic_AWS_OpsWorks_Instances--yaml"></a>

```
myInstance1: 
  Type: "AWS::OpsWorks::Instance"
  Properties: 
    StackId: 
      Ref: "myStack"
    LayerIds: 
      - 
        Ref: "myLayer"
    InstanceType: "m1.small"
myInstance2: 
  Type: "AWS::OpsWorks::Instance"
  Properties: 
    StackId: 
      Ref: "myStack"
    LayerIds: 
      - 
        Ref: "myLayer"
    InstanceType: "m1.small"
```

### Define a Time\-based Auto Scaling Instance<a name="aws-resource-opsworks-instance--examples--Define_a_Time-based_Auto_Scaling_Instance"></a>

In the following example, the `DBInstance` instance is online for four hours from UTC 1200\-1600 on Friday, Saturday, and Sunday\. The instance is offline for all other times and days\.

#### JSON<a name="aws-resource-opsworks-instance--examples--Define_a_Time-based_Auto_Scaling_Instance--json"></a>

```
"DBInstance" : {
  "Type" : "AWS::OpsWorks::Instance",
  "Properties" : {
    "AutoScalingType" : "timer",
    "StackId" : {"Ref":"Stack"},
    "LayerIds" : [{"Ref":"DBLayer"}],
    "InstanceType" : "m1.small",
    "TimeBasedAutoScaling" : {
      "Friday" : { "12" : "on", "13" : "on", "14" : "on", "15" : "on" },
      "Saturday" : { "12" : "on", "13" : "on", "14" : "on", "15" : "on" },
      "Sunday" : { "12" : "on", "13" : "on", "14" : "on", "15" : "on" }
    }
  }
}
```

#### YAML<a name="aws-resource-opsworks-instance--examples--Define_a_Time-based_Auto_Scaling_Instance--yaml"></a>

```
DBInstance: 
  Type: "AWS::OpsWorks::Instance"
  Properties: 
    AutoScalingType: "timer"
    StackId: 
      Ref: "Stack"
    LayerIds: 
      - Ref: "DBLayer"
    InstanceType: "m1.small"
    TimeBasedAutoScaling: 
      Friday: 
        "12": "on"
        "13": "on"
        "14": "on"
        "15": "on"
      Saturday: 
        "12": "on"
        "13": "on"
        "14": "on"
        "15": "on"
      Sunday: 
        "12": "on"
        "13": "on"
        "14": "on"
        "15": "on"
```

## See also<a name="aws-resource-opsworks-instance--seealso"></a>
+  [CreateInstance](https://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) in the *AWS OpsWorks API Reference*\.
+  [Adding an Instance to a Layer](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-add.html) in the *AWS OpsWorks User Guide*\.

