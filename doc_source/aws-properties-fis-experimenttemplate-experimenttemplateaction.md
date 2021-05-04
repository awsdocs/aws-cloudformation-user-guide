# AWS::FIS::ExperimentTemplate ExperimentTemplateAction<a name="aws-properties-fis-experimenttemplate-experimenttemplateaction"></a>

Specifies an action for an experiment template\.

For more information, see [Actions](https://docs.aws.amazon.com/fis/latest/userguide/actions.html) in the *AWS Fault Injection Simulator User Guide*\.

## Syntax<a name="aws-properties-fis-experimenttemplate-experimenttemplateaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-experimenttemplateaction-syntax.json"></a>

```
{
  "[ActionId](#cfn-fis-experimenttemplate-experimenttemplateaction-actionid)" : String,
  "[Description](#cfn-fis-experimenttemplate-experimenttemplateaction-description)" : String,
  "[Parameters](#cfn-fis-experimenttemplate-experimenttemplateaction-parameters)" : ExperimentTemplateActionItemParameterMap,
  "[StartAfter](#cfn-fis-experimenttemplate-experimenttemplateaction-startafter)" : [ String, ... ],
  "[Targets](#cfn-fis-experimenttemplate-experimenttemplateaction-targets)" : ExperimentTemplateActionItemTargetMap
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-experimenttemplateaction-syntax.yaml"></a>

```
  [ActionId](#cfn-fis-experimenttemplate-experimenttemplateaction-actionid): String
  [Description](#cfn-fis-experimenttemplate-experimenttemplateaction-description): String
  [Parameters](#cfn-fis-experimenttemplate-experimenttemplateaction-parameters): 
    ExperimentTemplateActionItemParameterMap
  [StartAfter](#cfn-fis-experimenttemplate-experimenttemplateaction-startafter): 
    - String
  [Targets](#cfn-fis-experimenttemplate-experimenttemplateaction-targets): 
    ExperimentTemplateActionItemTargetMap
```

## Properties<a name="aws-properties-fis-experimenttemplate-experimenttemplateaction-properties"></a>

`ActionId`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-actionid"></a>
The ID of the action\. The format of the action ID is: aws:*service\-name*:*action\-type*\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-description"></a>
A description for the action\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `[\s\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-parameters"></a>
The parameters for the action, if applicable\.  
*Required*: No  
*Type*: [ExperimentTemplateActionItemParameterMap](aws-properties-fis-experimenttemplate-experimenttemplateactionitemparametermap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartAfter`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-startafter"></a>
The name of the action that must be completed before the current action starts\. Omit this parameter to run the action at the start of the experiment\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-fis-experimenttemplate-experimenttemplateaction-targets"></a>
The targets for the action\.  
*Required*: No  
*Type*: [ExperimentTemplateActionItemTargetMap](aws-properties-fis-experimenttemplate-experimenttemplateactionitemtargetmap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)