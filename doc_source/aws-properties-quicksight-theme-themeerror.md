# AWS::QuickSight::Theme ThemeError<a name="aws-properties-quicksight-theme-themeerror"></a>

Theme error\.

## Syntax<a name="aws-properties-quicksight-theme-themeerror-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-theme-themeerror-syntax.json"></a>

```
{
  "[Message](#cfn-quicksight-theme-themeerror-message)" : String,
  "[Type](#cfn-quicksight-theme-themeerror-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-theme-themeerror-syntax.yaml"></a>

```
  [Message](#cfn-quicksight-theme-themeerror-message): String
  [Type](#cfn-quicksight-theme-themeerror-type): String
```

## Properties<a name="aws-properties-quicksight-theme-themeerror-properties"></a>

`Message`  <a name="cfn-quicksight-theme-themeerror-message"></a>
The error message\.  
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-theme-themeerror-type"></a>
The type of error\.  
*Required*: No  
*Type*: String  
*Allowed values*: `INTERNAL_FAILURE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)