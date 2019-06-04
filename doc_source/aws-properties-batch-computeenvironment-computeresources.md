# AWS::Batch::ComputeEnvironment ComputeResources<a name="aws-properties-batch-computeenvironment-computeresources"></a>

Details of the compute resources managed by the compute environment\. This parameter is required for managed compute environments\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.

## Syntax<a name="aws-properties-batch-computeenvironment-computeresources-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-computeenvironment-computeresources-syntax.json"></a>

```
{
  "[BidPercentage](#cfn-batch-computeenvironment-computeresources-bidpercentage)" : Integer,
  "[DesiredvCpus](#cfn-batch-computeenvironment-computeresources-desiredvcpus)" : Integer,
  "[Ec2KeyPair](#cfn-batch-computeenvironment-computeresources-ec2keypair)" : String,
  "[ImageId](#cfn-batch-computeenvironment-computeresources-imageid)" : String,
  "[InstanceRole](#cfn-batch-computeenvironment-computeresources-instancerole)" : String,
  "[InstanceTypes](#cfn-batch-computeenvironment-computeresources-instancetypes)" : [ String, ... ],
  "[LaunchTemplate](#cfn-batch-computeenvironment-computeresources-launchtemplate)" : [LaunchTemplateSpecification](aws-properties-batch-computeenvironment-launchtemplatespecification.md),
  "[MaxvCpus](#cfn-batch-computeenvironment-computeresources-maxvcpus)" : Integer,
  "[MinvCpus](#cfn-batch-computeenvironment-computeresources-minvcpus)" : Integer,
  "[PlacementGroup](#cfn-batch-computeenvironment-computeresources-placementgroup)" : String,
  "[SecurityGroupIds](#cfn-batch-computeenvironment-computeresources-securitygroupids)" : [ String, ... ],
  "[SpotIamFleetRole](#cfn-batch-computeenvironment-computeresources-spotiamfleetrole)" : String,
  "[Subnets](#cfn-batch-computeenvironment-computeresources-subnets)" : [ String, ... ],
  "[Tags](#cfn-batch-computeenvironment-computeresources-tags)" : Json,
  "[Type](#cfn-batch-computeenvironment-computeresources-type)" : String
}
```

### YAML<a name="aws-properties-batch-computeenvironment-computeresources-syntax.yaml"></a>

```
  [BidPercentage](#cfn-batch-computeenvironment-computeresources-bidpercentage): Integer
  [DesiredvCpus](#cfn-batch-computeenvironment-computeresources-desiredvcpus): Integer
  [Ec2KeyPair](#cfn-batch-computeenvironment-computeresources-ec2keypair): String
  [ImageId](#cfn-batch-computeenvironment-computeresources-imageid): String
  [InstanceRole](#cfn-batch-computeenvironment-computeresources-instancerole): String
  [InstanceTypes](#cfn-batch-computeenvironment-computeresources-instancetypes): 
    - String
  [LaunchTemplate](#cfn-batch-computeenvironment-computeresources-launchtemplate): 
    [LaunchTemplateSpecification](aws-properties-batch-computeenvironment-launchtemplatespecification.md)
  [MaxvCpus](#cfn-batch-computeenvironment-computeresources-maxvcpus): Integer
  [MinvCpus](#cfn-batch-computeenvironment-computeresources-minvcpus): Integer
  [PlacementGroup](#cfn-batch-computeenvironment-computeresources-placementgroup): String
  [SecurityGroupIds](#cfn-batch-computeenvironment-computeresources-securitygroupids): 
    - String
  [SpotIamFleetRole](#cfn-batch-computeenvironment-computeresources-spotiamfleetrole): String
  [Subnets](#cfn-batch-computeenvironment-computeresources-subnets): 
    - String
  [Tags](#cfn-batch-computeenvironment-computeresources-tags): Json
  [Type](#cfn-batch-computeenvironment-computeresources-type): String
```

## Properties<a name="aws-properties-batch-computeenvironment-computeresources-properties"></a>

`BidPercentage`  <a name="cfn-batch-computeenvironment-computeresources-bidpercentage"></a>
The maximum percentage that a Spot Instance price can be when compared with the On\-Demand price for that instance type before instances are launched\. For example, if your maximum percentage is 20%, then the Spot price must be below 20% of the current On\-Demand price for that EC2 instance\. You always pay the lowest \(market\) price and never more than your maximum percentage\. If you leave this field empty, the default value is 100% of the On\-Demand price\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DesiredvCpus`  <a name="cfn-batch-computeenvironment-computeresources-desiredvcpus"></a>
The desired number of EC2 vCPUS in the compute environment\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2KeyPair`  <a name="cfn-batch-computeenvironment-computeresources-ec2keypair"></a>
The EC2 key pair that is used for instances launched in the compute environment\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageId`  <a name="cfn-batch-computeenvironment-computeresources-imageid"></a>
The Amazon Machine Image \(AMI\) ID used for instances launched in the compute environment\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceRole`  <a name="cfn-batch-computeenvironment-computeresources-instancerole"></a>
The Amazon ECS instance profile applied to Amazon EC2 instances in a compute environment\. You can specify the short name or full Amazon Resource Name \(ARN\) of an instance profile\. For example, ` ecsInstanceRole ` or `arn:aws:iam::<aws_account_id>:instance-profile/ecsInstanceRole `\. For more information, see [Amazon ECS Instance Role](https://docs.aws.amazon.com/batch/latest/userguide/instance_IAM_role.html) in the *AWS Batch User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceTypes`  <a name="cfn-batch-computeenvironment-computeresources-instancetypes"></a>
The instances types that may be launched\. You can specify instance families to launch any instance type within those families \(for example, `c4` or `p3`\), or you can specify specific sizes within a family \(such as `c4.8xlarge`\)\. You can also choose `optimal` to pick instance types \(from the C, M, and R instance families\) on the fly that match the demand of your job queues\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchTemplate`  <a name="cfn-batch-computeenvironment-computeresources-launchtemplate"></a>
The launch template to use for your compute resources\. Any other compute resource parameters that you specify in a [CreateComputeEnvironment](https://docs.aws.amazon.com/batch/latest/APIReference/API_CreateComputeEnvironment.html) API operation override the same parameters in the launch template\. You must specify either the launch template ID or launch template name in the request, but not both\. For more information, see [Launch Template Support](https://docs.aws.amazon.com/batch/latest/userguide/launch-templates.html) in the *AWS Batch User Guide*\.  
*Required*: No  
*Type*: [LaunchTemplateSpecification](aws-properties-batch-computeenvironment-launchtemplatespecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxvCpus`  <a name="cfn-batch-computeenvironment-computeresources-maxvcpus"></a>
The maximum number of EC2 vCPUs that an environment can reach\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinvCpus`  <a name="cfn-batch-computeenvironment-computeresources-minvcpus"></a>
The minimum number of EC2 vCPUs that an environment should maintain \(even if the compute environment is `DISABLED`\)\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlacementGroup`  <a name="cfn-batch-computeenvironment-computeresources-placementgroup"></a>
The Amazon EC2 placement group to associate with your compute resources\. If you intend to submit multi\-node parallel jobs to your compute environment, you should consider creating a cluster placement group and associate it with your compute resources\. This keeps your multi\-node parallel job on a logical grouping of instances within a single Availability Zone with high network flow potential\. For more information, see [Placement Groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroupIds`  <a name="cfn-batch-computeenvironment-computeresources-securitygroupids"></a>
The EC2 security group that is associated with instances launched in the compute environment\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SpotIamFleetRole`  <a name="cfn-batch-computeenvironment-computeresources-spotiamfleetrole"></a>
The Amazon Resource Name \(ARN\) of the Amazon EC2 Spot Fleet IAM role applied to a `SPOT` compute environment\. For more information, see [Amazon EC2 Spot Fleet Role](https://docs.aws.amazon.com/batch/latest/userguide/spot_fleet_IAM_role.html) in the *AWS Batch User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subnets`  <a name="cfn-batch-computeenvironment-computeresources-subnets"></a>
The VPC subnets into which the compute resources are launched\. For more information, see [VPCs and Subnets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html) in the *Amazon VPC User Guide*\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-batch-computeenvironment-computeresources-tags"></a>
Key\-value pair tags to be applied to resources that are launched in the compute environment\. For AWS Batch, these take the form of "String1": "String2", where String1 is the tag key and String2 is the tag value—for example, \{ "Name": "AWS Batch Instance \- C4OnDemand" \}\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-batch-computeenvironment-computeresources-type"></a>
The type of compute environment: EC2 or SPOT\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `EC2 | SPOT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See Also<a name="aws-properties-batch-computeenvironment-computeresources--seealso"></a>
+  [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.