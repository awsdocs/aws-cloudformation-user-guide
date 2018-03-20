# AWS Batch ComputeEnvironment ComputeResources<a name="aws-properties-batch-computeenvironment-computeresources"></a>

The `ComputeResources` property type specifies details of the compute resources managed by the compute environment\. This parameter is required for managed compute environments\. For more information, see [ Compute Environments](http://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.

`ComputeResources` is a property of the [AWS::Batch::ComputeEnvironment](aws-resource-batch-computeenvironment.md) resource\.

## Syntax<a name="aws-properties-batch-computeenvironment-computeresources-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-computeenvironment-computeresources-syntax.json"></a>

```
{
  "[SpotIamFleetRole](#cfn-batch-computeenvironment-computeresources-spotiamfleetrole)" : String,
  "[MaxvCpus](#cfn-batch-computeenvironment-computeresources-maxvcpus)" : Integer,
  "[BidPercentage](#cfn-batch-computeenvironment-computeresources-bidpercentage)" : Integer,
  "[SecurityGroupIds](#cfn-batch-computeenvironment-computeresources-securitygroupids)" : [ String, ... ],
  "[Subnets](#cfn-batch-computeenvironment-computeresources-subnets)" :  [ String, ... ],
  "[Type](#cfn-batch-computeenvironment-computeresources-type)" : String,
  "[MinvCpus](#cfn-batch-computeenvironment-computeresources-minvcpus)" : Integer,
  "[ImageId](#cfn-batch-computeenvironment-computeresources-imageid)" : String,
  "[InstanceRole](#cfn-batch-computeenvironment-computeresources-instancerole)" : String,
  "[InstanceTypes](#cfn-batch-computeenvironment-computeresources-instancetypes)" : [ String, ... ],
  "[Ec2KeyPair](#cfn-batch-computeenvironment-computeresources-ec2keypair)" : String,
  "[Tags](#cfn-batch-computeenvironment-computeresources-tags)" : JSON object,
  "[DesiredvCpus](#cfn-batch-computeenvironment-computeresources-desiredvcpus)" : Integer
}
```

### YAML<a name="aws-properties-batch-computeenvironment-computeresources-syntax.yaml"></a>

```
[SpotIamFleetRole](#cfn-batch-computeenvironment-computeresources-spotiamfleetrole): String
[MaxvCpus](#cfn-batch-computeenvironment-computeresources-maxvcpus): Integer
[BidPercentage](#cfn-batch-computeenvironment-computeresources-bidpercentage): Integer
[SecurityGroupIds](#cfn-batch-computeenvironment-computeresources-securitygroupids): 
  - String
[Subnets](#cfn-batch-computeenvironment-computeresources-subnets): 
  - String
[Type](#cfn-batch-computeenvironment-computeresources-type): String
[MinvCpus](#cfn-batch-computeenvironment-computeresources-minvcpus): Integer
[ImageId](#cfn-batch-computeenvironment-computeresources-imageid): String
[InstanceRole](#cfn-batch-computeenvironment-computeresources-instancerole): String
[InstanceTypes](#cfn-batch-computeenvironment-computeresources-instancetypes): 
  - String
[Ec2KeyPair](#cfn-batch-computeenvironment-computeresources-ec2keypair): String
[Tags](#cfn-batch-computeenvironment-computeresources-tags): JSON object
[DesiredvCpus](#cfn-batch-computeenvironment-computeresources-desiredvcpus): Integer
```

## Properties<a name="aws-properties-batch-computeenvironment-computeresources-properties"></a>

For more information about each property, see [ ComputeResource](http://docs.aws.amazon.com/batch/latest/APIReference/API_ComputeResource.html) in the *AWS Batch API Reference*\.

`SpotIamFleetRole`  <a name="cfn-batch-computeenvironment-computeresources-spotiamfleetrole"></a>
The Amazon Resource Name \(ARN\) of the Amazon EC2 Spot Fleet IAM role applied to a `SPOT` compute environment\.  
 *Required*: No  
*Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`MaxvCpus`  <a name="cfn-batch-computeenvironment-computeresources-maxvcpus"></a>
The maximum number of EC2 vCPUs that an environment can reach\.  
 *Required*: Yes  
*Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SecurityGroupIds`  <a name="cfn-batch-computeenvironment-computeresources-securitygroupids"></a>
The EC2 security group that is associated with instances launched in the compute environment\.  
 *Required*: Yes  
*Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`BidPercentage`  <a name="cfn-batch-computeenvironment-computeresources-bidpercentage"></a>
The minimum percentage that a Spot Instance price must be when compared with the On\-Demand price for that instance type before instances are launched\. For example, if your bid percentage is 20%, then the Spot price must be below 20% of the current On\-Demand price for that EC2 instance\.  
 *Required*: No  
*Type*: Integer  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Type`  <a name="cfn-batch-computeenvironment-computeresources-type"></a>
The type of compute environment: `EC2` or `SPOT`\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Subnets`  <a name="cfn-batch-computeenvironment-computeresources-subnets"></a>
The VPC subnets into which the compute resources are launched\.  
 *Required*: Yes  
*Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`MinvCpus`  <a name="cfn-batch-computeenvironment-computeresources-minvcpus"></a>
The minimum number of EC2 vCPUs that an environment should maintain\.  
 *Required*: Yes  
*Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ImageId`  <a name="cfn-batch-computeenvironment-computeresources-imageid"></a>
The Amazon Machine Image \(AMI\) ID used for instances launched in the compute environment\.  
 *Required*: No  
*Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`InstanceRole`  <a name="cfn-batch-computeenvironment-computeresources-instancerole"></a>
The Amazon ECS instance profile applied to Amazon EC2 instances in a compute environment\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`InstanceTypes`  <a name="cfn-batch-computeenvironment-computeresources-instancetypes"></a>
The instances types that may launched\.  
 *Required*: Yes  
*Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Ec2KeyPair`  <a name="cfn-batch-computeenvironment-computeresources-ec2keypair"></a>
The EC2 key pair that is used for instances launched in the compute environment\.  
 *Required*: No  
*Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-batch-computeenvironment-computeresources-tags"></a>
Key\-value pair tags to be applied to instances that are launched in the compute environment\. For AWS Batch, these take the form of `"String1": "String2"`, where `String1` is the tag key and `String2` is the tag value—for example, `{ "Name": "AWS Batch Instance - C4OnDemand" }`\.  
 *Required*: No  
*Type*: JSON object  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DesiredvCpus`  <a name="cfn-batch-computeenvironment-computeresources-desiredvcpus"></a>
The desired number of EC2 vCPUS in the compute environment\.  
 *Required*: No  
*Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 