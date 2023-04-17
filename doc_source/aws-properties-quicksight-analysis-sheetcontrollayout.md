# AWS::QuickSight::Analysis SheetControlLayout<a name="aws-properties-quicksight-analysis-sheetcontrollayout"></a>

A grid layout to define the placement of sheet control\.

## Syntax<a name="aws-properties-quicksight-analysis-sheetcontrollayout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-sheetcontrollayout-syntax.json"></a>

```
{
  "[Configuration](#cfn-quicksight-analysis-sheetcontrollayout-configuration)" : SheetControlLayoutConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-sheetcontrollayout-syntax.yaml"></a>

```
  [Configuration](#cfn-quicksight-analysis-sheetcontrollayout-configuration): 
    SheetControlLayoutConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-sheetcontrollayout-properties"></a>

`Configuration`  <a name="cfn-quicksight-analysis-sheetcontrollayout-configuration"></a>
The configuration that determines the elements and canvas size options of sheet control\.  
*Required*: Yes  
*Type*: [SheetControlLayoutConfiguration](aws-properties-quicksight-analysis-sheetcontrollayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)