# AWS::IoTWireless::PartnerAccount SidewalkAccountInfoWithFingerprint<a name="aws-properties-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint"></a>

Information about a Sidewalk account\.

## Syntax<a name="aws-properties-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-syntax.json"></a>

```
{
  "[AmazonId](#cfn-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-amazonid)" : String,
  "[Arn](#cfn-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-arn)" : String,
  "[Fingerprint](#cfn-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-fingerprint)" : String
}
```

### YAML<a name="aws-properties-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-syntax.yaml"></a>

```
  [AmazonId](#cfn-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-amazonid): String
  [Arn](#cfn-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-arn): String
  [Fingerprint](#cfn-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-fingerprint): String
```

## Properties<a name="aws-properties-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-properties"></a>

`AmazonId`  <a name="cfn-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-amazonid"></a>
The Sidewalk Amazon ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Arn`  <a name="cfn-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-arn"></a>
The Amazon Resource Name \(ARN\) of the resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Fingerprint`  <a name="cfn-iotwireless-partneraccount-sidewalkaccountinfowithfingerprint-fingerprint"></a>
The fingerprint of the Sidewalk application server private key\.  
*Required*: No  
*Type*: String  
*Minimum*: `64`  
*Maximum*: `64`  
*Pattern*: `[a-fA-F0-9]{64}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)