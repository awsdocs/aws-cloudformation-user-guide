# AWS::QuickSight::Template SheetControlLayout<a name="aws-properties-quicksight-template-sheetcontrollayout"></a>

A grid layout to define the placement of sheet control\.

## Syntax<a name="aws-properties-quicksight-template-sheetcontrollayout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-sheetcontrollayout-syntax.json"></a>

```
{
  "[Configuration](#cfn-quicksight-template-sheetcontrollayout-configuration)" : SheetControlLayoutConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-sheetcontrollayout-syntax.yaml"></a>

```
  [Configuration](#cfn-quicksight-template-sheetcontrollayout-configuration): 
    SheetControlLayoutConfiguration
```

## Properties<a name="aws-properties-quicksight-template-sheetcontrollayout-properties"></a>

`Configuration`  <a name="cfn-quicksight-template-sheetcontrollayout-configuration"></a>
The configuration that determines the elements and canvas size options of sheet control\.  
*Required*: Yes  
*Type*: [SheetControlLayoutConfiguration](aws-properties-quicksight-template-sheetcontrollayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)