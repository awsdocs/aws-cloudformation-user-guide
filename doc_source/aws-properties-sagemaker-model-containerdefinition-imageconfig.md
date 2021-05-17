# AWS::SageMaker::Model ImageConfig<a name="aws-properties-sagemaker-model-containerdefinition-imageconfig"></a>

Specifies whether the model container is in Amazon ECR or a private Docker registry accessible from your Amazon Virtual Private Cloud \(VPC\)\.

## Syntax<a name="aws-properties-sagemaker-model-containerdefinition-imageconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-model-containerdefinition-imageconfig-syntax.json"></a>

```
{
  "[RepositoryAccessMode](#cfn-sagemaker-model-containerdefinition-imageconfig-repositoryaccessmode)" : String
}
```

### YAML<a name="aws-properties-sagemaker-model-containerdefinition-imageconfig-syntax.yaml"></a>

```
  [RepositoryAccessMode](#cfn-sagemaker-model-containerdefinition-imageconfig-repositoryaccessmode): String
```

## Properties<a name="aws-properties-sagemaker-model-containerdefinition-imageconfig-properties"></a>

`RepositoryAccessMode`  <a name="cfn-sagemaker-model-containerdefinition-imageconfig-repositoryaccessmode"></a>
Set this to one of the following values:  
+  `Platform` \- The model image is hosted in Amazon ECR\.
+  `Vpc` \- The model image is hosted in a private Docker registry in your VPC\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `Platform | Vpc`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)