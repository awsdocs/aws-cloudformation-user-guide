# AWS::Timestream::ScheduledQuery MultiMeasureMappings<a name="aws-properties-timestream-scheduledquery-multimeasuremappings"></a>

Only one of MixedMeasureMappings or MultiMeasureMappings is to be provided\. MultiMeasureMappings can be used to ingest data as multi measures in the derived table\.

## Syntax<a name="aws-properties-timestream-scheduledquery-multimeasuremappings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-scheduledquery-multimeasuremappings-syntax.json"></a>

```
{
  "[MultiMeasureAttributeMappings](#cfn-timestream-scheduledquery-multimeasuremappings-multimeasureattributemappings)" : [ MultiMeasureAttributeMapping, ... ],
  "[TargetMultiMeasureName](#cfn-timestream-scheduledquery-multimeasuremappings-targetmultimeasurename)" : String
}
```

### YAML<a name="aws-properties-timestream-scheduledquery-multimeasuremappings-syntax.yaml"></a>

```
  [MultiMeasureAttributeMappings](#cfn-timestream-scheduledquery-multimeasuremappings-multimeasureattributemappings): 
    - MultiMeasureAttributeMapping
  [TargetMultiMeasureName](#cfn-timestream-scheduledquery-multimeasuremappings-targetmultimeasurename): String
```

## Properties<a name="aws-properties-timestream-scheduledquery-multimeasuremappings-properties"></a>

`MultiMeasureAttributeMappings`  <a name="cfn-timestream-scheduledquery-multimeasuremappings-multimeasureattributemappings"></a>
Required\. Attribute mappings to be used for mapping query results to ingest data for multi\-measure attributes\.  
*Required*: Yes  
*Type*: List of [MultiMeasureAttributeMapping](aws-properties-timestream-scheduledquery-multimeasureattributemapping.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetMultiMeasureName`  <a name="cfn-timestream-scheduledquery-multimeasuremappings-targetmultimeasurename"></a>
The name of the target multi\-measure name in the derived table\. This input is required when measureNameColumn is not provided\. If MeasureNameColumn is provided, then value from that column will be used as multi\-measure name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)