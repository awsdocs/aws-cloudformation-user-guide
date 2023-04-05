# AWS::QuickSight::Dashboard SeriesItem<a name="aws-properties-quicksight-dashboard-seriesitem"></a>

The series item configuration of a line chart\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-seriesitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-seriesitem-syntax.json"></a>

```
{
  "[DataFieldSeriesItem](#cfn-quicksight-dashboard-seriesitem-datafieldseriesitem)" : DataFieldSeriesItem,
  "[FieldSeriesItem](#cfn-quicksight-dashboard-seriesitem-fieldseriesitem)" : FieldSeriesItem
}
```

### YAML<a name="aws-properties-quicksight-dashboard-seriesitem-syntax.yaml"></a>

```
  [DataFieldSeriesItem](#cfn-quicksight-dashboard-seriesitem-datafieldseriesitem): 
    DataFieldSeriesItem
  [FieldSeriesItem](#cfn-quicksight-dashboard-seriesitem-fieldseriesitem): 
    FieldSeriesItem
```

## Properties<a name="aws-properties-quicksight-dashboard-seriesitem-properties"></a>

`DataFieldSeriesItem`  <a name="cfn-quicksight-dashboard-seriesitem-datafieldseriesitem"></a>
The data field series item configuration of a line chart\.  
*Required*: No  
*Type*: [DataFieldSeriesItem](aws-properties-quicksight-dashboard-datafieldseriesitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldSeriesItem`  <a name="cfn-quicksight-dashboard-seriesitem-fieldseriesitem"></a>
The field series item configuration of a line chart\.  
*Required*: No  
*Type*: [FieldSeriesItem](aws-properties-quicksight-dashboard-fieldseriesitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)