# AWS::EC2::NetworkInterface Ipv6PrefixSpecification<a name="aws-properties-ec2-networkinterface-ipv6prefixspecification"></a>

Describes the IPv6 prefix\.

## Syntax<a name="aws-properties-ec2-networkinterface-ipv6prefixspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinterface-ipv6prefixspecification-syntax.json"></a>

```
{
  "[Ipv6Prefix](#cfn-ec2-networkinterface-ipv6prefixspecification-ipv6prefix)" : String
}
```

### YAML<a name="aws-properties-ec2-networkinterface-ipv6prefixspecification-syntax.yaml"></a>

```
  [Ipv6Prefix](#cfn-ec2-networkinterface-ipv6prefixspecification-ipv6prefix): String
```

## Properties<a name="aws-properties-ec2-networkinterface-ipv6prefixspecification-properties"></a>

`Ipv6Prefix`  <a name="cfn-ec2-networkinterface-ipv6prefixspecification-ipv6prefix"></a>
The IPv6 prefix\. For information, see [ Assigning prefixes to Amazon EC2 network interfaces](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-prefix-eni.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)