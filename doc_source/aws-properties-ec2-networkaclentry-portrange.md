# AWS::EC2::NetworkAclEntry PortRange<a name="aws-properties-ec2-networkaclentry-portrange"></a>

Describes a range of ports\.

## Syntax<a name="aws-properties-ec2-networkaclentry-portrange-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkaclentry-portrange-syntax.json"></a>

```
{
  "[From](#cfn-ec2-networkaclentry-portrange-from)" : Integer,
  "[To](#cfn-ec2-networkaclentry-portrange-to)" : Integer
}
```

### YAML<a name="aws-properties-ec2-networkaclentry-portrange-syntax.yaml"></a>

```
  [From](#cfn-ec2-networkaclentry-portrange-from): Integer
  [To](#cfn-ec2-networkaclentry-portrange-to): Integer
```

## Properties<a name="aws-properties-ec2-networkaclentry-portrange-properties"></a>

`From`  <a name="cfn-ec2-networkaclentry-portrange-from"></a>
The first port in the range\. Required if you specify 6 \(TCP\) or 17 \(UDP\) for the protocol parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`To`  <a name="cfn-ec2-networkaclentry-portrange-to"></a>
The last port in the range\. Required if you specify 6 \(TCP\) or 17 \(UDP\) for the protocol parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)