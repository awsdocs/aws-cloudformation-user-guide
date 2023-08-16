# AWS::QuickSight::Analysis DataLabelType<a name="aws-properties-quicksight-analysis-datalabeltype"></a>

The option that determines the data label type\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-datalabeltype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-datalabeltype-syntax.json"></a>

```
{
  "[DataPathLabelType](#cfn-quicksight-analysis-datalabeltype-datapathlabeltype)" : DataPathLabelType,
  "[FieldLabelType](#cfn-quicksight-analysis-datalabeltype-fieldlabeltype)" : FieldLabelType,
  "[MaximumLabelType](#cfn-quicksight-analysis-datalabeltype-maximumlabeltype)" : MaximumLabelType,
  "[MinimumLabelType](#cfn-quicksight-analysis-datalabeltype-minimumlabeltype)" : MinimumLabelType,
  "[RangeEndsLabelType](#cfn-quicksight-analysis-datalabeltype-rangeendslabeltype)" : RangeEndsLabelType
}
```

### YAML<a name="aws-properties-quicksight-analysis-datalabeltype-syntax.yaml"></a>

```
  [DataPathLabelType](#cfn-quicksight-analysis-datalabeltype-datapathlabeltype): 
    DataPathLabelType
  [FieldLabelType](#cfn-quicksight-analysis-datalabeltype-fieldlabeltype): 
    FieldLabelType
  [MaximumLabelType](#cfn-quicksight-analysis-datalabeltype-maximumlabeltype): 
    MaximumLabelType
  [MinimumLabelType](#cfn-quicksight-analysis-datalabeltype-minimumlabeltype): 
    MinimumLabelType
  [RangeEndsLabelType](#cfn-quicksight-analysis-datalabeltype-rangeendslabeltype): 
    RangeEndsLabelType
```

## Properties<a name="aws-properties-quicksight-analysis-datalabeltype-properties"></a>

`DataPathLabelType`  <a name="cfn-quicksight-analysis-datalabeltype-datapathlabeltype"></a>
The option that specifies individual data values for labels\.  
*Required*: No  
*Type*: [DataPathLabelType](aws-properties-quicksight-analysis-datapathlabeltype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldLabelType`  <a name="cfn-quicksight-analysis-datalabeltype-fieldlabeltype"></a>
Determines the label configuration for the entire field\.  
*Required*: No  
*Type*: [FieldLabelType](aws-properties-quicksight-analysis-fieldlabeltype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumLabelType`  <a name="cfn-quicksight-analysis-datalabeltype-maximumlabeltype"></a>
Determines the label configuration for the maximum value in a visual\.  
*Required*: No  
*Type*: [MaximumLabelType](aws-properties-quicksight-analysis-maximumlabeltype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumLabelType`  <a name="cfn-quicksight-analysis-datalabeltype-minimumlabeltype"></a>
Determines the label configuration for the minimum value in a visual\.  
*Required*: No  
*Type*: [MinimumLabelType](aws-properties-quicksight-analysis-minimumlabeltype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeEndsLabelType`  <a name="cfn-quicksight-analysis-datalabeltype-rangeendslabeltype"></a>
Determines the label configuration for range end value in a visual\.  
*Required*: No  
*Type*: [RangeEndsLabelType](aws-properties-quicksight-analysis-rangeendslabeltype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)