# AWS::FIS::ExperimentTemplate ExperimentTemplateTarget<a name="aws-properties-fis-experimenttemplate-experimenttemplatetarget"></a>

Describes a target for an experiment template\.

## Syntax<a name="aws-properties-fis-experimenttemplate-experimenttemplatetarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-experimenttemplatetarget-syntax.json"></a>

```
{
  "[Filters](#cfn-fis-experimenttemplate-experimenttemplatetarget-filters)" : ExperimentTemplateTargetFilterList,
  "[ResourceArns](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcearns)" : ResourceArnList,
  "[ResourceTags](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetags)" : TagMap,
  "[ResourceType](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetype)" : String,
  "[SelectionMode](#cfn-fis-experimenttemplate-experimenttemplatetarget-selectionmode)" : String
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-experimenttemplatetarget-syntax.yaml"></a>

```
  [Filters](#cfn-fis-experimenttemplate-experimenttemplatetarget-filters): 
    ExperimentTemplateTargetFilterList
  [ResourceArns](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcearns): 
    ResourceArnList
  [ResourceTags](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetags): 
    TagMap
  [ResourceType](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetype): String
  [SelectionMode](#cfn-fis-experimenttemplate-experimenttemplatetarget-selectionmode): String
```

## Properties<a name="aws-properties-fis-experimenttemplate-experimenttemplatetarget-properties"></a>

`Filters`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-filters"></a>
The filters to apply to identify target resources using specific attributes\.  
*Required*: No  
*Type*: [ExperimentTemplateTargetFilterList](aws-properties-fis-experimenttemplate-experimenttemplatetargetfilterlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceArns`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-resourcearns"></a>
The Amazon Resource Names \(ARNs\) of the targets\.  
*Required*: No  
*Type*: [ResourceArnList](aws-properties-fis-experimenttemplate-resourcearnlist.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTags`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetags"></a>
The tags for the target resources\.  
*Required*: No  
*Type*: [TagMap](aws-properties-fis-experimenttemplate-tagmap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetype"></a>
The resource type\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectionMode`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-selectionmode"></a>
Scopes the identified resources to a specific count or percentage\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)