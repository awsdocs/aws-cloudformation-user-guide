# AWS::EC2::LaunchTemplate PrivateDnsNameOptions<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions"></a>

Describes the options for instance hostnames\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-syntax.json"></a>

```
{
  "[EnableResourceNameDnsAAAARecord](#cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-enableresourcenamednsaaaarecord)" : Boolean,
  "[EnableResourceNameDnsARecord](#cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-enableresourcenamednsarecord)" : Boolean,
  "[HostnameType](#cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-hostnametype)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-syntax.yaml"></a>

```
  [EnableResourceNameDnsAAAARecord](#cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-enableresourcenamednsaaaarecord): Boolean
  [EnableResourceNameDnsARecord](#cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-enableresourcenamednsarecord): Boolean
  [HostnameType](#cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-hostnametype): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-properties"></a>

`EnableResourceNameDnsAAAARecord`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-enableresourcenamednsaaaarecord"></a>
Indicates whether to respond to DNS queries for instance hostnames with DNS AAAA records\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableResourceNameDnsARecord`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-enableresourcenamednsarecord"></a>
Indicates whether to respond to DNS queries for instance hostnames with DNS A records\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostnameType`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions-hostnametype"></a>
The type of hostname for EC2 instances\. For IPv4 only subnets, an instance DNS name must be based on the instance IPv4 address\. For IPv6 only subnets, an instance DNS name must be based on the instance ID\. For dual\-stack subnets, you can specify whether DNS names use the instance IPv4 address or the instance ID\. For more information, see [Amazon EC2 instance hostname types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-naming.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ip-name | resource-name`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)