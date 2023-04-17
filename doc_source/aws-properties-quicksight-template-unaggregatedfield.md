# AWS::QuickSight::Template UnaggregatedField<a name="aws-properties-quicksight-template-unaggregatedfield"></a>

The unaggregated field for a table\.

## Syntax<a name="aws-properties-quicksight-template-unaggregatedfield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-unaggregatedfield-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-template-unaggregatedfield-column)" : ColumnIdentifier,
  "[FieldId](#cfn-quicksight-template-unaggregatedfield-fieldid)" : String,
  "[FormatConfiguration](#cfn-quicksight-template-unaggregatedfield-formatconfiguration)" : FormatConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-unaggregatedfield-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-template-unaggregatedfield-column): 
    ColumnIdentifier
  [FieldId](#cfn-quicksight-template-unaggregatedfield-fieldid): String
  [FormatConfiguration](#cfn-quicksight-template-unaggregatedfield-formatconfiguration): 
    FormatConfiguration
```

## Properties<a name="aws-properties-quicksight-template-unaggregatedfield-properties"></a>

`Column`  <a name="cfn-quicksight-template-unaggregatedfield-column"></a>
The column that is used in the `UnaggregatedField`\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-template-unaggregatedfield-fieldid"></a>
The custom field ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatConfiguration`  <a name="cfn-quicksight-template-unaggregatedfield-formatconfiguration"></a>
The format configuration of the field\.  
*Required*: No  
*Type*: [FormatConfiguration](aws-properties-quicksight-template-formatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)