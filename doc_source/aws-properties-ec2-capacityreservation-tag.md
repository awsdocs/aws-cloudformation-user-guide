# AWS::EC2::CapacityReservation Tag<a name="aws-properties-ec2-capacityreservation-tag"></a>

Describes a tag\.

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
The key of the tag\.
Constraints: Tag keys are case\-sensitive and accept a maximum of 127 Unicode characters\. May not begin with `aws:`\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-ec2-capacityreservation-tag-value"></a>
The value of the tag\.
Constraints: Tag values are case\-sensitive and accept a maximum of 255 Unicode characters\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
