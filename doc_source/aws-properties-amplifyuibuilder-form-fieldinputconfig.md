# AWS::AmplifyUIBuilder::Form FieldInputConfig<a name="aws-properties-amplifyuibuilder-form-fieldinputconfig"></a>

Describes the configuration for the default input values to display for a field\.

## Syntax<a name="aws-properties-amplifyuibuilder-form-fieldinputconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-form-fieldinputconfig-syntax.json"></a>

```
{
  "[DefaultChecked](#cfn-amplifyuibuilder-form-fieldinputconfig-defaultchecked)" : Boolean,
  "[DefaultCountryCode](#cfn-amplifyuibuilder-form-fieldinputconfig-defaultcountrycode)" : String,
  "[DefaultValue](#cfn-amplifyuibuilder-form-fieldinputconfig-defaultvalue)" : String,
  "[DescriptiveText](#cfn-amplifyuibuilder-form-fieldinputconfig-descriptivetext)" : String,
  "[IsArray](#cfn-amplifyuibuilder-form-fieldinputconfig-isarray)" : Boolean,
  "[MaxValue](#cfn-amplifyuibuilder-form-fieldinputconfig-maxvalue)" : Double,
  "[MinValue](#cfn-amplifyuibuilder-form-fieldinputconfig-minvalue)" : Double,
  "[Name](#cfn-amplifyuibuilder-form-fieldinputconfig-name)" : String,
  "[Placeholder](#cfn-amplifyuibuilder-form-fieldinputconfig-placeholder)" : String,
  "[ReadOnly](#cfn-amplifyuibuilder-form-fieldinputconfig-readonly)" : Boolean,
  "[Required](#cfn-amplifyuibuilder-form-fieldinputconfig-required)" : Boolean,
  "[Step](#cfn-amplifyuibuilder-form-fieldinputconfig-step)" : Double,
  "[Type](#cfn-amplifyuibuilder-form-fieldinputconfig-type)" : String,
  "[Value](#cfn-amplifyuibuilder-form-fieldinputconfig-value)" : String,
  "[ValueMappings](#cfn-amplifyuibuilder-form-fieldinputconfig-valuemappings)" : ValueMappings
}
```

### YAML<a name="aws-properties-amplifyuibuilder-form-fieldinputconfig-syntax.yaml"></a>

```
  [DefaultChecked](#cfn-amplifyuibuilder-form-fieldinputconfig-defaultchecked): Boolean
  [DefaultCountryCode](#cfn-amplifyuibuilder-form-fieldinputconfig-defaultcountrycode): String
  [DefaultValue](#cfn-amplifyuibuilder-form-fieldinputconfig-defaultvalue): String
  [DescriptiveText](#cfn-amplifyuibuilder-form-fieldinputconfig-descriptivetext): String
  [IsArray](#cfn-amplifyuibuilder-form-fieldinputconfig-isarray): Boolean
  [MaxValue](#cfn-amplifyuibuilder-form-fieldinputconfig-maxvalue): Double
  [MinValue](#cfn-amplifyuibuilder-form-fieldinputconfig-minvalue): Double
  [Name](#cfn-amplifyuibuilder-form-fieldinputconfig-name): String
  [Placeholder](#cfn-amplifyuibuilder-form-fieldinputconfig-placeholder): String
  [ReadOnly](#cfn-amplifyuibuilder-form-fieldinputconfig-readonly): Boolean
  [Required](#cfn-amplifyuibuilder-form-fieldinputconfig-required): Boolean
  [Step](#cfn-amplifyuibuilder-form-fieldinputconfig-step): Double
  [Type](#cfn-amplifyuibuilder-form-fieldinputconfig-type): String
  [Value](#cfn-amplifyuibuilder-form-fieldinputconfig-value): String
  [ValueMappings](#cfn-amplifyuibuilder-form-fieldinputconfig-valuemappings): 
    ValueMappings
```

## Properties<a name="aws-properties-amplifyuibuilder-form-fieldinputconfig-properties"></a>

`DefaultChecked`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-defaultchecked"></a>
Specifies whether a field has a default value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultCountryCode`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-defaultcountrycode"></a>
The default country code for a phone number\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultValue`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-defaultvalue"></a>
The default value for the field\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DescriptiveText`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-descriptivetext"></a>
The text to display to describe the field\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsArray`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-isarray"></a>
Specifies whether to render the field as an array\. This property is ignored if the `dataSourceType` for the form is a Data Store\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxValue`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-maxvalue"></a>
The maximum value to display for the field\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinValue`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-minvalue"></a>
The minimum value to display for the field\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-name"></a>
The name of the field\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Placeholder`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-placeholder"></a>
The text to display as a placeholder for the field\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadOnly`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-readonly"></a>
Specifies a read only field\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Required`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-required"></a>
Specifies a field that requires input\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Step`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-step"></a>
The stepping increment for a numeric value in a field\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-type"></a>
The input type for the field\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-value"></a>
The value for the field\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueMappings`  <a name="cfn-amplifyuibuilder-form-fieldinputconfig-valuemappings"></a>
The information to use to customize the input fields with data at runtime\.  
*Required*: No  
*Type*: [ValueMappings](aws-properties-amplifyuibuilder-form-valuemappings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)