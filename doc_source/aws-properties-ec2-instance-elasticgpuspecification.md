# Amazon EC2 Instance ElasticGpuSpecification<a name="aws-properties-ec2-instance-elasticgpuspecification"></a>

The `ElasticGpuSpecification` property is part of the [AWS::EC2::Instance](aws-properties-ec2-instance.md) resource that specifies the type of Elastic GPU\. An Elastic GPU is a GPU resource that you can attach to your Amazon EC2 instance to accelerate the graphics performance of your applications\. For more information, see [Amazon EC2 Elastic GPUs](http://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/elastic-gpus.html) in the *Amazon EC2 User Guide for Windows Instances*\.

## Syntax<a name="w3ab2c21c14d657b5"></a>

### JSON<a name="aws-properties-ec2-instance-elasticgpuspecification.json"></a>

```
{
  "[Type](#cfn-ec2-instance-elasticgpuspecification-type)" : String
}
```

### YAML<a name="aws-properties-ec2-instance-elasticgpuspecification.yaml"></a>

```
[Type](#cfn-ec2-instance-elasticgpuspecification-type): String
```

## Properties<a name="w3ab2c21c14d657b7"></a>

`Type`  <a name="cfn-ec2-instance-elasticgpuspecification-type"></a>
The type of Elastic GPU\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)