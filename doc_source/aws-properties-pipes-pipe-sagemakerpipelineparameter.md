# AWS::Pipes::Pipe SageMakerPipelineParameter<a name="aws-properties-pipes-pipe-sagemakerpipelineparameter"></a>

Name/Value pair of a parameter to start execution of a SageMaker Model Building Pipeline\.

## Syntax<a name="aws-properties-pipes-pipe-sagemakerpipelineparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-sagemakerpipelineparameter-syntax.json"></a>

```
{
  "[Name](#cfn-pipes-pipe-sagemakerpipelineparameter-name)" : String,
  "[Value](#cfn-pipes-pipe-sagemakerpipelineparameter-value)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-sagemakerpipelineparameter-syntax.yaml"></a>

```
  [Name](#cfn-pipes-pipe-sagemakerpipelineparameter-name): String
  [Value](#cfn-pipes-pipe-sagemakerpipelineparameter-value): String
```

## Properties<a name="aws-properties-pipes-pipe-sagemakerpipelineparameter-properties"></a>

`Name`  <a name="cfn-pipes-pipe-sagemakerpipelineparameter-name"></a>
Name of parameter to start execution of a SageMaker Model Building Pipeline\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-pipes-pipe-sagemakerpipelineparameter-value"></a>
Value of parameter to start execution of a SageMaker Model Building Pipeline\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)