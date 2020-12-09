# AWS::Kendra::Index ServerSideEncryptionConfiguration<a name="aws-properties-kendra-index-serversideencryptionconfiguration"></a>

Provides the identifier of the AWS KMS customer master key \(CMK\) used to encrypt data indexed by Amazon Kendra\. We suggest that you use a CMK from your account to help secure your index\. Amazon Kendra doesn't support asymmetric CMKs\.

## Syntax<a name="aws-properties-kendra-index-serversideencryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-index-serversideencryptionconfiguration-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-kendra-index-serversideencryptionconfiguration-kmskeyid)" : String
}
```

### YAML<a name="aws-properties-kendra-index-serversideencryptionconfiguration-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-kendra-index-serversideencryptionconfiguration-kmskeyid): String
```

## Properties<a name="aws-properties-kendra-index-serversideencryptionconfiguration-properties"></a>

`KmsKeyId`  <a name="cfn-kendra-index-serversideencryptionconfiguration-kmskeyid"></a>
The identifier of the AWS KMS customer master key \(CMK\)\. Amazon Kendra doesn't support asymmetric CMKs\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)