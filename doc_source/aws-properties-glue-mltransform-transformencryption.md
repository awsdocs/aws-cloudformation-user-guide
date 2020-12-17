# AWS::Glue::MLTransform TransformEncryption<a name="aws-properties-glue-mltransform-transformencryption"></a>

The encryption\-at\-rest settings of the transform that apply to accessing user data\. Machine learning transforms can access user data encrypted in Amazon S3 using KMS\.

Additionally, imported labels and trained transforms can now be encrypted using a customer provided KMS key\.

## Syntax<a name="aws-properties-glue-mltransform-transformencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-mltransform-transformencryption-syntax.json"></a>

```
{
  "[MLUserDataEncryption](#cfn-glue-mltransform-transformencryption-mluserdataencryption)" : MLUserDataEncryption,
  "[TaskRunSecurityConfigurationName](#cfn-glue-mltransform-transformencryption-taskrunsecurityconfigurationname)" : String
}
```

### YAML<a name="aws-properties-glue-mltransform-transformencryption-syntax.yaml"></a>

```
  [MLUserDataEncryption](#cfn-glue-mltransform-transformencryption-mluserdataencryption): 
    MLUserDataEncryption
  [TaskRunSecurityConfigurationName](#cfn-glue-mltransform-transformencryption-taskrunsecurityconfigurationname): String
```

## Properties<a name="aws-properties-glue-mltransform-transformencryption-properties"></a>

`MLUserDataEncryption`  <a name="cfn-glue-mltransform-transformencryption-mluserdataencryption"></a>
An `MLUserDataEncryption` object containing the encryption mode and customer\-provided KMS key ID\.  
*Required*: No  
*Type*: [MLUserDataEncryption](aws-properties-glue-mltransform-transformencryption-mluserdataencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskRunSecurityConfigurationName`  <a name="cfn-glue-mltransform-transformencryption-taskrunsecurityconfigurationname"></a>
The name of the security configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)