# AWS::EC2::Instance PrivateIpAddressSpecification<a name="aws-properties-ec2-network-interface-privateipspec-1"></a>

Specifies a secondary private IPv4 address for a network interface\.

 `PrivateIpAddressSpecification` is a property of the [AWS::EC2::NetworkInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-network-interface.html) resource\.

## Syntax<a name="aws-properties-ec2-network-interface-privateipspec-1-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-network-interface-privateipspec-1-syntax.json"></a>

```
{
  "[Primary](#cfn-ec2-networkinterface-privateipspecification-primary)" : Boolean,
  "[PrivateIpAddress](#cfn-ec2-networkinterface-privateipspecification-privateipaddress)" : String
}
```

### YAML<a name="aws-properties-ec2-network-interface-privateipspec-1-syntax.yaml"></a>

```
  [Primary](#cfn-ec2-networkinterface-privateipspecification-primary): Boolean
  [PrivateIpAddress](#cfn-ec2-networkinterface-privateipspecification-privateipaddress): String
```

## Properties<a name="aws-properties-ec2-network-interface-privateipspec-1-properties"></a>

`Primary`  <a name="cfn-ec2-networkinterface-privateipspecification-primary"></a>
Indicates whether the private IPv4 address is the primary private IPv4 address\. Only one IPv4 address can be designated as primary\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateIpAddress`  <a name="cfn-ec2-networkinterface-privateipspecification-privateipaddress"></a>
The private IPv4 addresses\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)