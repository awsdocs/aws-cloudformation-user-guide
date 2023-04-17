# AWS::QuickSight::Analysis RelativeDateTimeControlDisplayOptions<a name="aws-properties-quicksight-analysis-relativedatetimecontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-analysis-relativedatetimecontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-relativedatetimecontroldisplayoptions-syntax.json"></a>

```
{
  "[DateTimeFormat](#cfn-quicksight-analysis-relativedatetimecontroldisplayoptions-datetimeformat)" : String,
  "[TitleOptions](#cfn-quicksight-analysis-relativedatetimecontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-relativedatetimecontroldisplayoptions-syntax.yaml"></a>

```
  [DateTimeFormat](#cfn-quicksight-analysis-relativedatetimecontroldisplayoptions-datetimeformat): String
  [TitleOptions](#cfn-quicksight-analysis-relativedatetimecontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-analysis-relativedatetimecontroldisplayoptions-properties"></a>

`DateTimeFormat`  <a name="cfn-quicksight-analysis-relativedatetimecontroldisplayoptions-datetimeformat"></a>
Customize how dates are formatted in controls\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-analysis-relativedatetimecontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-analysis-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)