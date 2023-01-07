# AWS::Timestream::ScheduledQuery DimensionMapping<a name="aws-properties-timestream-scheduledquery-dimensionmapping"></a>

This type is used to map column\(s\) from the query result to a dimension in the destination table\.

## Syntax<a name="aws-properties-timestream-scheduledquery-dimensionmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-scheduledquery-dimensionmapping-syntax.json"></a>

```
{
  "[DimensionValueType](#cfn-timestream-scheduledquery-dimensionmapping-dimensionvaluetype)" : String,
  "[Name](#cfn-timestream-scheduledquery-dimensionmapping-name)" : String
}
```

### YAML<a name="aws-properties-timestream-scheduledquery-dimensionmapping-syntax.yaml"></a>

```
  [DimensionValueType](#cfn-timestream-scheduledquery-dimensionmapping-dimensionvaluetype): String
  [Name](#cfn-timestream-scheduledquery-dimensionmapping-name): String
```

## Properties<a name="aws-properties-timestream-scheduledquery-dimensionmapping-properties"></a>

`DimensionValueType`  <a name="cfn-timestream-scheduledquery-dimensionmapping-dimensionvaluetype"></a>
Type for the dimension\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-timestream-scheduledquery-dimensionmapping-name"></a>
Column name from query result\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)