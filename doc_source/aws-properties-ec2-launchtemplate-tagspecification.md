# Amazon EC2 LaunchTemplate TagSpecification<a name="aws-properties-ec2-launchtemplate-tagspecification"></a>

<a name="aws-properties-ec2-launchtemplate-tagspecification-description"></a>The `TagSpecification` property type specifies the tags specification for an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-tagspecification-inheritance"></a> `TagSpecification` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](aws-properties-ec2-launchtemplate-launchtemplatedata.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-tagspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-tagspecification-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-launchtemplate-tagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-launchtemplate-tagspecification-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ]
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-tagspecification-syntax.yaml"></a>

```
[ResourceType](#cfn-ec2-launchtemplate-tagspecification-resourcetype): String
[Tags](#cfn-ec2-launchtemplate-tagspecification-tags): 
  - [*Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-properties-ec2-launchtemplate-tagspecification-properties"></a>

`ResourceType`  <a name="cfn-ec2-launchtemplate-tagspecification-resourcetype"></a>
The type of resource to tag\. Currently, the resource types that support tagging on creation are `instance` and `volume`\.  
For a list of valid values, see [LaunchTemplateTagSpecificationRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateTagSpecificationRequest.html) in the *Amazon EC2 API Reference*  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-ec2-launchtemplate-tagspecification-tags"></a>
The tags to apply to the resource\.  
 *Required*: No  
 *Type*: List of [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-tagspecification-seealso"></a>
+ [LaunchTemplateTagSpecificationRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateTagSpecificationRequest.html) in the *Amazon EC2 API Reference*