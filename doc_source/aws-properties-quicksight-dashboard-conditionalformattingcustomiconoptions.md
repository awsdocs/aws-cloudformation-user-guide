# AWS::QuickSight::Dashboard ConditionalFormattingCustomIconOptions<a name="aws-properties-quicksight-dashboard-conditionalformattingcustomiconoptions"></a>

Custom icon options for an icon set\.

## Syntax<a name="aws-properties-quicksight-dashboard-conditionalformattingcustomiconoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-conditionalformattingcustomiconoptions-syntax.json"></a>

```
{
  "[Icon](#cfn-quicksight-dashboard-conditionalformattingcustomiconoptions-icon)" : String,
  "[UnicodeIcon](#cfn-quicksight-dashboard-conditionalformattingcustomiconoptions-unicodeicon)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-conditionalformattingcustomiconoptions-syntax.yaml"></a>

```
  [Icon](#cfn-quicksight-dashboard-conditionalformattingcustomiconoptions-icon): String
  [UnicodeIcon](#cfn-quicksight-dashboard-conditionalformattingcustomiconoptions-unicodeicon): String
```

## Properties<a name="aws-properties-quicksight-dashboard-conditionalformattingcustomiconoptions-properties"></a>

`Icon`  <a name="cfn-quicksight-dashboard-conditionalformattingcustomiconoptions-icon"></a>
Determines the type of icon\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ARROW_DOWN | ARROW_DOWN_LEFT | ARROW_DOWN_RIGHT | ARROW_LEFT | ARROW_RIGHT | ARROW_UP | ARROW_UP_LEFT | ARROW_UP_RIGHT | CARET_DOWN | CARET_UP | CHECKMARK | CIRCLE | FACE_DOWN | FACE_FLAT | FACE_UP | FLAG | MINUS | ONE_BAR | PLUS | SQUARE | THREE_BAR | THUMBS_DOWN | THUMBS_UP | TRIANGLE | TWO_BAR | X`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnicodeIcon`  <a name="cfn-quicksight-dashboard-conditionalformattingcustomiconoptions-unicodeicon"></a>
Determines the Unicode icon type\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[^\u0000-\u00FF]$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)