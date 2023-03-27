# AWS::Batch::ComputeEnvironment<a name="aws-resource-batch-computeenvironment"></a>

The `AWS::Batch::ComputeEnvironment` resource defines your AWS Batch compute environment\. You can define `MANAGED` or `UNMANAGED` compute environments\. `MANAGED` compute environments can use Amazon EC2 or AWS Fargate resources\. `UNMANAGED` compute environments can only use EC2 resources\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.

In a managed compute environment, AWS Batch manages the capacity and instance types of the compute resources within the environment\. This is based on the compute resource specification that you define or the [launch template](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-launch-templates.html) that you specify when you create the compute environment\. You can choose either to use EC2 On\-Demand Instances and EC2 Spot Instances, or to use Fargate and Fargate Spot capacity in your managed compute environment\. You can optionally set a maximum price so that Spot Instances only launch when the Spot Instance price is below a specified percentage of the On\-Demand price\.

**Note**  
Multi\-node parallel jobs are not supported on Spot Instances\.

In an unmanaged compute environment, you can manage your own EC2 compute resources and have a lot of flexibility with how you configure your compute resources\. For example, you can use custom AMI\. However, you need to verify that your AMI meets the Amazon ECS container instance AMI specification\. For more information, see [container instance AMIs](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/container_instance_AMIs.html) in the *Amazon Elastic Container Service Developer Guide*\. After you have created your unmanaged compute environment, you can use the [DescribeComputeEnvironments](https://docs.aws.amazon.com/batch/latest/APIReference/API_DescribeComputeEnvironments.html) operation to find the Amazon ECS cluster that is associated with it\. Then, manually launch your container instances into that Amazon ECS cluster\. For more information, see [Launching an Amazon ECS container instance](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/launch_container_instance.html) in the *Amazon Elastic Container Service Developer Guide*\.

**Note**  
To create a compute environment that uses EKS resources, the caller must have permissions to call `eks:DescribeCluster`\.

**Note**  
AWS Batch doesn't upgrade the AMIs in a compute environment after it's created except under specific conditions\. For example, it doesn't automatically update the AMIs when a newer version of the Amazon ECS optimized AMI is available\. Therefore, you're responsible for the management of the guest operating system \(including updates and security patches\) and any additional application software or utilities that you install on the compute resources\. There are two ways to use a new AMI for your AWS Batch jobs\. The original method is to complete these steps:  
Create a new compute environment with the new AMI\.
Add the compute environment to an existing job queue\.
Remove the earlier compute environment from your job queue\.
Delete the earlier compute environment\.
In April 2022, AWS Batch added enhanced support for updating compute environments\. For more information, see [Updating compute environments](https://docs.aws.amazon.com/batch/latest/userguide/updating-compute-environments.html) in the * AWS Batch User Guide*\. To use the enhanced updating of compute environments to update AMIs, follow these rules:  
Either do not set the [ServiceRole](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html#cfn-batch-computeenvironment-servicerole) property or set it to the **AWSServiceRoleForBatch** service\-linked role\.
Set the [AllocationStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-allocationstrategy) property to `BEST_FIT_PROGRESSIVE` or `SPOT_CAPACITY_OPTIMIZED`\.
Set the [ReplaceComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html#cfn-batch-computeenvironment-replacecomputeenvironment) property to `false`\.
Set the [UpdateToLatestImageVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-updatetolatestimageversion) property to `true`\.
Either do not specify an image ID in [ImageId](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-imageid) or [ImageIdOverride](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-ec2configurationobject.html#cfn-batch-computeenvironment-ec2configurationobject-imageidoverride) properties, or in the launch template identified by the [Launch Template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-launchtemplate) property\. In that case AWS Batch will select the latest Amazon ECS optimized AMI supported by AWS Batch at the time the infrastructure update is initiated\. Alternatively you can specify the AMI ID in the `ImageId` or `ImageIdOverride` properties, or the launch template identified by the `LaunchTemplate` properties\. Changing any of these properties will trigger an infrastructure update\.
If these rules are followed, any update that triggers an infrastructure update will cause the AMI ID to be re\-selected\. If the [Version](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-launchtemplatespecification.html#cfn-batch-computeenvironment-launchtemplatespecification-version) property of the [LaunchTemplateSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-launchtemplatespecification.html) is set to `$Latest` or `$Default`, the latest or default version of the launch template will be evaluated up at the time of the infrastructure update, even if the `LaunchTemplateSpecification` was not updated\.

## Syntax<a name="aws-resource-batch-computeenvironment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-batch-computeenvironment-syntax.json"></a>

```
{
  "Type" : "AWS::Batch::ComputeEnvironment",
  "Properties" : {
      "[ComputeEnvironmentName](#cfn-batch-computeenvironment-computeenvironmentname)" : String,
      "[ComputeResources](#cfn-batch-computeenvironment-computeresources)" : ComputeResources,
      "[EksConfiguration](#cfn-batch-computeenvironment-eksconfiguration)" : EksConfiguration,
      "[ReplaceComputeEnvironment](#cfn-batch-computeenvironment-replacecomputeenvironment)" : Boolean,
      "[ServiceRole](#cfn-batch-computeenvironment-servicerole)" : String,
      "[State](#cfn-batch-computeenvironment-state)" : String,
      "[Tags](#cfn-batch-computeenvironment-tags)" : {Key : Value, ...},
      "[Type](#cfn-batch-computeenvironment-type)" : String,
      "[UnmanagedvCpus](#cfn-batch-computeenvironment-unmanagedvcpus)" : Integer,
      "[UpdatePolicy](#cfn-batch-computeenvironment-updatepolicy)" : UpdatePolicy
    }
}
```

### YAML<a name="aws-resource-batch-computeenvironment-syntax.yaml"></a>

```
Type: AWS::Batch::ComputeEnvironment
Properties: 
  [ComputeEnvironmentName](#cfn-batch-computeenvironment-computeenvironmentname): String
  [ComputeResources](#cfn-batch-computeenvironment-computeresources): 
    ComputeResources
  [EksConfiguration](#cfn-batch-computeenvironment-eksconfiguration): 
    EksConfiguration
  [ReplaceComputeEnvironment](#cfn-batch-computeenvironment-replacecomputeenvironment): Boolean
  [ServiceRole](#cfn-batch-computeenvironment-servicerole): String
  [State](#cfn-batch-computeenvironment-state): String
  [Tags](#cfn-batch-computeenvironment-tags): 
    Key : Value
  [Type](#cfn-batch-computeenvironment-type): String
  [UnmanagedvCpus](#cfn-batch-computeenvironment-unmanagedvcpus): Integer
  [UpdatePolicy](#cfn-batch-computeenvironment-updatepolicy): 
    UpdatePolicy
```

## Properties<a name="aws-resource-batch-computeenvironment-properties"></a>

`ComputeEnvironmentName`  <a name="cfn-batch-computeenvironment-computeenvironmentname"></a>
The name for your compute environment\. It can be up to 128 characters long\. It can contain uppercase and lowercase letters, numbers, hyphens \(\-\), and underscores \(\_\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ComputeResources`  <a name="cfn-batch-computeenvironment-computeresources"></a>
The ComputeResources property type specifies details of the compute resources managed by the compute environment\. This parameter is required for managed compute environments\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.  
*Required*: No  
*Type*: [ComputeResources](aws-properties-batch-computeenvironment-computeresources.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EksConfiguration`  <a name="cfn-batch-computeenvironment-eksconfiguration"></a>
The details for the Amazon EKS cluster that supports the compute environment\.  
*Required*: No  
*Type*: [EksConfiguration](aws-properties-batch-computeenvironment-eksconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplaceComputeEnvironment`  <a name="cfn-batch-computeenvironment-replacecomputeenvironment"></a>
Specifies whether the compute environment is replaced if an update is made that requires replacing the instances in the compute environment\. The default value is `true`\. To enable more properties to be updated, set this property to `false`\. When changing the value of this property to `false`, do not change any other properties at the same time\. If other properties are changed at the same time, and the change needs to be rolled back but it can't, it's possible for the stack to go into the `UPDATE_ROLLBACK_FAILED` state\. You can't update a stack that is in the `UPDATE_ROLLBACK_FAILED` state\. However, if you can continue to roll it back, you can return the stack to its original settings and then try to update it again\. For more information, see [Continue rolling back an update](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-continueupdaterollback.html) in the *AWS CloudFormation User Guide*\.  
The properties that can't be changed without replacing the compute environment are in the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html) property type: [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-allocationstrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-allocationstrategy), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-bidpercentage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-bidpercentage), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-ec2configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-ec2configuration), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-ec2keypair](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-ec2keypair), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-ec2keypair](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-ec2keypair), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-imageid](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-imageid), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-instancerole](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-instancerole), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-instancetypes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-instancetypes), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-launchtemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-launchtemplate), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-maxvcpus](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-maxvcpus), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-minvcpus](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-minvcpus), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-placementgroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-placementgroup), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-securitygroupids](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-securitygroupids), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-subnets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-subnets), [Tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-tags), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-type), and [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-updatetolatestimageversion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html#cfn-batch-computeenvironment-computeresources-updatetolatestimageversion)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceRole`  <a name="cfn-batch-computeenvironment-servicerole"></a>
The full Amazon Resource Name \(ARN\) of the IAM role that allows AWS Batch to make calls to other AWS services on your behalf\. For more information, see [AWS Batch service IAM role](https://docs.aws.amazon.com/batch/latest/userguide/service_IAM_role.html) in the * AWS Batch User Guide*\.  
If your account already created the AWS Batch service\-linked role, that role is used by default for your compute environment unless you specify a different role here\. If the AWS Batch service\-linked role doesn't exist in your account, and no role is specified here, the service attempts to create the AWS Batch service\-linked role in your account\.
If your specified role has a path other than `/`, then you must specify either the full role ARN \(recommended\) or prefix the role name with the path\. For example, if a role with the name `bar` has a path of `/foo/`, specify `/foo/bar` as the role name\. For more information, see [Friendly names and paths](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_identifiers.html#identifiers-friendly-names) in the *IAM User Guide*\.  
Depending on how you created your AWS Batch service role, its ARN might contain the `service-role` path prefix\. When you only specify the name of the service role, AWS Batch assumes that your ARN doesn't use the `service-role` path prefix\. Because of this, we recommend that you specify the full ARN of your service role when you create compute environments\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-batch-computeenvironment-state"></a>
The state of the compute environment\. If the state is `ENABLED`, then the compute environment accepts jobs from a queue and can scale out automatically based on queues\.  
If the state is `ENABLED`, then the AWS Batch scheduler can attempt to place jobs from an associated job queue on the compute resources within the environment\. If the compute environment is managed, then it can scale its instances out or in automatically, based on the job queue demand\.  
If the state is `DISABLED`, then the AWS Batch scheduler doesn't attempt to place jobs within the environment\. Jobs in a `STARTING` or `RUNNING` state continue to progress normally\. Managed compute environments in the `DISABLED` state don't scale out\.   
Compute environments in a `DISABLED` state may continue to incur billing charges\. To prevent additional charges, turn off and then delete the compute environment\. For more information, see [State](https://docs.aws.amazon.com/batch/latest/userguide/compute_environment_parameters.html#compute_environment_state) in the * AWS Batch User Guide*\.
When an instance is idle, the instance scales down to the `minvCpus` value\. However, the instance size doesn't change\. For example, consider a `c5.8xlarge` instance with a `minvCpus` value of `4` and a `desiredvCpus` value of `36`\. This instance doesn't scale down to a `c5.large` instance\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-batch-computeenvironment-tags"></a>
The tags applied to the compute environment\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-batch-computeenvironment-type"></a>
The type of the compute environment: `MANAGED` or `UNMANAGED`\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the * AWS Batch User Guide*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MANAGED | UNMANAGED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UnmanagedvCpus`  <a name="cfn-batch-computeenvironment-unmanagedvcpus"></a>
The maximum number of vCPUs for an unmanaged compute environment\. This parameter is only used for fair share scheduling to reserve vCPU capacity for new share identifiers\. If this parameter isn't provided for a fair share job queue, no vCPU capacity is reserved\.  
This parameter is only supported when the `type` parameter is set to `UNMANAGED`\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdatePolicy`  <a name="cfn-batch-computeenvironment-updatepolicy"></a>
Specifies the infrastructure update policy for the compute environment\. For more information about infrastructure updates, see [Updating compute environments](https://docs.aws.amazon.com/batch/latest/userguide/updating-compute-environments.html) in the * AWS Batch User Guide*\.  
*Required*: No  
*Type*: [UpdatePolicy](aws-properties-batch-computeenvironment-updatepolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-batch-computeenvironment-return-values"></a>

### Ref<a name="aws-resource-batch-computeenvironment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the compute environment ARN, such as `arn:aws:batch:us-east-1:555555555555:compute-environment/M4OnDemand`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-batch-computeenvironment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-batch-computeenvironment-return-values-fn--getatt-fn--getatt"></a>

`ComputeEnvironmentArn`  <a name="ComputeEnvironmentArn-fn::getatt"></a>
Returns the compute environment ARN, such as `arn:aws:batch:us-east-1:111122223333:compute-environment/ComputeEnvironmentName`\.

## Examples<a name="aws-resource-batch-computeenvironment--examples"></a>



### Managed Compute Environment<a name="aws-resource-batch-computeenvironment--examples--Managed_Compute_Environment"></a>

The following example creates a managed compute environment called `C4OnDemand` that uses C4 On\-Demand instances and a custom AMI\.

#### JSON<a name="aws-resource-batch-computeenvironment--examples--Managed_Compute_Environment--json"></a>

```
{
  "ComputeEnvironment": {
    "Type": "AWS::Batch::ComputeEnvironment",
    "Properties": {
      "Type": "MANAGED",
      "ServiceRole": "arn:aws:iam::111122223333:role/aws-service-role/batch.amazonaws.com/AWSServiceRoleForBatch",
      "ComputeEnvironmentName": "C4OnDemand",
      "ComputeResources": {
        "MaxvCpus": 128,
        "SecurityGroupIds": [
          "sg-abcd1234"
        ],
        "Type": "EC2",
        "Subnets": [
          "subnet-aaaaaaaa",
          "subnet-bbbbbbbb",
          "subnet-cccccccc"
        ],
        "MinvCpus": 0,
        "ImageId": "ami-a1b2c3d4",
        "InstanceRole": "ecsInstanceRole",
        "InstanceTypes": [
          "c4.large",
          "c4.xlarge",
          "c4.2xlarge",
          "c4.4xlarge",
          "c4.8xlarge"
        ],
        "Ec2KeyPair": "id_rsa",
        "Tags": {
          "Name": "Batch Instance - C4OnDemand"
        },
        "DesiredvCpus": 48
      },
      "State": "ENABLED"
    }
  }
}
```

#### YAML<a name="aws-resource-batch-computeenvironment--examples--Managed_Compute_Environment--yaml"></a>

```
ComputeEnvironment:
  Type: AWS::Batch::ComputeEnvironment
  Properties:
    Type: MANAGED
    ServiceRole: arn:aws:iam::111122223333:role/aws-service-role/batch.amazonaws.com/AWSServiceRoleForBatch
    ComputeEnvironmentName: C4OnDemand
    ComputeResources:
      MaxvCpus: 128
      SecurityGroupIds:
        - sg-abcd1234
      Type: EC2
      Subnets:
        - subnet-aaaaaaaa
        - subnet-bbbbbbbb
        - subnet-cccccccc
      MinvCpus: 0
      ImageId: ami-a1b2c3d4
      InstanceRole: ecsInstanceRole
      InstanceTypes:
        - c4.large
        - c4.xlarge
        - c4.2xlarge
        - c4.4xlarge
        - c4.8xlarge
      Ec2KeyPair: id_rsa
      Tags: {"Name" : "Batch Instance - C4OnDemand"}
      DesiredvCpus: 48
    State: ENABLED
```

## See also<a name="aws-resource-batch-computeenvironment--seealso"></a>
+  [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.