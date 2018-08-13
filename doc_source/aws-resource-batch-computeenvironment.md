# AWS::Batch::ComputeEnvironment<a name="aws-resource-batch-computeenvironment"></a>

The `AWS::Batch::ComputeEnvironment` resource to define your AWS Batch compute environment\. For more information, see [Compute Environments](http://docs.aws.amazon.com/batch/latest/userguide/compute_environments.html) in the *AWS Batch User Guide*\. 

**Topics**
+ [Syntax](#aws-resource-batch-computeenvironment-syntax)
+ [Properties](#aws-resource-batch-computeenvironment-properties)
+ [Return Values](#aws-resource-batch-computeenvironment-returnvalues)
+ [Examples](#aws-resource-batch-computeenvironment-examples)

## Syntax<a name="aws-resource-batch-computeenvironment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-batch-computeenvironment-syntax.json"></a>

```
{
  "Type" : "AWS::Batch::ComputeEnvironment",
  "Properties" : {
    "[Type](#cfn-batch-computeenvironment-type)" : String,
    "[ServiceRole](#cfn-batch-computeenvironment-servicerole)" : String,
    "[ComputeEnvironmentName](#cfn-batch-computeenvironment-computeenvironmentname)" : String,
    "[ComputeResources](#cfn-batch-computeenvironment-computeresources)" : [*ComputeResources*](aws-properties-batch-computeenvironment-computeresources.md),
    "[State](#cfn-batch-computeenvironment-state)" : String
  }
}
```

### YAML<a name="aws-resource-batch-computeenvironment-syntax.yaml"></a>

```
Type: "AWS::Batch::ComputeEnvironment"
Properties:
  [Type](#cfn-batch-computeenvironment-type): String
  [ServiceRole](#cfn-batch-computeenvironment-servicerole): String
  [ComputeEnvironmentName](#cfn-batch-computeenvironment-computeenvironmentname): String
  [ComputeResources](#cfn-batch-computeenvironment-computeresources): 
    [*ComputeResources*](aws-properties-batch-computeenvironment-computeresources.md)
  [State](#cfn-batch-computeenvironment-state): String
```

## Properties<a name="aws-resource-batch-computeenvironment-properties"></a>

`Type`  <a name="cfn-batch-computeenvironment-type"></a>
The type of the compute environment\.  
 *Required*: yes  
*Type*: String  
 *Update requires*: Replacement 

`ServiceRole`  <a name="cfn-batch-computeenvironment-servicerole"></a>
The service role associated with the compute environment that allows AWS Batch to make calls to AWS API operations on your behalf\.  
 *Required*: yes  
*Type*: String  
 *Update requires*: No Interruption 

`ComputeEnvironmentName`  <a name="cfn-batch-computeenvironment-computeenvironmentname"></a>
The name of the compute environment\.  
 *Required*: no  
*Type*: String  
 *Update requires*: Replacement 

`ComputeResources`  <a name="cfn-batch-computeenvironment-computeresources"></a>
The compute resources defined for the compute environment\.  
 *Required*: yes  
 *Type*: [AWS Batch ComputeEnvironment ComputeResources](aws-properties-batch-computeenvironment-computeresources.md)  
 *Update requires*: No Interruption 

`State`  <a name="cfn-batch-computeenvironment-state"></a>
The state of the compute environment\. The valid values are `ENABLED` or `DISABLED`\. An `ENABLED` state indicates that you can register instances with the compute environment and that the associated instances can accept jobs\.  
 *Required*: no  
*Type*: String  
 *Update requires*: No Interruption 

## Return Values<a name="aws-resource-batch-computeenvironment-returnvalues"></a>

### Ref<a name="aws-resource-batch-computeenvironment-ref"></a>

When you pass the logical ID of an `AWS::Batch::ComputeEnvironment` resource to the intrinsic `Ref` function, the function returns the compute environment ARN, such as `arn:aws:batch:us-east-1:555555555555:compute-environment/M4OnDemand`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="aws-resource-batch-computeenvironment-examples"></a>

### Managed Compute Environment<a name="aws-resource-batch-computeenvironment-example1"></a>

The following example creates a managed compute environment called `C4OnDemand` that uses C4 On\-Demand instances and a custom AMI\.

#### JSON<a name="aws-resource-batch-computeenvironment-example1.json"></a>

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
        "Tags": {"Name": "Batch Instance - C4OnDemand"},
        "DesiredvCpus": 48
      },
      "State": "ENABLED"
    }
  }
}
```

#### YAML<a name="aws-resource-batch-computeenvironment-example1.yaml"></a>

```
ComputeEnvironment:
  Type: AWS::Batch::ComputeEnvironment
  Properties:
    [Type](#cfn-batch-computeenvironment-type): MANAGED
    [ServiceRole](#cfn-batch-computeenvironment-servicerole): arn:aws:iam::111122223333:role/service-role/AWSBatchServiceRole
    [ComputeEnvironmentName](#cfn-batch-computeenvironment-computeenvironmentname): C4OnDemand
    [ComputeResources](#cfn-batch-computeenvironment-computeresources):
      [MaxvCpus](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-maxvcpus): 128
      [SecurityGroupIds](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-securitygroupids):
        - sg-abcd1234
      [Type](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-type): EC2
      [Subnets](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-subnets):
        - subnet-aaaaaaaa
        - subnet-bbbbbbbb
        - subnet-cccccccc
      [MinvCpus](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-minvcpus): 0
      [ImageId](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-imageid): ami-a1b2c3d4
      [InstanceRole](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-instancerole): ecsInstanceRole
      [InstanceTypes](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-instancetypes):
        - c4.large
        - c4.xlarge
        - c4.2xlarge
        - c4.4xlarge
        - c4.8xlarge
      [Ec2KeyPair](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-ec2keypair): id_rsa
      [Tags](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-tags): {"Name": "Batch Instance - C4OnDemand"}
      [DesiredvCpus](aws-properties-batch-computeenvironment-computeresources.md#cfn-batch-computeenvironment-computeresources-desiredvcpus): 48
    [State](#cfn-batch-computeenvironment-state): ENABLED
```

### <a name="aws-resource-batch-computeenvironment-example2"></a>

The following example creates a compute environment named `my-first-compute-environment` and specifies tags for the compute resources\.

#### JSON<a name="aws-resource-batch-computeenvironment-example2.json"></a>

```
"MyComputeEnv": {
  "Type": "AWS::Batch::ComputeEnvironment",
  "Properties": {
    "Type": "MANAGED",
    "ServiceRole": "AWSBatchServiceRole",
    "ComputeEnvironmentName": "my-first-compute-environment",
    "ComputeResources": {
      "MinvCpus": "4",
      "MaxvCpus": "256",
      "DesiredvCpus": "4",
      "SecurityGroupIds": [
        "sg-a1b2c3d4",
        "sg-4d3c2ba1"
      ],
      "Type": "EC2",
      "Subnets": [
        "subnet-12345678",
        "subnet-87654321"
      ],
      "InstanceRole": "batch-instance-profile",
      "InstanceTypes": [
        "optimal"
      ],
      "Ec2KeyPair": {
        "Ref": "MyKeyPair"
      },
      "Tags": {
        "Owner": "A",
        "Project": "B"
      }
    },
    "State": "ENABLED"
  }
}
```

#### YAML<a name="aws-resource-batch-computeenvironment-example2.yaml"></a>

```
MyComputeEnv:
  Type: AWS::Batch::ComputeEnvironment
  Properties:
    Type: MANAGED
    ServiceRole: AWSBatchServiceRole
    ComputeEnvironmentName: my-first-compute-environment
    ComputeResources:
      MinvCpus: 4
      MaxvCpus: 256
      DesiredvCpus: 4
      SecurityGroupIds:
        - sg-a1b2c3d4
        - sg-4d3c2ba1
      Type: EC2
      Subnets:
        - subnet-12345678
        - subnet-87654321
      InstanceRole: batch-instance-profile
      InstanceTypes:
        - optimal
      Ec2KeyPair: !Ref MyKeyPair
      Tags:
        Owner: A
        Project: B
    State: ENABLED
```