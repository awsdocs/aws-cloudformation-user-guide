# Amazon EC2 LaunchTemplate ElasticGpuSpecification<a name="aws-properties-ec2-launchtemplate-elasticgpuspecification"></a>

<a name="aws-properties-ec2-launchtemplate-elasticgpuspecification-description"></a>The `ElasticGpuSpecification` property type specifies a specification for an Elastic GPU for an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-elasticgpuspecification-inheritance"></a> `ElasticGpuSpecification` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](aws-properties-ec2-launchtemplate-launchtemplatedata.md) property type\.

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
The type of Elastic GPU\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-elasticgpuspecification-seealso"></a>
+ [ElasticGpuSpecification](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ElasticGpuSpecification.html) in the *Amazon EC2 API Reference*