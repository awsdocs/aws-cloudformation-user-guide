# AWS::FIS::ExperimentTemplate ExperimentTemplateTarget<a name="aws-properties-fis-experimenttemplate-experimenttemplatetarget"></a>

Specifies a target for an experiment\. You must specify at least one Amazon Resource Name \(ARN\) or at least one resource tag\. You cannot specify both ARNs and tags\.

For more information, see [Targets](https://docs.aws.amazon.com/fis/latest/userguide/targets.html) in the *AWS Fault Injection Simulator User Guide*\.

## Syntax<a name="aws-properties-fis-experimenttemplate-experimenttemplatetarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-experimenttemplatetarget-syntax.json"></a>

```
{
  "[Filters](#cfn-fis-experimenttemplate-experimenttemplatetarget-filters)" : [ ExperimentTemplateTargetFilter, ... ],
  "[Parameters](#cfn-fis-experimenttemplate-experimenttemplatetarget-parameters)" : {Key : Value, ...},
  "[ResourceArns](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcearns)" : [ String, ... ],
  "[ResourceTags](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetags)" : {Key : Value, ...},
  "[ResourceType](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetype)" : String,
  "[SelectionMode](#cfn-fis-experimenttemplate-experimenttemplatetarget-selectionmode)" : String
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-experimenttemplatetarget-syntax.yaml"></a>

```
  [Filters](#cfn-fis-experimenttemplate-experimenttemplatetarget-filters): 
    - ExperimentTemplateTargetFilter
  [Parameters](#cfn-fis-experimenttemplate-experimenttemplatetarget-parameters): 
    Key : Value
  [ResourceArns](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcearns): 
    - String
  [ResourceTags](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetags): 
    Key : Value
  [ResourceType](#cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetype): String
  [SelectionMode](#cfn-fis-experimenttemplate-experimenttemplatetarget-selectionmode): String
```

## Properties<a name="aws-properties-fis-experimenttemplate-experimenttemplatetarget-properties"></a>

`Filters`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-filters"></a>
The filters to apply to identify target resources using specific attributes\.  
*Required*: No  
*Type*: List of [ExperimentTemplateTargetFilter](aws-properties-fis-experimenttemplate-experimenttemplatetargetfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-parameters"></a>
The parameters for the resource type\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceArns`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-resourcearns"></a>
The Amazon Resource Names \(ARNs\) of the resources\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTags`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetags"></a>
The tags for the target resources\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-resourcetype"></a>
The resource type\. The resource type must be supported for the specified action\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectionMode`  <a name="cfn-fis-experimenttemplate-experimenttemplatetarget-selectionmode"></a>
Scopes the identified resources to a specific count of the resources at random, or a percentage of the resources\. All identified resources are included in the target\.  
+ ALL \- Run the action on all identified targets\. This is the default\.
+ COUNT\(n\) \- Run the action on the specified number of targets, chosen from the identified targets at random\. For example, COUNT\(1\) selects one of the targets\.
+ PERCENT\(n\) \- Run the action on the specified percentage of targets, chosen from the identified targets at random\. For example, PERCENT\(25\) selects 25% of the targets\.
*Required*: Yes  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)