# AWS::EC2::LaunchTemplate PrivateIpAdd<a name="aws-properties-ec2-launchtemplate-privateipadd"></a>

Specifies a secondary private IPv4 address for a network interface\.

 `PrivateIpAdd` is a property of the [Amazon EC2 LaunchTemplate NetworkInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-networkinterface.html) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-privateipadd-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-privateipadd-syntax.json"></a>

```
{
  "[Primary](#cfn-ec2-launchtemplate-privateipadd-primary)" : Boolean,
  "[PrivateIpAddress](#cfn-ec2-launchtemplate-privateipadd-privateipaddress)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-privateipadd-syntax.yaml"></a>

```
  [Primary](#cfn-ec2-launchtemplate-privateipadd-primary): Boolean
  [PrivateIpAddress](#cfn-ec2-launchtemplate-privateipadd-privateipaddress): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-privateipadd-properties"></a>

`Primary`  <a name="cfn-ec2-launchtemplate-privateipadd-primary"></a>
Indicates whether the private IPv4 address is the primary private IPv4 address\. Only one IPv4 address can be designated as primary\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateIpAddress`  <a name="cfn-ec2-launchtemplate-privateipadd-privateipaddress"></a>
The private IPv4 addresses\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-ec2-launchtemplate-privateipadd--seealso"></a>
+  [ PrivateIpAddressSpecification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_PrivateIpAddressSpecification.html) in the *Amazon Elastic Compute Cloud API Reference* 

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-east-1`
- `ap-northeast-1`
- `ap-northeast-2`
- `ap-northeast-3`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `cn-north-1`
- `cn-northwest-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-east-1`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
