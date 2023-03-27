# AWS::AmplifyUIBuilder::Form FieldValidationConfiguration<a name="aws-properties-amplifyuibuilder-form-fieldvalidationconfiguration"></a>

Describes the validation configuration for a field\.

## Syntax<a name="aws-properties-amplifyuibuilder-form-fieldvalidationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-form-fieldvalidationconfiguration-syntax.json"></a>

```
{
  "[NumValues](#cfn-amplifyuibuilder-form-fieldvalidationconfiguration-numvalues)" : [ Double, ... ],
  "[StrValues](#cfn-amplifyuibuilder-form-fieldvalidationconfiguration-strvalues)" : [ String, ... ],
  "[Type](#cfn-amplifyuibuilder-form-fieldvalidationconfiguration-type)" : String,
  "[ValidationMessage](#cfn-amplifyuibuilder-form-fieldvalidationconfiguration-validationmessage)" : String
}
```

### YAML<a name="aws-properties-amplifyuibuilder-form-fieldvalidationconfiguration-syntax.yaml"></a>

```
  [NumValues](#cfn-amplifyuibuilder-form-fieldvalidationconfiguration-numvalues): 
    - Double
  [StrValues](#cfn-amplifyuibuilder-form-fieldvalidationconfiguration-strvalues): 
    - String
  [Type](#cfn-amplifyuibuilder-form-fieldvalidationconfiguration-type): String
  [ValidationMessage](#cfn-amplifyuibuilder-form-fieldvalidationconfiguration-validationmessage): String
```

## Properties<a name="aws-properties-amplifyuibuilder-form-fieldvalidationconfiguration-properties"></a>

`NumValues`  <a name="cfn-amplifyuibuilder-form-fieldvalidationconfiguration-numvalues"></a>
The validation to perform on a number value\.  
*Required*: No  
*Type*: List of Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StrValues`  <a name="cfn-amplifyuibuilder-form-fieldvalidationconfiguration-strvalues"></a>
The validation to perform on a string value\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-amplifyuibuilder-form-fieldvalidationconfiguration-type"></a>
The validation to perform on an object type\.``  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidationMessage`  <a name="cfn-amplifyuibuilder-form-fieldvalidationconfiguration-validationmessage"></a>
The validation message to display\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)