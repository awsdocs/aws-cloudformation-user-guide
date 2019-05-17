# AWS::EC2::NetworkInterface PrivateIpAddressSpecification<a name="aws-properties-ec2-network-interface-privateipspec"></a>

Describes a secondary private IPv4 address for a network interface\.

## Syntax<a name="aws-properties-ec2-network-interface-privateipspec-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-network-interface-privateipspec-syntax.json"></a>

```
{
  "[Primary](#cfn-ec2-networkinterface-privateipspecification-primary)" : Boolean,
  "[PrivateIpAddress](#cfn-ec2-networkinterface-privateipspecification-privateipaddress)" : String
}
```

### YAML<a name="aws-properties-ec2-network-interface-privateipspec-syntax.yaml"></a>

```
  [Primary](#cfn-ec2-networkinterface-privateipspecification-primary): Boolean
  [PrivateIpAddress](#cfn-ec2-networkinterface-privateipspecification-privateipaddress): String
```

## Properties<a name="aws-properties-ec2-network-interface-privateipspec-properties"></a>

`Primary`  <a name="cfn-ec2-networkinterface-privateipspecification-primary"></a>
Sets the private IP address as the primary private address\. You can set only one primary private IP address\. If you don't specify a primary private IP address, Amazon EC2 automatically assigns a primary private IP address\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateIpAddress`  <a name="cfn-ec2-networkinterface-privateipspecification-privateipaddress"></a>
The private IP address of the network interface\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)