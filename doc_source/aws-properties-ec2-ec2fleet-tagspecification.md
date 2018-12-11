# Amazon EC2 EC2Fleet TagSpecification<a name="aws-properties-ec2-ec2fleet-tagspecification"></a>

<a name="aws-properties-ec2-ec2fleet-tagspecification-description"></a>The `TagSpecification` property type specifies the tags to apply to a resource when the resource is being created for an EC2 Fleet\.

<a name="aws-properties-ec2-ec2fleet-tagspecification-inheritance"></a> `TagSpecification` is a property of the [AWS::EC2::EC2Fleet](aws-resource-ec2-ec2fleet.md) resource\.

## Syntax<a name="aws-properties-ec2-ec2fleet-tagspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-tagspecification-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-ec2fleet-tagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-ec2fleet-tagspecification-tags)" : [ [*Resource Tag*](aws-properties-resource-tags.md), ... ]
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-tagspecification-syntax.yaml"></a>

```
[ResourceType](#cfn-ec2-ec2fleet-tagspecification-resourcetype): String
[Tags](#cfn-ec2-ec2fleet-tagspecification-tags): 
  - [*Resouce Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-properties-ec2-ec2fleet-tagspecification-properties"></a>

`ResourceType`  <a name="cfn-ec2-ec2fleet-tagspecification-resourcetype"></a>
The type of resource to tag\. Currently, the resource types that support tagging on creation are `fleet`, `dedicated-host`, `instance`, `snapshot`, and `volume`\. To tag a resource after it has been created, see [CreateTags](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/API_CreateTags.html)\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-ec2-ec2fleet-tagspecification-tags"></a>
One or more tags\. The `value` parameter is required, but if you don't want the tag to have a value, specify the parameter with no value, and we set the value to an empty string\.   
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-ec2fleet-tagspecification-seealso"></a>
+ [TagSpecification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_TagSpecification.html) in the *Amazon EC2 API Reference*