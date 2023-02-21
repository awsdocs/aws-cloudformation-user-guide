# AWS::AmplifyUIBuilder::Form FormButton<a name="aws-properties-amplifyuibuilder-form-formbutton"></a>

Describes the configuration for a button UI element that is a part of a form\.

## Syntax<a name="aws-properties-amplifyuibuilder-form-formbutton-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-form-formbutton-syntax.json"></a>

```
{
  "[Children](#cfn-amplifyuibuilder-form-formbutton-children)" : String,
  "[Excluded](#cfn-amplifyuibuilder-form-formbutton-excluded)" : Boolean,
  "[Position](#cfn-amplifyuibuilder-form-formbutton-position)" : FieldPosition
}
```

### YAML<a name="aws-properties-amplifyuibuilder-form-formbutton-syntax.yaml"></a>

```
  [Children](#cfn-amplifyuibuilder-form-formbutton-children): String
  [Excluded](#cfn-amplifyuibuilder-form-formbutton-excluded): Boolean
  [Position](#cfn-amplifyuibuilder-form-formbutton-position): 
    FieldPosition
```

## Properties<a name="aws-properties-amplifyuibuilder-form-formbutton-properties"></a>

`Children`  <a name="cfn-amplifyuibuilder-form-formbutton-children"></a>
Describes the button's properties\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Excluded`  <a name="cfn-amplifyuibuilder-form-formbutton-excluded"></a>
Specifies whether the button is visible on the form\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Position`  <a name="cfn-amplifyuibuilder-form-formbutton-position"></a>
The position of the button\.  
*Required*: No  
*Type*: [FieldPosition](aws-properties-amplifyuibuilder-form-fieldposition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)