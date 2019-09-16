# AWS::EC2::EC2Fleet TagRequest<a name="aws-properties-ec2-ec2fleet-tagrequest"></a>

Specifies the tag key and value pair to use\.

 `TagRequest` is a property of the [ AWS::EC2::TagSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ec2fleet-tagspecification.html) resource\.

## Syntax<a name="aws-properties-ec2-ec2fleet-tagrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-tagrequest-syntax.json"></a>

```
{
  "[Key](#cfn-ec2-ec2fleet-tagrequest-key)" : String,
  "[Value](#cfn-ec2-ec2fleet-tagrequest-value)" : String
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-tagrequest-syntax.yaml"></a>

```
  [Key](#cfn-ec2-ec2fleet-tagrequest-key): String
  [Value](#cfn-ec2-ec2fleet-tagrequest-value): String
```

## Properties<a name="aws-properties-ec2-ec2fleet-tagrequest-properties"></a>

`Key`  <a name="cfn-ec2-ec2fleet-tagrequest-key"></a>
The value of the tag\.  
Constraints: Tag values are case\-sensitive and accept a maximum of 255 Unicode characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-ec2-ec2fleet-tagrequest-value"></a>
The key of the tag\.  
Constraints: Tag keys are case\-sensitive and accept a maximum of 127 Unicode characters\. May not begin with `aws:`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)