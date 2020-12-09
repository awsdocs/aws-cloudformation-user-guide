# AWS::EC2::Instance ElasticGpuSpecification<a name="aws-properties-ec2-instance-elasticgpuspecification"></a>

Specifies the type of Elastic GPU\. An Elastic GPU is a GPU resource that you can attach to your Amazon EC2 instance to accelerate the graphics performance of your applications\. For more information, see [ Amazon EC2 Elastic GPUs](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/elastic-graphics.html) in the *Amazon EC2 User Guide for Windows Instances*\.

`ElasticGpuSpecification` is a property of the [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\.

## Syntax<a name="aws-properties-ec2-instance-elasticgpuspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-elasticgpuspecification-syntax.json"></a>

```
{
  "[Type](#cfn-ec2-instance-elasticgpuspecification-type)" : String
}
```

### YAML<a name="aws-properties-ec2-instance-elasticgpuspecification-syntax.yaml"></a>

```
  [Type](#cfn-ec2-instance-elasticgpuspecification-type): String
```

## Properties<a name="aws-properties-ec2-instance-elasticgpuspecification-properties"></a>

`Type`  <a name="cfn-ec2-instance-elasticgpuspecification-type"></a>
The type of Elastic Graphics accelerator\. For more information about the values to specify for `Type`, see [Elastic Graphics Basics](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/elastic-graphics.html#elastic-graphics-basics), specifically the Elastic Graphics accelerator column, in the *Amazon Elastic Compute Cloud User Guide for Windows Instances*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)