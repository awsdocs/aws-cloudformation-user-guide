# AWS::AmplifyUIBuilder::Form SectionalElement<a name="aws-properties-amplifyuibuilder-form-sectionalelement"></a>

Stores the configuration information for a visual helper element for a form\. A sectional element can be a header, a text block, or a divider\. These elements are static and not associated with any data\.

## Syntax<a name="aws-properties-amplifyuibuilder-form-sectionalelement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-form-sectionalelement-syntax.json"></a>

```
{
  "[Excluded](#cfn-amplifyuibuilder-form-sectionalelement-excluded)" : Boolean,
  "[Level](#cfn-amplifyuibuilder-form-sectionalelement-level)" : Double,
  "[Orientation](#cfn-amplifyuibuilder-form-sectionalelement-orientation)" : String,
  "[Position](#cfn-amplifyuibuilder-form-sectionalelement-position)" : FieldPosition,
  "[Text](#cfn-amplifyuibuilder-form-sectionalelement-text)" : String,
  "[Type](#cfn-amplifyuibuilder-form-sectionalelement-type)" : String
}
```

### YAML<a name="aws-properties-amplifyuibuilder-form-sectionalelement-syntax.yaml"></a>

```
  [Excluded](#cfn-amplifyuibuilder-form-sectionalelement-excluded): Boolean
  [Level](#cfn-amplifyuibuilder-form-sectionalelement-level): Double
  [Orientation](#cfn-amplifyuibuilder-form-sectionalelement-orientation): String
  [Position](#cfn-amplifyuibuilder-form-sectionalelement-position): 
    FieldPosition
  [Text](#cfn-amplifyuibuilder-form-sectionalelement-text): String
  [Type](#cfn-amplifyuibuilder-form-sectionalelement-type): String
```

## Properties<a name="aws-properties-amplifyuibuilder-form-sectionalelement-properties"></a>

`Excluded`  <a name="cfn-amplifyuibuilder-form-sectionalelement-excluded"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Level`  <a name="cfn-amplifyuibuilder-form-sectionalelement-level"></a>
Specifies the size of the font for a `Heading` sectional element\. Valid values are `1 | 2 | 3 | 4 | 5 | 6`\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Orientation`  <a name="cfn-amplifyuibuilder-form-sectionalelement-orientation"></a>
Specifies the orientation for a `Divider` sectional element\. Valid values are `horizontal` or `vertical`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Position`  <a name="cfn-amplifyuibuilder-form-sectionalelement-position"></a>
Specifies the position of the text in a field for a `Text` sectional element\.  
*Required*: No  
*Type*: [FieldPosition](aws-properties-amplifyuibuilder-form-fieldposition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Text`  <a name="cfn-amplifyuibuilder-form-sectionalelement-text"></a>
The text for a `Text` sectional element\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-amplifyuibuilder-form-sectionalelement-type"></a>
The type of sectional element\. Valid values are `Heading`, `Text`, and `Divider`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)