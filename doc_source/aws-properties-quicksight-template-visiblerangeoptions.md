# AWS::QuickSight::Template VisibleRangeOptions<a name="aws-properties-quicksight-template-visiblerangeoptions"></a>

The range options for the data zoom scroll bar\.

## Syntax<a name="aws-properties-quicksight-template-visiblerangeoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-visiblerangeoptions-syntax.json"></a>

```
{
  "[PercentRange](#cfn-quicksight-template-visiblerangeoptions-percentrange)" : PercentVisibleRange
}
```

### YAML<a name="aws-properties-quicksight-template-visiblerangeoptions-syntax.yaml"></a>

```
  [PercentRange](#cfn-quicksight-template-visiblerangeoptions-percentrange): 
    PercentVisibleRange
```

## Properties<a name="aws-properties-quicksight-template-visiblerangeoptions-properties"></a>

`PercentRange`  <a name="cfn-quicksight-template-visiblerangeoptions-percentrange"></a>
The percent range in the visible range\.  
*Required*: No  
*Type*: [PercentVisibleRange](aws-properties-quicksight-template-percentvisiblerange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)