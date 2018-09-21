# Amazon SageMaker NotebookInstanceLifecycleConfig NotebookInstanceLifecycleHook<a name="aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook"></a>

<a name="aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook-description"></a>The `NotebookInstanceLifecycleHook` property type specifies the notebook instance lifecycle configuration script\.

<a name="aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook-inheritance"></a> `NotebookInstanceLifecycleHook` is a property of the [AWS::SageMaker::NotebookInstanceLifecycleConfig](aws-resource-sagemaker-notebookinstancelifecycleconfig.md) resource\.

## Syntax<a name="aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook-syntax.json"></a>

```
{
  "[Content](#cfn-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook-content)" : String
}
```

### YAML<a name="aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook-syntax.yaml"></a>

```
[Content](#cfn-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook-content): String
```

## Properties<a name="aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook-properties"></a>

`Content`  <a name="cfn-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook-content"></a>
A base64\-encoded string that contains a shell script for a notebook instance lifecycle configuration\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 