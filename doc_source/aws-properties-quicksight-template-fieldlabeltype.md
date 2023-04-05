# AWS::QuickSight::Template FieldLabelType<a name="aws-properties-quicksight-template-fieldlabeltype"></a>

The field label type\.

## Syntax<a name="aws-properties-quicksight-template-fieldlabeltype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-fieldlabeltype-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-template-fieldlabeltype-fieldid)" : String,
  "[Visibility](#cfn-quicksight-template-fieldlabeltype-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-fieldlabeltype-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-template-fieldlabeltype-fieldid): String
  [Visibility](#cfn-quicksight-template-fieldlabeltype-visibility): String
```

## Properties<a name="aws-properties-quicksight-template-fieldlabeltype-properties"></a>

`FieldId`  <a name="cfn-quicksight-template-fieldlabeltype-fieldid"></a>
Indicates the field that is targeted by the field label\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-template-fieldlabeltype-visibility"></a>
The visibility of the field label\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)