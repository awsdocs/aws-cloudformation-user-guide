# AWS::HealthLake::FHIRDatastore SseConfiguration<a name="aws-properties-healthlake-fhirdatastore-sseconfiguration"></a>

 The server\-side encryption key configuration for a customer provided encryption key\. 

## Syntax<a name="aws-properties-healthlake-fhirdatastore-sseconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-healthlake-fhirdatastore-sseconfiguration-syntax.json"></a>

```
{
  "[KmsEncryptionConfig](#cfn-healthlake-fhirdatastore-sseconfiguration-kmsencryptionconfig)" : Json
}
```

### YAML<a name="aws-properties-healthlake-fhirdatastore-sseconfiguration-syntax.yaml"></a>

```
  [KmsEncryptionConfig](#cfn-healthlake-fhirdatastore-sseconfiguration-kmsencryptionconfig): Json
```

## Properties<a name="aws-properties-healthlake-fhirdatastore-sseconfiguration-properties"></a>

`KmsEncryptionConfig`  <a name="cfn-healthlake-fhirdatastore-sseconfiguration-kmsencryptionconfig"></a>
 The server\-side encryption key configuration for a customer provided encryption key \(CMK\)\.   
*Required*: Yes  
*Type*: [Json](aws-properties-healthlake-fhirdatastore-kmsencryptionconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)