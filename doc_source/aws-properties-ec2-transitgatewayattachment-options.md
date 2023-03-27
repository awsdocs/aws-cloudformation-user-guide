# AWS::EC2::TransitGatewayAttachment Options<a name="aws-properties-ec2-transitgatewayattachment-options"></a>

Describes the VPC attachment options\.

## Syntax<a name="aws-properties-ec2-transitgatewayattachment-options-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-transitgatewayattachment-options-syntax.json"></a>

```
{
  "[ApplianceModeSupport](#cfn-ec2-transitgatewayattachment-options-appliancemodesupport)" : String,
  "[DnsSupport](#cfn-ec2-transitgatewayattachment-options-dnssupport)" : String,
  "[Ipv6Support](#cfn-ec2-transitgatewayattachment-options-ipv6support)" : String
}
```

### YAML<a name="aws-properties-ec2-transitgatewayattachment-options-syntax.yaml"></a>

```
  [ApplianceModeSupport](#cfn-ec2-transitgatewayattachment-options-appliancemodesupport): String
  [DnsSupport](#cfn-ec2-transitgatewayattachment-options-dnssupport): String
  [Ipv6Support](#cfn-ec2-transitgatewayattachment-options-ipv6support): String
```

## Properties<a name="aws-properties-ec2-transitgatewayattachment-options-properties"></a>

`ApplianceModeSupport`  <a name="cfn-ec2-transitgatewayattachment-options-appliancemodesupport"></a>
Indicates whether appliance mode support is enabled\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DnsSupport`  <a name="cfn-ec2-transitgatewayattachment-options-dnssupport"></a>
Indicates whether DNS support is enabled\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ipv6Support`  <a name="cfn-ec2-transitgatewayattachment-options-ipv6support"></a>
Indicates whether IPv6 support is disabled\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)