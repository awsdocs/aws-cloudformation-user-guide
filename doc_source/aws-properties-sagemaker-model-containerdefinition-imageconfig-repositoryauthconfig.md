# AWS::SageMaker::Model RepositoryAuthConfig<a name="aws-properties-sagemaker-model-containerdefinition-imageconfig-repositoryauthconfig"></a>

Specifies an authentication configuration for the private docker registry where your model image is hosted\. Specify a value for this property only if you specified `Vpc` as the value for the `RepositoryAccessMode` field of the `ImageConfig` object that you passed to a call to `CreateModel` and the private Docker registry where the model image is hosted requires authentication\.

## Syntax<a name="aws-properties-sagemaker-model-containerdefinition-imageconfig-repositoryauthconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-model-containerdefinition-imageconfig-repositoryauthconfig-syntax.json"></a>

```
{
  "[RepositoryCredentialsProviderArn](#cfn-sagemaker-model-containerdefinition-imageconfig-repositoryauthconfig-repositorycredentialsproviderarn)" : String
}
```

### YAML<a name="aws-properties-sagemaker-model-containerdefinition-imageconfig-repositoryauthconfig-syntax.yaml"></a>

```
  [RepositoryCredentialsProviderArn](#cfn-sagemaker-model-containerdefinition-imageconfig-repositoryauthconfig-repositorycredentialsproviderarn): String
```

## Properties<a name="aws-properties-sagemaker-model-containerdefinition-imageconfig-repositoryauthconfig-properties"></a>

`RepositoryCredentialsProviderArn`  <a name="cfn-sagemaker-model-containerdefinition-imageconfig-repositoryauthconfig-repositorycredentialsproviderarn"></a>
The Amazon Resource Name \(ARN\) of an AWS Lambda function that provides credentials to authenticate to the private Docker registry where your model image is hosted\. For information about how to create an AWS Lambda function, see [Create a Lambda function with the console](https://docs.aws.amazon.com/lambda/latest/dg/getting-started-create-function.html) in the * AWS Lambda Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)