# AWS::SageMaker::CodeRepository<a name="aws-resource-sagemaker-coderepository"></a>

Creates a Git repository as a resource in your Amazon SageMaker account\. You can associate the repository with notebook instances so that you can use Git source control for the notebooks you create\. The Git repository is a resource in your Amazon SageMaker account, so it can be associated with more than one notebook instance, and it persists independently from the lifecycle of any notebook instances it is associated with\.

The repository can be hosted either in [AWS CodeCommit](https://docs.aws.amazon.com/codecommit/latest/userguide/welcome.html) or in any other Git repository\.

## Syntax<a name="aws-resource-sagemaker-coderepository-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-coderepository-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::CodeRepository",
  "Properties" : {
      "[CodeRepositoryName](#cfn-sagemaker-coderepository-coderepositoryname)" : String,
      "[GitConfig](#cfn-sagemaker-coderepository-gitconfig)" : [GitConfig](aws-properties-sagemaker-coderepository-gitconfig.md)
    }
}
```

### YAML<a name="aws-resource-sagemaker-coderepository-syntax.yaml"></a>

```
Type: AWS::SageMaker::CodeRepository
Properties: 
  [CodeRepositoryName](#cfn-sagemaker-coderepository-coderepositoryname): String
  [GitConfig](#cfn-sagemaker-coderepository-gitconfig): 
    [GitConfig](aws-properties-sagemaker-coderepository-gitconfig.md)
```

## Properties<a name="aws-resource-sagemaker-coderepository-properties"></a>

`CodeRepositoryName`  <a name="cfn-sagemaker-coderepository-coderepositoryname"></a>
The name of the Git repository\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9])*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GitConfig`  <a name="cfn-sagemaker-coderepository-gitconfig"></a>
Configuration details for the Git repository, including the URL where it is located and the ARN of the AWS Secrets Manager secret that contains the credentials used to access the repository\.  
*Required*: Yes  
*Type*: [GitConfig](aws-properties-sagemaker-coderepository-gitconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-sagemaker-coderepository-return-values"></a>

### Ref<a name="aws-resource-sagemaker-coderepository-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the new repository\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-coderepository-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-sagemaker-coderepository-return-values-fn--getatt-fn--getatt"></a>

`CodeRepositoryName`  <a name="CodeRepositoryName-fn::getatt"></a>
The name of the Git repository\.