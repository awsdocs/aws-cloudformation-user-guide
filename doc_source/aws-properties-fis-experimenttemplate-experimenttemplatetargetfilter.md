# AWS::FIS::ExperimentTemplate ExperimentTemplateTargetFilter<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter"></a>

Describes a filter used for the target resources in an experiment template\.

## Syntax<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter-syntax.json"></a>

```
{
  "[Path](#cfn-fis-experimenttemplate-experimenttemplatetargetfilter-path)" : String,
  "[Values](#cfn-fis-experimenttemplate-experimenttemplatetargetfilter-values)" : ExperimentTemplateTargetFilterValues
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter-syntax.yaml"></a>

```
  [Path](#cfn-fis-experimenttemplate-experimenttemplatetargetfilter-path): String
  [Values](#cfn-fis-experimenttemplate-experimenttemplatetargetfilter-values): 
    ExperimentTemplateTargetFilterValues
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
*Type*: [ExperimentTemplateTargetFilterValues](aws-properties-fis-experimenttemplate-experimenttemplatetargetfiltervalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)