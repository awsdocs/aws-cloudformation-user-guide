# AWS::FIS::ExperimentTemplate ExperimentTemplateTargetFilter<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter"></a>

Specifies a filter used for the target resource input in an experiment template\.

For more information, see [Resource filters](https://docs.aws.amazon.com/fis/latest/userguide/targets.html#target-filters) in the *AWS Fault Injection Simulator User Guide*\.

## Syntax<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter-syntax.json"></a>

```
{
  "[Path](#cfn-fis-experimenttemplate-experimenttemplatetargetfilter-path)" : String,
  "[Values](#cfn-fis-experimenttemplate-experimenttemplatetargetfilter-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter-syntax.yaml"></a>

```
  [Path](#cfn-fis-experimenttemplate-experimenttemplatetargetfilter-path): String
  [Values](#cfn-fis-experimenttemplate-experimenttemplatetargetfilter-values): 
    - String
```

## Properties<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter-properties"></a>

`Path`  <a name="cfn-fis-experimenttemplate-experimenttemplatetargetfilter-path"></a>
The attribute path for the filter\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-fis-experimenttemplate-experimenttemplatetargetfilter-values"></a>
The attribute values for the filter\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)