# AWS::QuickSight::Analysis SimpleClusterMarker<a name="aws-properties-quicksight-analysis-simpleclustermarker"></a>

The simple cluster marker of the cluster marker\.

## Syntax<a name="aws-properties-quicksight-analysis-simpleclustermarker-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-simpleclustermarker-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-analysis-simpleclustermarker-color)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-simpleclustermarker-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-analysis-simpleclustermarker-color): String
```

## Properties<a name="aws-properties-quicksight-analysis-simpleclustermarker-properties"></a>

`Color`  <a name="cfn-quicksight-analysis-simpleclustermarker-color"></a>
The color of the simple cluster marker\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)