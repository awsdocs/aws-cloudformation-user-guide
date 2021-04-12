# AWS::FIS::ExperimentTemplate<a name="aws-resource-fis-experimenttemplate"></a>

Specifies an experiment template\.

## Syntax<a name="aws-resource-fis-experimenttemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-fis-experimenttemplate-syntax.json"></a>

```
{
  "Type" : "AWS::FIS::ExperimentTemplate",
  "Properties" : {
      "[Actions](#cfn-fis-experimenttemplate-actions)" : {Key : Value, ...},
      "[Description](#cfn-fis-experimenttemplate-description)" : String,
      "[RoleArn](#cfn-fis-experimenttemplate-rolearn)" : String,
      "[StopConditions](#cfn-fis-experimenttemplate-stopconditions)" : [ ExperimentTemplateStopCondition, ... ],
      "[Tags](#cfn-fis-experimenttemplate-tags)" : {Key : Value, ...},
      "[Targets](#cfn-fis-experimenttemplate-targets)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-fis-experimenttemplate-syntax.yaml"></a>

```
Type: AWS::FIS::ExperimentTemplate
Properties: 
  [Actions](#cfn-fis-experimenttemplate-actions): 
    Key : Value
  [Description](#cfn-fis-experimenttemplate-description): String
  [RoleArn](#cfn-fis-experimenttemplate-rolearn): String
  [StopConditions](#cfn-fis-experimenttemplate-stopconditions): 
    - ExperimentTemplateStopCondition
  [Tags](#cfn-fis-experimenttemplate-tags): 
    Key : Value
  [Targets](#cfn-fis-experimenttemplate-targets): 
    Key : Value
```

## Properties<a name="aws-resource-fis-experimenttemplate-properties"></a>

`Actions`  <a name="cfn-fis-experimenttemplate-actions"></a>
The actions for the experiment\.  
*Required*: No  
*Type*: Map of [ExperimentTemplateAction](aws-properties-fis-experimenttemplate-experimenttemplateaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-fis-experimenttemplate-description"></a>
The description for the experiment template\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `[\s\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-fis-experimenttemplate-rolearn"></a>
The Amazon Resource Name \(ARN\) of an IAM role\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StopConditions`  <a name="cfn-fis-experimenttemplate-stopconditions"></a>
The stop conditions for the experiment\.  
*Required*: Yes  
*Type*: List of [ExperimentTemplateStopCondition](aws-properties-fis-experimenttemplate-experimenttemplatestopcondition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-fis-experimenttemplate-tags"></a>
The tags for the experiment template\.  
*Required*: Yes  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Targets`  <a name="cfn-fis-experimenttemplate-targets"></a>
The targets for the experiment\.  
*Required*: Yes  
*Type*: Map of [ExperimentTemplateTarget](aws-properties-fis-experimenttemplate-experimenttemplatetarget.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-fis-experimenttemplate-return-values"></a>

### Ref<a name="aws-resource-fis-experimenttemplate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the experiment template ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-fis-experimenttemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-fis-experimenttemplate-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the experiment template\.