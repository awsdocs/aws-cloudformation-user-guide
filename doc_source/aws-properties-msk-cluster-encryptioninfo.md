# AWS::MSK::Cluster EncryptionInfo<a name="aws-properties-msk-cluster-encryptioninfo"></a>

Includes encryption\-related information, such as the AWS KMS key used for encrypting data at rest and whether you want MSK to encrypt your data in transit\.

## Syntax<a name="aws-properties-msk-cluster-encryptioninfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-encryptioninfo-syntax.json"></a>

```
{
  "[EncryptionAtRest](#cfn-msk-cluster-encryptioninfo-encryptionatrest)" : [EncryptionAtRest](aws-properties-msk-cluster-encryptionatrest.md),
  "[EncryptionInTransit](#cfn-msk-cluster-encryptioninfo-encryptionintransit)" : [EncryptionInTransit](aws-properties-msk-cluster-encryptionintransit.md)
}
```

### YAML<a name="aws-properties-msk-cluster-encryptioninfo-syntax.yaml"></a>

```
  [EncryptionAtRest](#cfn-msk-cluster-encryptioninfo-encryptionatrest): 
    [EncryptionAtRest](aws-properties-msk-cluster-encryptionatrest.md)
  [EncryptionInTransit](#cfn-msk-cluster-encryptioninfo-encryptionintransit): 
    [EncryptionInTransit](aws-properties-msk-cluster-encryptionintransit.md)
```

## Properties<a name="aws-properties-msk-cluster-encryptioninfo-properties"></a>

`EncryptionAtRest`  <a name="cfn-msk-cluster-encryptioninfo-encryptionatrest"></a>
The data\-volume encryption details\.  
*Required*: No  
*Type*: [EncryptionAtRest](aws-properties-msk-cluster-encryptionatrest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EncryptionInTransit`  <a name="cfn-msk-cluster-encryptioninfo-encryptionintransit"></a>
The details for encryption in transit\.  
*Required*: No  
*Type*: [EncryptionInTransit](aws-properties-msk-cluster-encryptionintransit.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-2`
