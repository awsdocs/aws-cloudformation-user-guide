# AWS::Scheduler::Schedule SageMakerPipelineParameter<a name="aws-properties-scheduler-schedule-sagemakerpipelineparameter"></a>

The name and value pair of a parameter to use to start execution of a SageMaker Model Building Pipeline\.

## Syntax<a name="aws-properties-scheduler-schedule-sagemakerpipelineparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-scheduler-schedule-sagemakerpipelineparameter-syntax.json"></a>

```
{
  "[Name](#cfn-scheduler-schedule-sagemakerpipelineparameter-name)" : String,
  "[Value](#cfn-scheduler-schedule-sagemakerpipelineparameter-value)" : String
}
```

### YAML<a name="aws-properties-scheduler-schedule-sagemakerpipelineparameter-syntax.yaml"></a>

```
  [Name](#cfn-scheduler-schedule-sagemakerpipelineparameter-name): String
  [Value](#cfn-scheduler-schedule-sagemakerpipelineparameter-value): String
```

## Properties<a name="aws-properties-scheduler-schedule-sagemakerpipelineparameter-properties"></a>

`Name`  <a name="cfn-scheduler-schedule-sagemakerpipelineparameter-name"></a>
Name of parameter to start execution of a SageMaker Model Building Pipeline\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-scheduler-schedule-sagemakerpipelineparameter-value"></a>
Value of parameter to start execution of a SageMaker Model Building Pipeline\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)