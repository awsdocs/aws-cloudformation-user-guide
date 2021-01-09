# AWS::Batch::ComputeEnvironment ComputeResources<a name="aws-properties-batch-computeenvironment-computeresources"></a>

Details about the compute resources managed by the compute environment\. This parameter is required for managed compute environments\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.

## Syntax<a name="aws-properties-batch-computeenvironment-computeresources-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-computeenvironment-computeresources-syntax.json"></a>

```
{
  "[AllocationStrategy](#cfn-batch-computeenvironment-computeresources-allocationstrategy)" : String,
  "[BidPercentage](#cfn-batch-computeenvironment-computeresources-bidpercentage)" : Integer,
  "[DesiredvCpus](#cfn-batch-computeenvironment-computeresources-desiredvcpus)" : Integer,
  "[Ec2Configuration](#cfn-batch-computeenvironment-computeresources-ec2configuration)" : [ Ec2ConfigurationObject, ... ],
  "[Ec2KeyPair](#cfn-batch-computeenvironment-computeresources-ec2keypair)" : String,
  "[ImageId](#cfn-batch-computeenvironment-computeresources-imageid)" : String,
  "[InstanceRole](#cfn-batch-computeenvironment-computeresources-instancerole)" : String,
  "[InstanceTypes](#cfn-batch-computeenvironment-computeresources-instancetypes)" : [ String, ... ],
  "[LaunchTemplate](#cfn-batch-computeenvironment-computeresources-launchtemplate)" : LaunchTemplateSpecification,
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
  [AllocationStrategy](#cfn-batch-computeenvironment-computeresources-allocationstrategy): String
  [BidPercentage](#cfn-batch-computeenvironment-computeresources-bidpercentage): Integer
  [DesiredvCpus](#cfn-batch-computeenvironment-computeresources-desiredvcpus): Integer
  [Ec2Configuration](#cfn-batch-computeenvironment-computeresources-ec2configuration): 
    - Ec2ConfigurationObject
  [Ec2KeyPair](#cfn-batch-computeenvironment-computeresources-ec2keypair): String
  [ImageId](#cfn-batch-computeenvironment-computeresources-imageid): String
  [InstanceRole](#cfn-batch-computeenvironment-computeresources-instancerole): String
  [InstanceTypes](#cfn-batch-computeenvironment-computeresources-instancetypes): 
    - String
  [LaunchTemplate](#cfn-batch-computeenvironment-computeresources-launchtemplate): 
    LaunchTemplateSpecification
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

`AllocationStrategy`  <a name="cfn-batch-computeenvironment-computeresources-allocationstrategy"></a>
The allocation strategy to use for the compute resource if not enough instances of the best fitting instance type can be allocated\. This might be because of availability of the instance type in the Region or [Amazon EC2 service limits](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-resource-limits.html)\. For more information, see [Allocation Strategies](https://docs.aws.amazon.com/batch/latest/userguide/allocation-strategies.html) in the *AWS Batch User Guide*\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.  
BEST\_FIT \(default\)  
AWS Batch selects an instance type that best fits the needs of the jobs with a preference for the lowest\-cost instance type\. If additional instances of the selected instance type aren't available, AWS Batch will wait for the additional instances to be available\. If there are not enough instances available, or if the user is hitting [Amazon EC2 service limits](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-resource-limits.html) then additional jobs aren't run until currently running jobs have completed\. This allocation strategy keeps costs lower but can limit scaling\. If you are using Spot Fleets with `BEST_FIT` then the Spot Fleet IAM Role must be specified\.  
BEST\_FIT\_PROGRESSIVE  
AWS Batch will select additional instance types that are large enough to meet the requirements of the jobs in the queue, with a preference for instance types with a lower cost per unit vCPU\. If additional instances of the previously selected instance types aren't available, AWS Batch will select new instance types\.  
SPOT\_CAPACITY\_OPTIMIZED  
AWS Batch will select one or more instance types that are large enough to meet the requirements of the jobs in the queue, with a preference for instance types that are less likely to be interrupted\. This allocation strategy is only available for Spot Instance compute resources\.
With both `BEST_FIT_PROGRESSIVE` and `SPOT_CAPACITY_OPTIMIZED` strategies, AWS Batch might need to go above `maxvCpus` to meet your capacity requirements\. In this event, AWS Batch never exceeds `maxvCpus` by more than a single instance\.  
*Required*: No  
*Type*: String  
*Allowed values*: `BEST_FIT | BEST_FIT_PROGRESSIVE | SPOT_CAPACITY_OPTIMIZED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BidPercentage`  <a name="cfn-batch-computeenvironment-computeresources-bidpercentage"></a>
The maximum percentage that a Spot Instance price can be when compared with the On\-Demand price for that instance type before instances are launched\. For example, if your maximum percentage is 20%, then the Spot price must be less than 20% of the current On\-Demand price for that Amazon EC2 instance\. You always pay the lowest \(market\) price and never more than your maximum percentage\. If you leave this field empty, the default value is 100% of the On\-Demand price\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DesiredvCpus`  <a name="cfn-batch-computeenvironment-computeresources-desiredvcpus"></a>
The desired number of Amazon EC2 vCPUS in the compute environment\. AWS Batch modifies this value between the minimum and maximum values, based on job queue demand\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2Configuration`  <a name="cfn-batch-computeenvironment-computeresources-ec2configuration"></a>
Provides information used to select Amazon Machine Images \(AMIs\) for EC2 instances in the compute environment\. If `Ec2Configuration` isn't specified, the default is `ECS_AL1`\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
*Required*: No  
*Type*: List of [Ec2ConfigurationObject](aws-properties-batch-computeenvironment-ec2configurationobject.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ec2KeyPair`  <a name="cfn-batch-computeenvironment-computeresources-ec2keypair"></a>
The Amazon EC2 key pair that's used for instances launched in the compute environment\. You can use this key pair to log in to your instances with SSH\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageId`  <a name="cfn-batch-computeenvironment-computeresources-imageid"></a>
The Amazon Machine Image \(AMI\) ID used for instances launched in the compute environment\. This parameter is overridden by the `imageIdOverride` member of the `Ec2Configuration` structure\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
The AMI that you choose for a compute environment must match the architecture of the instance types that you intend to use for that compute environment\. For example, if your compute environment uses A1 instance types, the compute resource AMI that you choose must support ARM instances\. Amazon ECS vends both x86 and ARM versions of the Amazon ECS\-optimized Amazon Linux 2 AMI\. For more information, see [Amazon ECS\-optimized Amazon Linux 2 AMI](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-optimized_AMI.html#ecs-optimized-ami-linux-variants.html) in the *Amazon Elastic Container Service Developer Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceRole`  <a name="cfn-batch-computeenvironment-computeresources-instancerole"></a>
The Amazon ECS instance profile applied to Amazon EC2 instances in a compute environment\. You can specify the short name or full Amazon Resource Name \(ARN\) of an instance profile\. For example, ` ecsInstanceRole ` or `arn:aws:iam::<aws_account_id>:instance-profile/ecsInstanceRole `\. For more information, see [Amazon ECS Instance Role](https://docs.aws.amazon.com/batch/latest/userguide/instance_IAM_role.html) in the *AWS Batch User Guide*\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceTypes`  <a name="cfn-batch-computeenvironment-computeresources-instancetypes"></a>
The instances types that can be launched\. You can specify instance families to launch any instance type within those families \(for example, `c5` or `p3`\), or you can specify specific sizes within a family \(such as `c5.8xlarge`\)\. You can also choose `optimal` to select instance types \(from the C4, M4, and R4 instance families\) on the fly that match the demand of your job queues\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
When you create a compute environment, the instance types that you select for the compute environment must share the same architecture\. For example, you can't mix x86 and ARM instances in the same compute environment\.
Currently, `optimal` uses instance types from the C4, M4, and R4 instance families\. In Regions that don't have instance types from those instance families, instance types from the C5, M5\. and R5 instance families are used\.
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchTemplate`  <a name="cfn-batch-computeenvironment-computeresources-launchtemplate"></a>
The launch template to use for your compute resources\. Any other compute resource parameters that you specify in a [CreateComputeEnvironment](https://docs.aws.amazon.com/batch/latest/APIReference/API_CreateComputeEnvironment.html) API operation override the same parameters in the launch template\. You must specify either the launch template ID or launch template name in the request, but not both\. For more information, see [Launch Template Support](https://docs.aws.amazon.com/batch/latest/userguide/launch-templates.html) in the *AWS Batch User Guide*\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
*Required*: No  
*Type*: [LaunchTemplateSpecification](aws-properties-batch-computeenvironment-launchtemplatespecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxvCpus`  <a name="cfn-batch-computeenvironment-computeresources-maxvcpus"></a>
The maximum number of Amazon EC2 vCPUs that an environment can reach\.  
With both `BEST_FIT_PROGRESSIVE` and `SPOT_CAPACITY_OPTIMIZED` allocation strategies, AWS Batch might need to go above `maxvCpus` to meet your capacity requirements\. In this event, AWS Batch will never go above `maxvCpus` by more than a single instance \(e\.g\., no more than a single instance from among those specified in your compute environment\)\.
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinvCpus`  <a name="cfn-batch-computeenvironment-computeresources-minvcpus"></a>
The minimum number of Amazon EC2 vCPUs that an environment should maintain \(even if the compute environment is `DISABLED`\)\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlacementGroup`  <a name="cfn-batch-computeenvironment-computeresources-placementgroup"></a>
The Amazon EC2 placement group to associate with your compute resources\. If you intend to submit multi\-node parallel jobs to your compute environment, you should consider creating a cluster placement group and associate it with your compute resources\. This keeps your multi\-node parallel job on a logical grouping of instances within a single Availability Zone with high network flow potential\. For more information, see [Placement Groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroupIds`  <a name="cfn-batch-computeenvironment-computeresources-securitygroupids"></a>
The Amazon EC2 security groups associated with instances launched in the compute environment\. One or more security groups must be specified, either in `securityGroupIds` or using a launch template referenced in `launchTemplate`\. This parameter is required for jobs running on Fargate resources and must contain at least one security group\. \(Fargate does not support launch templates\.\) If security groups are specified using both `securityGroupIds` and `launchTemplate`, the values in `securityGroupIds` will be used\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotIamFleetRole`  <a name="cfn-batch-computeenvironment-computeresources-spotiamfleetrole"></a>
The Amazon Resource Name \(ARN\) of the Amazon EC2 Spot Fleet IAM role applied to a `SPOT` compute environment\. This role is required if the allocation strategy set to `BEST_FIT` or if the allocation strategy isn't specified\. For more information, see [Amazon EC2 Spot Fleet Role](https://docs.aws.amazon.com/batch/latest/userguide/spot_fleet_IAM_role.html) in the *AWS Batch User Guide*\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
To tag your Spot Instances on creation, the Spot Fleet IAM role specified here must use the newer **AmazonEC2SpotFleetTaggingRole** managed policy\. The previously recommended **AmazonEC2SpotFleetRole** managed policy doesn't have the required permissions to tag Spot Instances\. For more information, see [Spot Instances not tagged on creation](https://docs.aws.amazon.com/batch/latest/userguide/troubleshooting.html#spot-instance-no-tag) in the *AWS Batch User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subnets`  <a name="cfn-batch-computeenvironment-computeresources-subnets"></a>
The VPC subnets into which the compute resources are launched\. These subnets must be within the same VPC\. This parameter is required for jobs running on Fargate resources, where it can contain up to 16 subnets\. For more information, see [VPCs and Subnets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html) in the *Amazon VPC User Guide*\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-batch-computeenvironment-computeresources-tags"></a>
Key\-value pair tags to be applied to EC2 resources that are launched in the compute environment\. For AWS Batch, these take the form of "String1": "String2", where String1 is the tag key and String2 is the tag value−for example, \{ "Name": "AWS Batch Instance \- C4OnDemand" \}\. This is helpful for recognizing your AWS Batch instances in the Amazon EC2 console\. These tags can't be updated or removed after the compute environment has been created; any changes require creating a new compute environment and removing the old compute environment\. These tags are not seen when using the AWS Batch `ListTagsForResource` API operation\.  
This parameter isn't applicable to jobs running on Fargate resources, and shouldn't be specified\.
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-batch-computeenvironment-computeresources-type"></a>
The type of compute environment: `EC2`, `SPOT`, `FARGATE`, or `FARGATE_SPOT`\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.  
 If you choose `SPOT`, you must also specify an Amazon EC2 Spot Fleet role with the `spotIamFleetRole` parameter\. For more information, see [Amazon EC2 Spot Fleet role](https://docs.aws.amazon.com/batch/latest/userguide/spot_fleet_IAM_role.html) in the *AWS Batch User Guide*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `EC2 | FARGATE | FARGATE_SPOT | SPOT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-batch-computeenvironment-computeresources--seealso"></a>
+  [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.