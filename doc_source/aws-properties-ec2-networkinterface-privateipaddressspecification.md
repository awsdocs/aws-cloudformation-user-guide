# AWS::EC2::NetworkInterface PrivateIpAddressSpecification<a name="aws-properties-ec2-networkinterface-privateipaddressspecification"></a>

Describes a secondary private IPv4 address for a network interface\.

## Syntax<a name="aws-properties-ec2-networkinterface-privateipaddressspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinterface-privateipaddressspecification-syntax.json"></a>

```
{
  "[Primary](#cfn-ec2-networkinterface-privateipaddressspecification-primary)" : Boolean,
  "[PrivateIpAddress](#cfn-ec2-networkinterface-privateipaddressspecification-privateipaddress)" : String
}
```

### YAML<a name="aws-properties-ec2-networkinterface-privateipaddressspecification-syntax.yaml"></a>

```
  [Primary](#cfn-ec2-networkinterface-privateipaddressspecification-primary): Boolean
  [PrivateIpAddress](#cfn-ec2-networkinterface-privateipaddressspecification-privateipaddress): String
```

## Properties<a name="aws-properties-ec2-networkinterface-privateipaddressspecification-properties"></a>

`Primary`  <a name="cfn-ec2-networkinterface-privateipaddressspecification-primary"></a>
Sets the private IP address as the primary private address\. You can set only one primary private IP address\. If you don't specify a primary private IP address, Amazon EC2 automatically assigns a primary private IP address\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`PrivateIpAddress`  <a name="cfn-ec2-networkinterface-privateipaddressspecification-privateipaddress"></a>
The private IP address of the network interface\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)