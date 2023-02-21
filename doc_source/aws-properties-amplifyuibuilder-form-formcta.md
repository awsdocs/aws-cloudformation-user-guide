# AWS::AmplifyUIBuilder::Form FormCTA<a name="aws-properties-amplifyuibuilder-form-formcta"></a>

Describes the call to action button configuration for the form\.

## Syntax<a name="aws-properties-amplifyuibuilder-form-formcta-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-form-formcta-syntax.json"></a>

```
{
  "[Cancel](#cfn-amplifyuibuilder-form-formcta-cancel)" : FormButton,
  "[Clear](#cfn-amplifyuibuilder-form-formcta-clear)" : FormButton,
  "[Position](#cfn-amplifyuibuilder-form-formcta-position)" : String,
  "[Submit](#cfn-amplifyuibuilder-form-formcta-submit)" : FormButton
}
```

### YAML<a name="aws-properties-amplifyuibuilder-form-formcta-syntax.yaml"></a>

```
  [Cancel](#cfn-amplifyuibuilder-form-formcta-cancel): 
    FormButton
  [Clear](#cfn-amplifyuibuilder-form-formcta-clear): 
    FormButton
  [Position](#cfn-amplifyuibuilder-form-formcta-position): String
  [Submit](#cfn-amplifyuibuilder-form-formcta-submit): 
    FormButton
```

## Properties<a name="aws-properties-amplifyuibuilder-form-formcta-properties"></a>

`Cancel`  <a name="cfn-amplifyuibuilder-form-formcta-cancel"></a>
Displays a cancel button\.  
*Required*: No  
*Type*: [FormButton](aws-properties-amplifyuibuilder-form-formbutton.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Clear`  <a name="cfn-amplifyuibuilder-form-formcta-clear"></a>
Displays a clear button\.  
*Required*: No  
*Type*: [FormButton](aws-properties-amplifyuibuilder-form-formbutton.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Position`  <a name="cfn-amplifyuibuilder-form-formcta-position"></a>
The position of the button\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Submit`  <a name="cfn-amplifyuibuilder-form-formcta-submit"></a>
Displays a submit button\.  
*Required*: No  
*Type*: [FormButton](aws-properties-amplifyuibuilder-form-formbutton.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)