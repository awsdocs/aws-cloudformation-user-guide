# AWS::QuickSight::Analysis CustomColor<a name="aws-properties-quicksight-analysis-customcolor"></a>

Determines the color that's applied to a particular data value in a column\.

## Syntax<a name="aws-properties-quicksight-analysis-customcolor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-customcolor-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-analysis-customcolor-color)" : String,
  "[FieldValue](#cfn-quicksight-analysis-customcolor-fieldvalue)" : String,
  "[SpecialValue](#cfn-quicksight-analysis-customcolor-specialvalue)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-customcolor-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-analysis-customcolor-color): String
  [FieldValue](#cfn-quicksight-analysis-customcolor-fieldvalue): String
  [SpecialValue](#cfn-quicksight-analysis-customcolor-specialvalue): String
```

## Properties<a name="aws-properties-quicksight-analysis-customcolor-properties"></a>

`Color`  <a name="cfn-quicksight-analysis-customcolor-color"></a>
The color that is applied to the data value\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldValue`  <a name="cfn-quicksight-analysis-customcolor-fieldvalue"></a>
The data value that the color is applied to\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpecialValue`  <a name="cfn-quicksight-analysis-customcolor-specialvalue"></a>
The value of a special data value\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EMPTY | NULL | OTHER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)