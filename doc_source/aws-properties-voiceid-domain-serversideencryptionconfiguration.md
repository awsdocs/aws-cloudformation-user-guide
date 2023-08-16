# AWS::VoiceID::Domain ServerSideEncryptionConfiguration<a name="aws-properties-voiceid-domain-serversideencryptionconfiguration"></a>

The configuration containing information about the customer managed key used for encrypting customer data\.

## Syntax<a name="aws-properties-voiceid-domain-serversideencryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-voiceid-domain-serversideencryptionconfiguration-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-voiceid-domain-serversideencryptionconfiguration-kmskeyid)" : String
}
```

### YAML<a name="aws-properties-voiceid-domain-serversideencryptionconfiguration-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-voiceid-domain-serversideencryptionconfiguration-kmskeyid): String
```

## Properties<a name="aws-properties-voiceid-domain-serversideencryptionconfiguration-properties"></a>

`KmsKeyId`  <a name="cfn-voiceid-domain-serversideencryptionconfiguration-kmskeyid"></a>
The identifier of the KMS key to use to encrypt data stored by Voice ID\. Voice ID doesn't support asymmetric customer managed keys\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)