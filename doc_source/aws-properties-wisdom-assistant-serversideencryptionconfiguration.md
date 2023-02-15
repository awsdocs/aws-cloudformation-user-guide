# AWS::Wisdom::Assistant ServerSideEncryptionConfiguration<a name="aws-properties-wisdom-assistant-serversideencryptionconfiguration"></a>

The KMS key used for encryption\.

## Syntax<a name="aws-properties-wisdom-assistant-serversideencryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wisdom-assistant-serversideencryptionconfiguration-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-wisdom-assistant-serversideencryptionconfiguration-kmskeyid)" : String
}
```

### YAML<a name="aws-properties-wisdom-assistant-serversideencryptionconfiguration-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-wisdom-assistant-serversideencryptionconfiguration-kmskeyid): String
```

## Properties<a name="aws-properties-wisdom-assistant-serversideencryptionconfiguration-properties"></a>

`KmsKeyId`  <a name="cfn-wisdom-assistant-serversideencryptionconfiguration-kmskeyid"></a>
The KMS key\. For information about valid ID values, see [Key identifiers \(KeyId\)](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#key-id)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)