# AWS::EC2::LaunchTemplate Ipv4PrefixSpecification<a name="aws-properties-ec2-launchtemplate-ipv4prefixspecification"></a>

Specifies an IPv4 prefix for a network interface\.

`Ipv4PrefixSpecification` is a property of [AWS::EC2::LaunchTemplate NetworkInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-networkinterface.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-ipv4prefixspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-ipv4prefixspecification-syntax.json"></a>

```
{
  "[Ipv4Prefix](#cfn-ec2-launchtemplate-ipv4prefixspecification-ipv4prefix)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-ipv4prefixspecification-syntax.yaml"></a>

```
  [Ipv4Prefix](#cfn-ec2-launchtemplate-ipv4prefixspecification-ipv4prefix): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-ipv4prefixspecification-properties"></a>

`Ipv4Prefix`  <a name="cfn-ec2-launchtemplate-ipv4prefixspecification-ipv4prefix"></a>
The IPv4 prefix\. For information, see [ Assigning prefixes to Amazon EC2 network interfaces](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-prefix-eni.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)