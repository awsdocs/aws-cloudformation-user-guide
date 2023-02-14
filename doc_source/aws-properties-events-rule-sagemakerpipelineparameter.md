# AWS::Events::Rule SageMakerPipelineParameter<a name="aws-properties-events-rule-sagemakerpipelineparameter"></a>

Name/Value pair of a parameter to start execution of a SageMaker Model Building Pipeline\.

## Syntax<a name="aws-properties-events-rule-sagemakerpipelineparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-sagemakerpipelineparameter-syntax.json"></a>

```
{
  "[Name](#cfn-events-rule-sagemakerpipelineparameter-name)" : String,
  "[Value](#cfn-events-rule-sagemakerpipelineparameter-value)" : String
}
```

### YAML<a name="aws-properties-events-rule-sagemakerpipelineparameter-syntax.yaml"></a>

```
  [Name](#cfn-events-rule-sagemakerpipelineparameter-name): String
  [Value](#cfn-events-rule-sagemakerpipelineparameter-value): String
```

## Properties<a name="aws-properties-events-rule-sagemakerpipelineparameter-properties"></a>

`Name`  <a name="cfn-events-rule-sagemakerpipelineparameter-name"></a>
Name of parameter to start execution of a SageMaker Model Building Pipeline\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9])*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-events-rule-sagemakerpipelineparameter-value"></a>
Value of parameter to start execution of a SageMaker Model Building Pipeline\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)