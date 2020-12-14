# AWS::EC2::NetworkInterface InstanceIpv6Address<a name="aws-properties-ec2-networkinterface-instanceipv6address"></a>

Describes a list of IPv6 addresses to associate with the network interface\.

## Syntax<a name="aws-properties-ec2-networkinterface-instanceipv6address-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinterface-instanceipv6address-syntax.json"></a>

```
{
  "[Ipv6Address](#cfn-ec2-networkinterface-instanceipv6address-ipv6address)" : String
}
```

### YAML<a name="aws-properties-ec2-networkinterface-instanceipv6address-syntax.yaml"></a>

```
  [Ipv6Address](#cfn-ec2-networkinterface-instanceipv6address-ipv6address): String
```

## Properties<a name="aws-properties-ec2-networkinterface-instanceipv6address-properties"></a>

`Ipv6Address`  <a name="cfn-ec2-networkinterface-instanceipv6address-ipv6address"></a>
The IPv6 address to associate with the network interface\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)