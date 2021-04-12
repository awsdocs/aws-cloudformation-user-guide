# AWS::FIS::ExperimentTemplate ExperimentTemplateTargetFilterList<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilterlist"></a>

The filters to apply to identify target resources using specific attributes\.

## Syntax<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilterlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilterlist-syntax.json"></a>

```
{
  "[ExperimentTemplateTargetFilterList](#cfn-fis-experimenttemplate-experimenttemplatetargetfilterlist-experimenttemplatetargetfilterlist)" : [ ExperimentTemplateTargetFilter, ... ]
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilterlist-syntax.yaml"></a>

```
  [ExperimentTemplateTargetFilterList](#cfn-fis-experimenttemplate-experimenttemplatetargetfilterlist-experimenttemplatetargetfilterlist): 
    - ExperimentTemplateTargetFilter
```

## Properties<a name="aws-properties-fis-experimenttemplate-experimenttemplatetargetfilterlist-properties"></a>

`ExperimentTemplateTargetFilterList`  <a name="cfn-fis-experimenttemplate-experimenttemplatetargetfilterlist-experimenttemplatetargetfilterlist"></a>
The filters to apply to identify target resources using specific attributes\.  
*Required*: No  
*Type*: [List](#aws-properties-fis-experimenttemplate-experimenttemplatetargetfilterlist) of [ExperimentTemplateTargetFilter](aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)