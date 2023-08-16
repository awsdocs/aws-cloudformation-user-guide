# AWS::SageMaker::ModelCard SecurityConfig<a name="aws-properties-sagemaker-modelcard-securityconfig"></a>

The security configuration used to protect model card data\.

## Syntax<a name="aws-properties-sagemaker-modelcard-securityconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-securityconfig-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-sagemaker-modelcard-securityconfig-kmskeyid)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-securityconfig-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-sagemaker-modelcard-securityconfig-kmskeyid): String
```

## Properties<a name="aws-properties-sagemaker-modelcard-securityconfig-properties"></a>

`KmsKeyId`  <a name="cfn-sagemaker-modelcard-securityconfig-kmskeyid"></a>
A AWS Key Management Service [key ID](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#key-id-key-id) used to encrypt a model card\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)