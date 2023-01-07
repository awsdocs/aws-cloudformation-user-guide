# AWS::EC2::NetworkAclEntry Icmp<a name="aws-properties-ec2-networkaclentry-icmp"></a>

Describes the ICMP type and code\.

## Syntax<a name="aws-properties-ec2-networkaclentry-icmp-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkaclentry-icmp-syntax.json"></a>

```
{
  "[Code](#cfn-ec2-networkaclentry-icmp-code)" : Integer,
  "[Type](#cfn-ec2-networkaclentry-icmp-type)" : Integer
}
```

### YAML<a name="aws-properties-ec2-networkaclentry-icmp-syntax.yaml"></a>

```
  [Code](#cfn-ec2-networkaclentry-icmp-code): Integer
  [Type](#cfn-ec2-networkaclentry-icmp-type): Integer
```

## Properties<a name="aws-properties-ec2-networkaclentry-icmp-properties"></a>

`Code`  <a name="cfn-ec2-networkaclentry-icmp-code"></a>
The Internet Control Message Protocol \(ICMP\) code\. You can use \-1 to specify all ICMP codes for the given ICMP type\. Requirement is conditional: Required if you specify 1 \(ICMP\) for the protocol parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-ec2-networkaclentry-icmp-type"></a>
The Internet Control Message Protocol \(ICMP\) type\. You can use \-1 to specify all ICMP types\. Conditional requirement: Required if you specify 1 \(ICMP\) for the `CreateNetworkAclEntry` protocol parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)