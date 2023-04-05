# AWS::QuickSight::Dashboard PivotTableFieldOption<a name="aws-properties-quicksight-dashboard-pivottablefieldoption"></a>

The selected field options for the pivot table field options\.

## Syntax<a name="aws-properties-quicksight-dashboard-pivottablefieldoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-pivottablefieldoption-syntax.json"></a>

```
{
  "[CustomLabel](#cfn-quicksight-dashboard-pivottablefieldoption-customlabel)" : String,
  "[FieldId](#cfn-quicksight-dashboard-pivottablefieldoption-fieldid)" : String,
  "[Visibility](#cfn-quicksight-dashboard-pivottablefieldoption-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-pivottablefieldoption-syntax.yaml"></a>

```
  [CustomLabel](#cfn-quicksight-dashboard-pivottablefieldoption-customlabel): String
  [FieldId](#cfn-quicksight-dashboard-pivottablefieldoption-fieldid): String
  [Visibility](#cfn-quicksight-dashboard-pivottablefieldoption-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-pivottablefieldoption-properties"></a>

`CustomLabel`  <a name="cfn-quicksight-dashboard-pivottablefieldoption-customlabel"></a>
The custom label of the pivot table field\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-dashboard-pivottablefieldoption-fieldid"></a>
The field ID of the pivot table field\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-pivottablefieldoption-visibility"></a>
The visibility of the pivot table field\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)