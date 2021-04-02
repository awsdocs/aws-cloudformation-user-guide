# AWS::FIS::ExperimentTemplate ExperimentTemplateActionItemStartAfterList<a name="aws-properties-fis-experimenttemplate-experimenttemplateactionitemstartafterlist"></a>

The name of the action that must be completed before the current action starts\. Omit this parameter to run the action at the start of the experiment\.

## Syntax<a name="aws-properties-fis-experimenttemplate-experimenttemplateactionitemstartafterlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-experimenttemplateactionitemstartafterlist-syntax.json"></a>

```
{
  "[ExperimentTemplateActionItemStartAfterList](#cfn-fis-experimenttemplate-experimenttemplateactionitemstartafterlist-experimenttemplateactionitemstartafterlist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-experimenttemplateactionitemstartafterlist-syntax.yaml"></a>

```
  [ExperimentTemplateActionItemStartAfterList](#cfn-fis-experimenttemplate-experimenttemplateactionitemstartafterlist-experimenttemplateactionitemstartafterlist): 
    - String
```

## Properties<a name="aws-properties-fis-experimenttemplate-experimenttemplateactionitemstartafterlist-properties"></a>

`ExperimentTemplateActionItemStartAfterList`  <a name="cfn-fis-experimenttemplate-experimenttemplateactionitemstartafterlist-experimenttemplateactionitemstartafterlist"></a>
The name of the action that must be completed before the current action starts\. Omit this parameter to run the action at the start of the experiment\.  
*Required*: No  
*Type*: [List](#aws-properties-fis-experimenttemplate-experimenttemplateactionitemstartafterlist) of [String](#aws-properties-fis-experimenttemplate-experimenttemplateactionitemstartafterlist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)