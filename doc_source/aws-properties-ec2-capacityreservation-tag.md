# Amazon EC2 CapacityReservation Tag<a name="aws-properties-ec2-capacityreservation-tag"></a>

<a name="aws-properties-ec2-capacityreservation-tag-description"></a>The `Tag` property type specifies the tag key and value pair to assign to a Capacity Reservation\.

<a name="aws-properties-ec2-capacityreservation-tag-inheritance"></a>`Tag` is a property of the [Amazon EC2 CapacityReservation TagSpecification](aws-properties-ec2-capacityreservation-tagspecification.md) property type\.

## Syntax<a name="aws-properties-ec2-capacityreservation-tag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-capacityreservation-tag-syntax.json"></a>

```
{
  "[Key](#cfn-ec2-capacityreservation-tag-key)" : String,
  "[Value](#cfn-ec2-capacityreservation-tag-value)" : String
}
```

### YAML<a name="aws-properties-ec2-capacityreservation-tag-syntax.yaml"></a>

```
[Key](#cfn-ec2-capacityreservation-tag-key): String
[Value](#cfn-ec2-capacityreservation-tag-value): String
```

## Properties<a name="aws-properties-ec2-capacityreservation-tag-properties"></a>

`Key`  <a name="cfn-ec2-capacityreservation-tag-key"></a>
The key name of the tag\. You can specify a value that is 1 to 127 Unicode characters in length and cannot be prefixed with `aws:`\. You can use any of the following characters: the set of Unicode letters, digits, whitespace, `_`, `.`, `/`, `=`, `+`, and `-`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Value`  <a name="cfn-ec2-capacityreservation-tag-value"></a>
The value for the tag\. You can specify a value that is 1 to 255 Unicode characters in length and cannot be prefixed with `aws:`\. You can use any of the following characters: the set of Unicode letters, digits, whitespace, `_`, `.`, `/`, `=`, `+`, and `-`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-ec2-capacityreservation-tag-seealso"></a>
+ [Tagging Your Amazon EC2 Resources](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html) in the *Amazon Elastic Compute Cloud User Guide*