# AWS::EC2::SpotFleet PrivateIpAddressSpecification<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses"></a>

Describes a secondary private IPv4 address for a network interface\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-syntax.json"></a>

```
{
  "[Primary](#cfn-ec2-spotfleet-privateipaddressspecification-primary)" : Boolean,
  "[PrivateIpAddress](#cfn-ec2-spotfleet-privateipaddressspecification-privateipaddress)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-syntax.yaml"></a>

```
  [Primary](#cfn-ec2-spotfleet-privateipaddressspecification-primary): Boolean
  [PrivateIpAddress](#cfn-ec2-spotfleet-privateipaddressspecification-privateipaddress): String
```

## Properties<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-properties"></a>

`Primary`  <a name="cfn-ec2-spotfleet-privateipaddressspecification-primary"></a>
Indicates whether the private IPv4 address is the primary private IPv4 address\. Only one IPv4 address can be designated as primary\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateIpAddress`  <a name="cfn-ec2-spotfleet-privateipaddressspecification-privateipaddress"></a>
The private IPv4 addresses\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)