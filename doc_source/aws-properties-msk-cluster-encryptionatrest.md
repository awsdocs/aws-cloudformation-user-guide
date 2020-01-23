# AWS::MSK::Cluster EncryptionAtRest<a name="aws-properties-msk-cluster-encryptionatrest"></a>

The data volume encryption details\.

## Syntax<a name="aws-properties-msk-cluster-encryptionatrest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-encryptionatrest-syntax.json"></a>

```
{
  "[DataVolumeKMSKeyId](#cfn-msk-cluster-encryptionatrest-datavolumekmskeyid)" : String
}
```

### YAML<a name="aws-properties-msk-cluster-encryptionatrest-syntax.yaml"></a>

```
  [DataVolumeKMSKeyId](#cfn-msk-cluster-encryptionatrest-datavolumekmskeyid): String
```

## Properties<a name="aws-properties-msk-cluster-encryptionatrest-properties"></a>

`DataVolumeKMSKeyId`  <a name="cfn-msk-cluster-encryptionatrest-datavolumekmskeyid"></a>
The ARN of the AWS KMS key for encrypting data at rest\. If you don't specify a KMS key, MSK creates one for you and uses it on your behalf\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)