# AWS::Batch::ComputeEnvironment<a name="aws-resource-batch-computeenvironment"></a>

The `AWS::Batch::ComputeEnvironment` resource defines your AWS Batch compute environment\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.

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
The full Amazon Resource Name \(ARN\) of the IAM role that allows AWS Batch to make calls to other AWS services on your behalf\.  
If your specified role has a path other than `/`, then you must either specify the full role ARN \(this is recommended\) or prefix the role name with the path\.  
Depending on how you created your AWS Batch service role, its ARN may contain the `service-role` path prefix\. When you only specify the name of the service role, AWS Batch assumes that your ARN does not use the `service-role` path prefix\. Because of this, we recommend that you specify the full ARN of your service role when you create compute environments\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-batch-computeenvironment-state"></a>
The state of the compute environment\. If the state is `ENABLED`, then the compute environment accepts jobs from a queue and can scale out automatically based on queues\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-batch-computeenvironment-type"></a>
The type of the compute environment\. For more information, see [Compute Environments](https://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\.  
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