# AWS::Batch::ComputeEnvironment<a name="aws-resource-batch-computeenvironment"></a>

The `AWS::Batch::ComputeEnvironment` resource defines your AWS Batch compute environment\. You can define `MANAGED` or `UNMANAGED` compute environments\. `MANAGED` compute environments can use Amazon EC2 or AWS Fargate resources\. `UNMANAGED` compute environments can only use EC2 resources\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.

In a managed compute environment, AWS Batch manages the capacity and instance types of the compute resources within the environment\. This is based on the compute resource specification that you define or the [launch template](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-launch-templates.html) that you specify when you create the compute environment\. You can choose either to use EC2 On\-Demand Instances and EC2 Spot Instances, or to use Fargate and Fargate Spot capacity in your managed compute environment\. You can optionally set a maximum price so that Spot Instances only launch when the Spot Instance price is below a specified percentage of the On\-Demand price\.

**Note**  
Multi\-node parallel jobs are not supported on Spot Instances\.

In an unmanaged compute environment, you can manage your own EC2 compute resources and have a lot of flexibility with how you configure your compute resources\. For example, you can use custom AMI\. However, you need to verify that your AMI meets the Amazon ECS container instance AMI specification\. For more information, see [container instance AMIs](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/container_instance_AMIs.html) in the *Amazon Elastic Container Service Developer Guide*\. After you have created your unmanaged compute environment, you can use the [DescribeComputeEnvironments](https://docs.aws.amazon.com/batch/latest/APIReference/API_DescribeComputeEnvironments.html) operation to find the Amazon ECS cluster that is associated with it\. Then, manually launch your container instances into that Amazon ECS cluster\. For more information, see [Launching an Amazon ECS container instance](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/launch_container_instance.html) in the *Amazon Elastic Container Service Developer Guide*\.

**Note**  
AWS Batch doesn't upgrade the AMIs in a compute environment after it's created\. For example, it doesn't update the AMIs when a newer version of the Amazon ECS optimized AMI is available\. Therefore, you're responsible for the management of the guest operating system \(including updates and security patches\) and any additional application software or utilities that you install on the compute resources\. To use a new AMI for your AWS Batch jobs, complete these steps:  
Create a new compute environment with the new AMI\.
Add the compute environment to an existing job queue\.
Remove the earlier compute environment from your job queue\.
Delete the earlier compute environment\.

## Syntax<a name="aws-resource-batch-computeenvironment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-batch-computeenvironment-syntax.json"></a>

```
{
  "Type" : "AWS::Batch::ComputeEnvironment",
  "Properties" : {
      "[ComputeEnvironmentName](#cfn-batch-computeenvironment-computeenvironmentname)" : String,
      "[ComputeResources](#cfn-batch-computeenvironment-computeresources)" : ComputeResources,
      "[ServiceRole](#cfn-batch-computeenvironment-servicerole)" : String,
      "[State](#cfn-batch-computeenvironment-state)" : String,
      "[Tags](#cfn-batch-computeenvironment-tags)" : Json,
      "[Type](#cfn-batch-computeenvironment-type)" : String
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
  [ServiceRole](#cfn-batch-computeenvironment-servicerole): String
  [State](#cfn-batch-computeenvironment-state): String
  [Tags](#cfn-batch-computeenvironment-tags): Json
  [Type](#cfn-batch-computeenvironment-type): String
```

## Properties<a name="aws-resource-batch-computeenvironment-properties"></a>

`ComputeEnvironmentName`  <a name="cfn-batch-computeenvironment-computeenvironmentname"></a>
The name for your compute environment\. Up to 128 letters \(uppercase and lowercase\), numbers, hyphens, and underscores are allowed\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ComputeResources`  <a name="cfn-batch-computeenvironment-computeresources"></a>
The ComputeResources property type specifies details of the compute resources managed by the compute environment\. This parameter is required for managed compute environments\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.  
*Required*: No  
*Type*: [ComputeResources](aws-properties-batch-computeenvironment-computeresources.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceRole`  <a name="cfn-batch-computeenvironment-servicerole"></a>
The full Amazon Resource Name \(ARN\) of the IAM role that allows AWS Batch to make calls to other AWS services on your behalf\. For more information, see [AWS Batch service IAM role](https://docs.aws.amazon.com/batch/latest/userguide/service_IAM_role.html) in the *AWS Batch User Guide*\.  
If your specified role has a path other than `/`, then you must either specify the full role ARN \(this is recommended\) or prefix the role name with the path\.  
Depending on how you created your AWS Batch service role, its ARN might contain the `service-role` path prefix\. When you only specify the name of the service role, AWS Batch assumes that your ARN doesn't use the `service-role` path prefix\. Because of this, we recommend that you specify the full ARN of your service role when you create compute environments\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-batch-computeenvironment-state"></a>
The state of the compute environment\. If the state is `ENABLED`, then the compute environment accepts jobs from a queue and can scale out automatically based on queues\.  
If the state is `ENABLED`, then the AWS Batch scheduler can attempt to place jobs from an associated job queue on the compute resources within the environment\. If the compute environment is managed, then it can scale its instances out or in automatically, based on the job queue demand\.  
If the state is `DISABLED`, then the AWS Batch scheduler doesn't attempt to place jobs within the environment\. Jobs in a `STARTING` or `RUNNING` state continue to progress normally\. Managed compute environments in the `DISABLED` state don't scale out\. However, they scale in to `minvCpus` value after instances become idle\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-batch-computeenvironment-tags"></a>
The tags applied to the compute environment\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-batch-computeenvironment-type"></a>
The type of the compute environment: `MANAGED` or `UNMANAGED`\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MANAGED | UNMANAGED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-batch-computeenvironment-return-values"></a>

### Ref<a name="aws-resource-batch-computeenvironment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the compute environment ARN, such as `arn:aws:batch:us-east-1:555555555555:compute-environment/M4OnDemand`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

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
      "ServiceRole": "arn:aws:iam::111122223333:role/service-role/AWSBatchServiceRole",
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
    ServiceRole: arn:aws:iam::111122223333:role/service-role/AWSBatchServiceRole
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