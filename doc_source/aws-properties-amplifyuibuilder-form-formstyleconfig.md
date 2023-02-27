# AWS::AmplifyUIBuilder::Form FormStyleConfig<a name="aws-properties-amplifyuibuilder-form-formstyleconfig"></a>

Describes the configuration settings for the form's style properties\.

## Syntax<a name="aws-properties-amplifyuibuilder-form-formstyleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-form-formstyleconfig-syntax.json"></a>

```
{
  "[TokenReference](#cfn-amplifyuibuilder-form-formstyleconfig-tokenreference)" : String,
  "[Value](#cfn-amplifyuibuilder-form-formstyleconfig-value)" : String
}
```

### YAML<a name="aws-properties-amplifyuibuilder-form-formstyleconfig-syntax.yaml"></a>

```
  [TokenReference](#cfn-amplifyuibuilder-form-formstyleconfig-tokenreference): String
  [Value](#cfn-amplifyuibuilder-form-formstyleconfig-value): String
```

## Properties<a name="aws-properties-amplifyuibuilder-form-formstyleconfig-properties"></a>

`TokenReference`  <a name="cfn-amplifyuibuilder-form-formstyleconfig-tokenreference"></a>
A reference to a design token to use to bind the form's style properties to an existing theme\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-amplifyuibuilder-form-formstyleconfig-value"></a>
The value of the style setting\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)