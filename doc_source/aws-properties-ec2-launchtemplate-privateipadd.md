# Amazon EC2 LaunchTemplate PrivateIpAdd<a name="aws-properties-ec2-launchtemplate-privateipadd"></a>

<a name="aws-properties-ec2-launchtemplate-privateipadd-description"></a>The `PrivateIpAdd` property type describes a private IPv4 address for a network interface in an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-privateipadd-inheritance"></a> `PrivateIpAdd` is a property of the [Amazon EC2 LaunchTemplate NetworkInterface](aws-properties-ec2-launchtemplate-networkinterface.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-privateipadd-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-privateipadd-syntax.json"></a>

```
{
  "[PrivateIpAddress](#cfn-ec2-launchtemplate-privateipadd-privateipaddress)" : String,
  "[Primary](#cfn-ec2-launchtemplate-privateipadd-primary)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-privateipadd-syntax.yaml"></a>

```
[PrivateIpAddress](#cfn-ec2-launchtemplate-privateipadd-privateipaddress): String
[Primary](#cfn-ec2-launchtemplate-privateipadd-primary): Boolean
```

## Properties<a name="aws-properties-ec2-launchtemplate-privateipadd-properties"></a>

`Primary`  <a name="cfn-ec2-launchtemplate-privateipadd-primary"></a>
Indicates whether the private IPv4 address is the primary private IPv4 address\. Only one IPv4 address can be designated as primary\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PrivateIpAddress`  <a name="cfn-ec2-launchtemplate-privateipadd-privateipaddress"></a>
The private IPv4 address\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-privateipadd-seealso"></a>
+ [PrivateIpAddressSpecification](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_PrivateIpAddressSpecification.html) in the *Amazon EC2 API Reference*