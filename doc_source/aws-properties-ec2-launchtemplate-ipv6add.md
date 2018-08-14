# Amazon EC2 LaunchTemplate Ipv6Add<a name="aws-properties-ec2-launchtemplate-ipv6add"></a>

<a name="aws-properties-ec2-launchtemplate-ipv6add-description"></a>The `Ipv6Add` property type describes an IPv6 address in an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-ipv6add-inheritance"></a> `Ipv6Add` is a property of the [Amazon EC2 LaunchTemplate NetworkInterface](aws-properties-ec2-launchtemplate-networkinterface.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-ipv6add-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-ipv6add-syntax.json"></a>

```
{
  "[Ipv6Address](#cfn-ec2-launchtemplate-ipv6add-ipv6address)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-ipv6add-syntax.yaml"></a>

```
[Ipv6Address](#cfn-ec2-launchtemplate-ipv6add-ipv6address): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-ipv6add-properties"></a>

`Ipv6Address`  <a name="cfn-ec2-launchtemplate-ipv6add-ipv6address"></a>
The IPv6 address\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-ipv6add-seealso"></a>
+ [InstanceIpv6AddressRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_InstanceIpv6AddressRequest.html) in the *Amazon EC2 API Reference*