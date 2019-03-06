# AWS IoT Analytics Dataset Filter<a name="aws-properties-iotanalytics-dataset-filter"></a>

<a name="aws-properties-iotanalytics-dataset-filter-description"></a>The `Filter` property type specifies pre\-filters which are applied to message data for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-filter-inheritance"></a> `Filter` is a property of the [QueryAction](aws-properties-iotanalytics-dataset-queryaction.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-dataset-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-filter-syntax.json"></a>

```
{
  "[DeltaTime](#cfn-iotanalytics-dataset-filter-deltatime)" : [*DeltaTime*](aws-properties-iotanalytics-dataset-deltatime.md)
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-filter-syntax.yaml"></a>

```
[DeltaTime](#cfn-iotanalytics-dataset-filter-deltatime): 
  [*DeltaTime*](aws-properties-iotanalytics-dataset-deltatime.md)
```

## Properties<a name="aws-properties-iotanalytics-dataset-filter-properties"></a>

`DeltaTime`  <a name="cfn-iotanalytics-dataset-filter-deltatime"></a>
Used to limit data to that which has arrived since the last execution of the action\.  
 *Required*: No  
 *Type*: [*DeltaTime*](aws-properties-iotanalytics-dataset-deltatime.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-filter-seealso"></a>
+ [ CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *AWS IoT Analytics User Guide*