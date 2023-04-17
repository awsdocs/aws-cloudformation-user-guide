# AWS::QuickSight::Dashboard DataPathLabelType<a name="aws-properties-quicksight-dashboard-datapathlabeltype"></a>

The option that specifies individual data values for labels\.

## Syntax<a name="aws-properties-quicksight-dashboard-datapathlabeltype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-datapathlabeltype-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-dashboard-datapathlabeltype-fieldid)" : String,
  "[FieldValue](#cfn-quicksight-dashboard-datapathlabeltype-fieldvalue)" : String,
  "[Visibility](#cfn-quicksight-dashboard-datapathlabeltype-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-datapathlabeltype-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-dashboard-datapathlabeltype-fieldid): String
  [FieldValue](#cfn-quicksight-dashboard-datapathlabeltype-fieldvalue): String
  [Visibility](#cfn-quicksight-dashboard-datapathlabeltype-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-datapathlabeltype-properties"></a>

`FieldId`  <a name="cfn-quicksight-dashboard-datapathlabeltype-fieldid"></a>
The field ID of the field that the data label needs to be applied to\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldValue`  <a name="cfn-quicksight-dashboard-datapathlabeltype-fieldvalue"></a>
The actual value of the field that is labeled\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-datapathlabeltype-visibility"></a>
The visibility of the data label\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)