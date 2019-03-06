# AWS IoT Analytics Dataset QueryAction<a name="aws-properties-iotanalytics-dataset-queryaction"></a>

<a name="aws-properties-iotanalytics-dataset-queryaction-description"></a>The `QueryAction` property type specifies how to automatically create data set contents using an SQL query for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-queryaction-inheritance"></a> `QueryAction` is a property of the [Action](aws-properties-iotanalytics-dataset-action.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-dataset-queryaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-queryaction-syntax.json"></a>

```
{
  "[Filters](#cfn-iotanalytics-dataset-queryaction-filters)" : [ [*Filter*](aws-properties-iotanalytics-dataset-filter.md), ... ],
  "[SqlQuery](#cfn-iotanalytics-dataset-queryaction-sqlquery)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-queryaction-syntax.yaml"></a>

```
[Filters](#cfn-iotanalytics-dataset-queryaction-filters): 
  - [*Filter*](aws-properties-iotanalytics-dataset-filter.md)
[SqlQuery](#cfn-iotanalytics-dataset-queryaction-sqlquery): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-queryaction-properties"></a>

`Filters`  <a name="cfn-iotanalytics-dataset-queryaction-filters"></a>
Pre\-filters applied to message data\.  
 *Required*: No  
 *Type*: List of [Filter](aws-properties-iotanalytics-dataset-filter.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SqlQuery`  <a name="cfn-iotanalytics-dataset-queryaction-sqlquery"></a>
An SQL query string\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-queryaction-seealso"></a>
+ [CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *AWS IoT Analytics User Guide\.*