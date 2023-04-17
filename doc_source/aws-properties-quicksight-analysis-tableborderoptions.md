# AWS::QuickSight::Analysis TableBorderOptions<a name="aws-properties-quicksight-analysis-tableborderoptions"></a>

The border options for a table border\.

## Syntax<a name="aws-properties-quicksight-analysis-tableborderoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-tableborderoptions-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-analysis-tableborderoptions-color)" : String,
  "[Style](#cfn-quicksight-analysis-tableborderoptions-style)" : String,
  "[Thickness](#cfn-quicksight-analysis-tableborderoptions-thickness)" : Double
}
```

### YAML<a name="aws-properties-quicksight-analysis-tableborderoptions-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-analysis-tableborderoptions-color): String
  [Style](#cfn-quicksight-analysis-tableborderoptions-style): String
  [Thickness](#cfn-quicksight-analysis-tableborderoptions-thickness): Double
```

## Properties<a name="aws-properties-quicksight-analysis-tableborderoptions-properties"></a>

`Color`  <a name="cfn-quicksight-analysis-tableborderoptions-color"></a>
The color of a table border\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Style`  <a name="cfn-quicksight-analysis-tableborderoptions-style"></a>
The style \(none, solid\) of a table border\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | SOLID`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Thickness`  <a name="cfn-quicksight-analysis-tableborderoptions-thickness"></a>
The thickness of a table border\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)