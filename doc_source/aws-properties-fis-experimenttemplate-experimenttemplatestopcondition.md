# AWS::FIS::ExperimentTemplate ExperimentTemplateStopCondition<a name="aws-properties-fis-experimenttemplate-experimenttemplatestopcondition"></a>

Describes a stop condition for an experiment template\.

## Syntax<a name="aws-properties-fis-experimenttemplate-experimenttemplatestopcondition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-experimenttemplatestopcondition-syntax.json"></a>

```
{
  "[Source](#cfn-fis-experimenttemplate-experimenttemplatestopcondition-source)" : String,
  "[Value](#cfn-fis-experimenttemplate-experimenttemplatestopcondition-value)" : String
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-experimenttemplatestopcondition-syntax.yaml"></a>

```
  [Source](#cfn-fis-experimenttemplate-experimenttemplatestopcondition-source): String
  [Value](#cfn-fis-experimenttemplate-experimenttemplatestopcondition-value): String
```

## Properties<a name="aws-properties-fis-experimenttemplate-experimenttemplatestopcondition-properties"></a>

`Source`  <a name="cfn-fis-experimenttemplate-experimenttemplatestopcondition-source"></a>
The source for the stop condition\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-fis-experimenttemplate-experimenttemplatestopcondition-value"></a>
The Amazon Resource Name \(ARN\) of the CloudWatch alarm, if applicable\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `[\s\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)