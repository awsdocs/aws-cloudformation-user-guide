# AWS::Glue::SecurityConfiguration<a name="aws-resource-glue-securityconfiguration"></a>

Creates a new security configuration\. A security configuration is a set of security properties that can be used by AWS Glue\. You can use a security configuration to encrypt data at rest\. For information about using security configurations in AWS Glue, see [Encrypting Data Written by Crawlers, Jobs, and Development Endpoints](https://docs.aws.amazon.com/glue/latest/dg/encryption-security-configuration.html)\.

## Syntax<a name="aws-resource-glue-securityconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-securityconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::SecurityConfiguration",
  "Properties" : {
      "[EncryptionConfiguration](#cfn-glue-securityconfiguration-encryptionconfiguration)" : EncryptionConfiguration,
      "[Name](#cfn-glue-securityconfiguration-name)" : String
    }
}
```

### YAML<a name="aws-resource-glue-securityconfiguration-syntax.yaml"></a>

```
Type: AWS::Glue::SecurityConfiguration
Properties: 
  [EncryptionConfiguration](#cfn-glue-securityconfiguration-encryptionconfiguration): 
    EncryptionConfiguration
  [Name](#cfn-glue-securityconfiguration-name): String
```

## Properties<a name="aws-resource-glue-securityconfiguration-properties"></a>

`EncryptionConfiguration`  <a name="cfn-glue-securityconfiguration-encryptionconfiguration"></a>
The encryption configuration associated with this security configuration\.  
*Required*: Yes  
*Type*: [EncryptionConfiguration](aws-properties-glue-securityconfiguration-encryptionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-securityconfiguration-name"></a>
The name of the security configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-glue-securityconfiguration-return-values"></a>

### Ref<a name="aws-resource-glue-securityconfiguration-return-values-ref"></a>