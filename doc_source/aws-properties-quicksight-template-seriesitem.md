# AWS::QuickSight::Template SeriesItem<a name="aws-properties-quicksight-template-seriesitem"></a>

The series item configuration of a line chart\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-seriesitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-seriesitem-syntax.json"></a>

```
{
  "[DataFieldSeriesItem](#cfn-quicksight-template-seriesitem-datafieldseriesitem)" : DataFieldSeriesItem,
  "[FieldSeriesItem](#cfn-quicksight-template-seriesitem-fieldseriesitem)" : FieldSeriesItem
}
```

### YAML<a name="aws-properties-quicksight-template-seriesitem-syntax.yaml"></a>

```
  [DataFieldSeriesItem](#cfn-quicksight-template-seriesitem-datafieldseriesitem): 
    DataFieldSeriesItem
  [FieldSeriesItem](#cfn-quicksight-template-seriesitem-fieldseriesitem): 
    FieldSeriesItem
```

## Properties<a name="aws-properties-quicksight-template-seriesitem-properties"></a>

`DataFieldSeriesItem`  <a name="cfn-quicksight-template-seriesitem-datafieldseriesitem"></a>
The data field series item configuration of a line chart\.  
*Required*: No  
*Type*: [DataFieldSeriesItem](aws-properties-quicksight-template-datafieldseriesitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldSeriesItem`  <a name="cfn-quicksight-template-seriesitem-fieldseriesitem"></a>
The field series item configuration of a line chart\.  
*Required*: No  
*Type*: [FieldSeriesItem](aws-properties-quicksight-template-fieldseriesitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)