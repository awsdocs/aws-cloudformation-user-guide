# AWS::QuickSight::Analysis NegativeValueConfiguration<a name="aws-properties-quicksight-analysis-negativevalueconfiguration"></a>

The options that determine the negative value configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-negativevalueconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-negativevalueconfiguration-syntax.json"></a>

```
{
  "[DisplayMode](#cfn-quicksight-analysis-negativevalueconfiguration-displaymode)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-negativevalueconfiguration-syntax.yaml"></a>

```
  [DisplayMode](#cfn-quicksight-analysis-negativevalueconfiguration-displaymode): String
```

## Properties<a name="aws-properties-quicksight-analysis-negativevalueconfiguration-properties"></a>

`DisplayMode`  <a name="cfn-quicksight-analysis-negativevalueconfiguration-displaymode"></a>
Determines the display mode of the negative value configuration\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `NEGATIVE | POSITIVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)