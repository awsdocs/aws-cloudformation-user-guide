# AWS::EC2::LaunchTemplate ElasticGpuSpecification<a name="aws-properties-ec2-launchtemplate-elasticgpuspecification"></a>

Specifies a specification for an Elastic GPU for an Amazon EC2 launch template\.

 `ElasticGpuSpecification` is a property of [ AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-elasticgpuspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-elasticgpuspecification-syntax.json"></a>

```
{
  "[Type](#cfn-ec2-launchtemplate-elasticgpuspecification-type)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-elasticgpuspecification-syntax.yaml"></a>

```
  [Type](#cfn-ec2-launchtemplate-elasticgpuspecification-type): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-elasticgpuspecification-properties"></a>

`Type`  <a name="cfn-ec2-launchtemplate-elasticgpuspecification-type"></a>
The type of Elastic Graphics accelerator\. For more information about the values to specify for `Type`, see [Elastic Graphics Basics](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/elastic-graphics.html#elastic-graphics-basics), specifically the Elastic Graphics accelerator column, in the *Amazon Elastic Compute Cloud User Guide for Windows Instances*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-elasticgpuspecification--seealso"></a>
+  [ ElasticGpuSpecification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ElasticGpuSpecification.html) in the *Amazon Elastic Compute Cloud API Reference* 

