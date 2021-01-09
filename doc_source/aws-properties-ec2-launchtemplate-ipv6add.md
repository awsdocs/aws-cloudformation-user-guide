# AWS::EC2::LaunchTemplate Ipv6Add<a name="aws-properties-ec2-launchtemplate-ipv6add"></a>

Specifies an IPv6 address in an Amazon EC2 launch template\.

`Ipv6Add` is a property of [AWS::EC2::LaunchTemplate NetworkInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-networkinterface.html)\.

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
One or more specific IPv6 addresses from the IPv6 CIDR block range of your subnet\. You can't use this option if you're specifying a number of IPv6 addresses\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-ipv6add--seealso"></a>
+  [ InstanceIpv6AddressRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_InstanceIpv6AddressRequest.html) in the *Amazon Elastic Compute Cloud API Reference* 

