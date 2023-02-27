# AWS::Timestream::ScheduledQuery TimestreamConfiguration<a name="aws-properties-timestream-scheduledquery-timestreamconfiguration"></a>

 Configuration to write data into Timestream database and table\. This configuration allows the user to map the query result select columns into the destination table columns\. 

## Syntax<a name="aws-properties-timestream-scheduledquery-timestreamconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-scheduledquery-timestreamconfiguration-syntax.json"></a>

```
{
  "[DatabaseName](#cfn-timestream-scheduledquery-timestreamconfiguration-databasename)" : String,
  "[DimensionMappings](#cfn-timestream-scheduledquery-timestreamconfiguration-dimensionmappings)" : [ DimensionMapping, ... ],
  "[MeasureNameColumn](#cfn-timestream-scheduledquery-timestreamconfiguration-measurenamecolumn)" : String,
  "[MixedMeasureMappings](#cfn-timestream-scheduledquery-timestreamconfiguration-mixedmeasuremappings)" : [ MixedMeasureMapping, ... ],
  "[MultiMeasureMappings](#cfn-timestream-scheduledquery-timestreamconfiguration-multimeasuremappings)" : MultiMeasureMappings,
  "[TableName](#cfn-timestream-scheduledquery-timestreamconfiguration-tablename)" : String,
  "[TimeColumn](#cfn-timestream-scheduledquery-timestreamconfiguration-timecolumn)" : String
}
```

### YAML<a name="aws-properties-timestream-scheduledquery-timestreamconfiguration-syntax.yaml"></a>

```
  [DatabaseName](#cfn-timestream-scheduledquery-timestreamconfiguration-databasename): String
  [DimensionMappings](#cfn-timestream-scheduledquery-timestreamconfiguration-dimensionmappings): 
    - DimensionMapping
  [MeasureNameColumn](#cfn-timestream-scheduledquery-timestreamconfiguration-measurenamecolumn): String
  [MixedMeasureMappings](#cfn-timestream-scheduledquery-timestreamconfiguration-mixedmeasuremappings): 
    - MixedMeasureMapping
  [MultiMeasureMappings](#cfn-timestream-scheduledquery-timestreamconfiguration-multimeasuremappings): 
    MultiMeasureMappings
  [TableName](#cfn-timestream-scheduledquery-timestreamconfiguration-tablename): String
  [TimeColumn](#cfn-timestream-scheduledquery-timestreamconfiguration-timecolumn): String
```

## Properties<a name="aws-properties-timestream-scheduledquery-timestreamconfiguration-properties"></a>

`DatabaseName`  <a name="cfn-timestream-scheduledquery-timestreamconfiguration-databasename"></a>
Name of Timestream database to which the query result will be written\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DimensionMappings`  <a name="cfn-timestream-scheduledquery-timestreamconfiguration-dimensionmappings"></a>
 This is to allow mapping column\(s\) from the query result to the dimension in the destination table\.   
*Required*: Yes  
*Type*: List of [DimensionMapping](aws-properties-timestream-scheduledquery-dimensionmapping.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MeasureNameColumn`  <a name="cfn-timestream-scheduledquery-timestreamconfiguration-measurenamecolumn"></a>
Name of the measure column\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MixedMeasureMappings`  <a name="cfn-timestream-scheduledquery-timestreamconfiguration-mixedmeasuremappings"></a>
Specifies how to map measures to multi\-measure records\.  
*Required*: No  
*Type*: List of [MixedMeasureMapping](aws-properties-timestream-scheduledquery-mixedmeasuremapping.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MultiMeasureMappings`  <a name="cfn-timestream-scheduledquery-timestreamconfiguration-multimeasuremappings"></a>
Multi\-measure mappings\.  
*Required*: No  
*Type*: [MultiMeasureMappings](aws-properties-timestream-scheduledquery-multimeasuremappings.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableName`  <a name="cfn-timestream-scheduledquery-timestreamconfiguration-tablename"></a>
Name of Timestream table that the query result will be written to\. The table should be within the same database that is provided in Timestream configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TimeColumn`  <a name="cfn-timestream-scheduledquery-timestreamconfiguration-timecolumn"></a>
Column from query result that should be used as the time column in destination table\. Column type for this should be TIMESTAMP\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)