# AWS::QuickSight::Template DataColor<a name="aws-properties-quicksight-template-datacolor"></a>

Determines the color that is applied to a particular data value\.

## Syntax<a name="aws-properties-quicksight-template-datacolor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-datacolor-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-template-datacolor-color)" : String,
  "[DataValue](#cfn-quicksight-template-datacolor-datavalue)" : Double
}
```

### YAML<a name="aws-properties-quicksight-template-datacolor-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-template-datacolor-color): String
  [DataValue](#cfn-quicksight-template-datacolor-datavalue): Double
```

## Properties<a name="aws-properties-quicksight-template-datacolor-properties"></a>

`Color`  <a name="cfn-quicksight-template-datacolor-color"></a>
The color that is applied to the data value\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataValue`  <a name="cfn-quicksight-template-datacolor-datavalue"></a>
The data value that the color is applied to\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)