# AWS::IoTWireless::PartnerAccount SidewalkAccountInfo<a name="aws-properties-iotwireless-partneraccount-sidewalkaccountinfo"></a>

Information about a Sidewalk account\.

## Syntax<a name="aws-properties-iotwireless-partneraccount-sidewalkaccountinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-partneraccount-sidewalkaccountinfo-syntax.json"></a>

```
{
  "[AppServerPrivateKey](#cfn-iotwireless-partneraccount-sidewalkaccountinfo-appserverprivatekey)" : String
}
```

### YAML<a name="aws-properties-iotwireless-partneraccount-sidewalkaccountinfo-syntax.yaml"></a>

```
  [AppServerPrivateKey](#cfn-iotwireless-partneraccount-sidewalkaccountinfo-appserverprivatekey): String
```

## Properties<a name="aws-properties-iotwireless-partneraccount-sidewalkaccountinfo-properties"></a>

`AppServerPrivateKey`  <a name="cfn-iotwireless-partneraccount-sidewalkaccountinfo-appserverprivatekey"></a>
The Sidewalk application server private key\. The application server private key is a secret key, which you should handle in a similar way as you would an application password\. You can protect the application server private key by storing the value in the AWS Secrets Manager and use the [secretsmanager](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html#dynamic-references-secretsmanager) to reference this value\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Pattern*: `[a-fA-F0-9]{64}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)