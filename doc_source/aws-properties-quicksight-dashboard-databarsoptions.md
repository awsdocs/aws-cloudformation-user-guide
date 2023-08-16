# AWS::QuickSight::Dashboard DataBarsOptions<a name="aws-properties-quicksight-dashboard-databarsoptions"></a>

The options for data bars\.

## Syntax<a name="aws-properties-quicksight-dashboard-databarsoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-databarsoptions-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-dashboard-databarsoptions-fieldid)" : String,
  "[NegativeColor](#cfn-quicksight-dashboard-databarsoptions-negativecolor)" : String,
  "[PositiveColor](#cfn-quicksight-dashboard-databarsoptions-positivecolor)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-databarsoptions-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-dashboard-databarsoptions-fieldid): String
  [NegativeColor](#cfn-quicksight-dashboard-databarsoptions-negativecolor): String
  [PositiveColor](#cfn-quicksight-dashboard-databarsoptions-positivecolor): String
```

## Properties<a name="aws-properties-quicksight-dashboard-databarsoptions-properties"></a>

`FieldId`  <a name="cfn-quicksight-dashboard-databarsoptions-fieldid"></a>
The field ID for the data bars options\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NegativeColor`  <a name="cfn-quicksight-dashboard-databarsoptions-negativecolor"></a>
The color of the negative data bar\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PositiveColor`  <a name="cfn-quicksight-dashboard-databarsoptions-positivecolor"></a>
The color of the positive data bar\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)