# AWS::EC2::NetworkInsightsPath FilterPortRange<a name="aws-properties-ec2-networkinsightspath-filterportrange"></a>

Describes a port range\.

## Syntax<a name="aws-properties-ec2-networkinsightspath-filterportrange-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightspath-filterportrange-syntax.json"></a>

```
{
  "[FromPort](#cfn-ec2-networkinsightspath-filterportrange-fromport)" : Integer,
  "[ToPort](#cfn-ec2-networkinsightspath-filterportrange-toport)" : Integer
}
```

### YAML<a name="aws-properties-ec2-networkinsightspath-filterportrange-syntax.yaml"></a>

```
  [FromPort](#cfn-ec2-networkinsightspath-filterportrange-fromport): Integer
  [ToPort](#cfn-ec2-networkinsightspath-filterportrange-toport): Integer
```

## Properties<a name="aws-properties-ec2-networkinsightspath-filterportrange-properties"></a>

`FromPort`  <a name="cfn-ec2-networkinsightspath-filterportrange-fromport"></a>
The first port in the range\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `65535`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ToPort`  <a name="cfn-ec2-networkinsightspath-filterportrange-toport"></a>
The last port in the range\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `65535`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)