# AWS::Athena::WorkGroup CustomerContentEncryptionConfiguration<a name="aws-properties-athena-workgroup-customercontentencryptionconfiguration"></a>

Specifies the KMS key that is used to encrypt the user's data stores in Athena\.

## Syntax<a name="aws-properties-athena-workgroup-customercontentencryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-workgroup-customercontentencryptionconfiguration-syntax.json"></a>

```
{
  "[KmsKey](#cfn-athena-workgroup-customercontentencryptionconfiguration-kmskey)" : String
}
```

### YAML<a name="aws-properties-athena-workgroup-customercontentencryptionconfiguration-syntax.yaml"></a>

```
  [KmsKey](#cfn-athena-workgroup-customercontentencryptionconfiguration-kmskey): String
```

## Properties<a name="aws-properties-athena-workgroup-customercontentencryptionconfiguration-properties"></a>

`KmsKey`  <a name="cfn-athena-workgroup-customercontentencryptionconfiguration-kmskey"></a>
The KMS key that is used to encrypt the user's data stores in Athena\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^arn:aws[a-z\-]*:kms:([a-z0-9\-]+):\d{12}:key/?[a-zA-Z_0-9+=,.@\-_/]+$|^arn:aws[a-z\-]*:kms:([a-z0-9\-]+):\d{12}:alias/?[a-zA-Z_0-9+=,.@\-_/]+$|^alias/[a-zA-Z0-9/_-]+$|[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)