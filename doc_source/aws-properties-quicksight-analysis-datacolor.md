# AWS::QuickSight::Analysis DataColor<a name="aws-properties-quicksight-analysis-datacolor"></a>

Determines the color that is applied to a particular data value\.

## Syntax<a name="aws-properties-quicksight-analysis-datacolor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-datacolor-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-analysis-datacolor-color)" : String,
  "[DataValue](#cfn-quicksight-analysis-datacolor-datavalue)" : Double
}
```

### YAML<a name="aws-properties-quicksight-analysis-datacolor-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-analysis-datacolor-color): String
  [DataValue](#cfn-quicksight-analysis-datacolor-datavalue): Double
```

## Properties<a name="aws-properties-quicksight-analysis-datacolor-properties"></a>

`Color`  <a name="cfn-quicksight-analysis-datacolor-color"></a>
The color that is applied to the data value\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataValue`  <a name="cfn-quicksight-analysis-datacolor-datavalue"></a>
The data value that the color is applied to\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)