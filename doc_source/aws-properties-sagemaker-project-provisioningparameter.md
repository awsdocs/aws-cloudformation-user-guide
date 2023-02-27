# AWS::SageMaker::Project ProvisioningParameter<a name="aws-properties-sagemaker-project-provisioningparameter"></a>

A key value pair used when you provision a project as a service catalog product\. For information, see [What is AWS Service Catalog](https://docs.aws.amazon.com/servicecatalog/latest/adminguide/introduction.html)\.

## Syntax<a name="aws-properties-sagemaker-project-provisioningparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-project-provisioningparameter-syntax.json"></a>

```
{
  "[Key](#cfn-sagemaker-project-provisioningparameter-key)" : String,
  "[Value](#cfn-sagemaker-project-provisioningparameter-value)" : String
}
```

### YAML<a name="aws-properties-sagemaker-project-provisioningparameter-syntax.yaml"></a>

```
  [Key](#cfn-sagemaker-project-provisioningparameter-key): String
  [Value](#cfn-sagemaker-project-provisioningparameter-value): String
```

## Properties<a name="aws-properties-sagemaker-project-provisioningparameter-properties"></a>

`Key`  <a name="cfn-sagemaker-project-provisioningparameter-key"></a>
The key that identifies a provisioning parameter\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-sagemaker-project-provisioningparameter-value"></a>
The value of the provisioning parameter\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)