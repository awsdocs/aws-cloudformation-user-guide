# AWS::FIS::ExperimentTemplate ExperimentTemplateAction<a name="aws-properties-fis-experimenttemplate-experimenttemplateaction"></a>

Describes an action for an experiment template\.

## Syntax<a name="aws-properties-fis-experimenttemplate-experimenttemplateaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-experimenttemplateaction-syntax.json"></a>

```
{
  "[actionId](#cfn-fis-experimenttemplate-experimenttemplateaction-actionid)" : String,
  "[description](#cfn-fis-experimenttemplate-experimenttemplateaction-description)" : String,
  "[duration](#cfn-fis-experimenttemplate-experimenttemplateaction-duration)" : String,
  "[parameters](#cfn-fis-experimenttemplate-experimenttemplateaction-parameters)" : ExperimentTemplateActionItemParameterMap,
  "[startAfter](#cfn-fis-experimenttemplate-experimenttemplateaction-startafter)" : ExperimentTemplateActionItemStartAfterList,
  "[targets](#cfn-fis-experimenttemplate-experimenttemplateaction-targets)" : ExperimentTemplateActionItemTargetMap
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-experimenttemplateaction-syntax.yaml"></a>

```
  [actionId](#cfn-fis-experimenttemplate-experimenttemplateaction-actionid): String
  [description](#cfn-fis-experimenttemplate-experimenttemplateaction-description): String
  [duration](#cfn-fis-experimenttemplate-experimenttemplateaction-duration): String
  [parameters](#cfn-fis-experimenttemplate-experimenttemplateaction-parameters): 
    ExperimentTemplateActionItemParameterMap
  [startAfter](#cfn-fis-experimenttemplate-experimenttemplateaction-startafter): 
    ExperimentTemplateActionItemStartAfterList
  [targets](#cfn-fis-experimenttemplate-experimenttemplateaction-targets): 
    ExperimentTemplateActionItemTargetMap
```

## Properties<a name="aws-properties-fis-experimenttemplate-experimenttemplateaction-properties"></a>

`actionId`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-actionid"></a>
The ID of the action\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`description`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-description"></a>
A description for the action\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `[\s\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`duration`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-duration"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`parameters`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-parameters"></a>
The parameters for the action\.  
*Required*: No  
*Type*: [ExperimentTemplateActionItemParameterMap](aws-properties-fis-experimenttemplate-experimenttemplateactionitemparametermap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`startAfter`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-startafter"></a>
The name of the action that must be completed before the current action starts\.  
*Required*: No  
*Type*: [ExperimentTemplateActionItemStartAfterList](aws-properties-fis-experimenttemplate-experimenttemplateactionitemstartafterlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`targets`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-targets"></a>
The targets for the action\.  
*Required*: No  
*Type*: [ExperimentTemplateActionItemTargetMap](aws-properties-fis-experimenttemplate-experimenttemplateactionitemtargetmap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)