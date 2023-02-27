# AWS::SageMaker::ModelPackage ModelInput<a name="aws-properties-sagemaker-modelpackage-modelinput"></a>

Input object for the model\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-modelinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-modelinput-syntax.json"></a>

```
{
  "[DataInputConfig](#cfn-sagemaker-modelpackage-modelinput-datainputconfig)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-modelinput-syntax.yaml"></a>

```
  [DataInputConfig](#cfn-sagemaker-modelpackage-modelinput-datainputconfig): String
```

## Properties<a name="aws-properties-sagemaker-modelpackage-modelinput-properties"></a>

`DataInputConfig`  <a name="cfn-sagemaker-modelpackage-modelinput-datainputconfig"></a>
The input configuration object for the model\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `[\S\s]+`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)