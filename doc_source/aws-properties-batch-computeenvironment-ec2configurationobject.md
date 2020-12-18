# AWS::Batch::ComputeEnvironment Ec2ConfigurationObject<a name="aws-properties-batch-computeenvironment-ec2configurationobject"></a>

Provides information used to select Amazon Machine Images \(AMIs\) for instances in the compute environment\. If the `Ec2Configuration` isn't specified, the default is `ECS_AL1`\.

**Note**  
This object isn't applicable to jobs running on Fargate resources\.

## Syntax<a name="aws-properties-batch-computeenvironment-ec2configurationobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-computeenvironment-ec2configurationobject-syntax.json"></a>

```
{
  "[ImageIdOverride](#cfn-batch-computeenvironment-ec2configurationobject-imageidoverride)" : String,
  "[ImageType](#cfn-batch-computeenvironment-ec2configurationobject-imagetype)" : String
}
```

### YAML<a name="aws-properties-batch-computeenvironment-ec2configurationobject-syntax.yaml"></a>

```
  [ImageIdOverride](#cfn-batch-computeenvironment-ec2configurationobject-imageidoverride): String
  [ImageType](#cfn-batch-computeenvironment-ec2configurationobject-imagetype): String
```

## Properties<a name="aws-properties-batch-computeenvironment-ec2configurationobject-properties"></a>

`ImageIdOverride`  <a name="cfn-batch-computeenvironment-ec2configurationobject-imageidoverride"></a>
The AMI ID used for instances launched in the compute environment that match the image type\. This setting overrides the `imageId` set in the `computeResource` object\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageType`  <a name="cfn-batch-computeenvironment-ec2configurationobject-imagetype"></a>
The image type to match with the instance type to select an AMI\. If the `imageIdOverride` parameter isn't specified, then a recent [Amazon ECS\-optimized AMI](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-optimized_AMI.html) is used\.    
ECS\_AL2  
 [Amazon Linux 2](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-optimized_AMI.html#al2ami)− Default for all AWS Graviton\-based instance families \(for example, `C6g`, `M6g`, `R6g`, and `T4g`\) and can be used for all non\-GPU instance types\.  
ECS\_AL2\_NVIDIA  
 [Amazon Linux 2 \(GPU\)](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-optimized_AMI.html#gpuami)−Default for all GPU instance families \(for example `P4` and `G4`\) and can be used for all non\-AWS Graviton\-based instance types\.  
ECS\_AL1  
 [Amazon Linux](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-optimized_AMI.html#alami)−Default for all non\-GPU, non\-AWS Graviton instance families\. Amazon Linux is reaching the end\-of\-life of standard support\. For more information, see [Amazon Linux AMI](http://aws.amazon.com/amazon-linux-ami/)\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)