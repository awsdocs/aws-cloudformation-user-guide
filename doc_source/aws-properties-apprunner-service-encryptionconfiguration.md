# AWS::AppRunner::Service EncryptionConfiguration<a name="aws-properties-apprunner-service-encryptionconfiguration"></a>

Describes a custom encryption key that AWS App Runner uses to encrypt copies of the source repository and service logs\.

## Syntax<a name="aws-properties-apprunner-service-encryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-encryptionconfiguration-syntax.json"></a>

```
{
  "[KmsKey](#cfn-apprunner-service-encryptionconfiguration-kmskey)" : String
}
```

### YAML<a name="aws-properties-apprunner-service-encryptionconfiguration-syntax.yaml"></a>

```
  [KmsKey](#cfn-apprunner-service-encryptionconfiguration-kmskey): String
```

## Properties<a name="aws-properties-apprunner-service-encryptionconfiguration-properties"></a>

`KmsKey`  <a name="cfn-apprunner-service-encryptionconfiguration-kmskey"></a>
The ARN of the KMS key that's used for encryption\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `arn:aws(-[\w]+)*:kms:[a-z\-]+-[0-9]{1}:[0-9]{12}:key\/[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)