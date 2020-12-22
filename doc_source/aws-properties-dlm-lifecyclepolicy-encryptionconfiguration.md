# AWS::DLM::LifecyclePolicy EncryptionConfiguration<a name="aws-properties-dlm-lifecyclepolicy-encryptionconfiguration"></a>

Specifies the encryption settings for shared snapshots that are copied across Regions\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-encryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-encryptionconfiguration-syntax.json"></a>

```
{
  "[CmkArn](#cfn-dlm-lifecyclepolicy-encryptionconfiguration-cmkarn)" : String,
  "[Encrypted](#cfn-dlm-lifecyclepolicy-encryptionconfiguration-encrypted)" : Boolean
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-encryptionconfiguration-syntax.yaml"></a>

```
  [CmkArn](#cfn-dlm-lifecyclepolicy-encryptionconfiguration-cmkarn): String
  [Encrypted](#cfn-dlm-lifecyclepolicy-encryptionconfiguration-encrypted): Boolean
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-encryptionconfiguration-properties"></a>

`CmkArn`  <a name="cfn-dlm-lifecyclepolicy-encryptionconfiguration-cmkarn"></a>
The Amazon Resource Name \(ARN\) of the AWS KMS customer master key \(CMK\) to use for EBS encryption\. If this parameter is not specified, your AWS managed CMK for EBS is used\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Pattern*: `arn:aws(-[a-z]{1,3}){0,2}:kms:([a-z]+-){2,3}\d:\d+:key/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-dlm-lifecyclepolicy-encryptionconfiguration-encrypted"></a>
To encrypt a copy of an unencrypted snapshot when encryption by default is not enabled, enable encryption using this parameter\. Copies of encrypted snapshots are encrypted, even if this parameter is false or when encryption by default is not enabled\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)