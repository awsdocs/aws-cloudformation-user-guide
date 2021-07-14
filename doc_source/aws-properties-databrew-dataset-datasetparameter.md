# AWS::DataBrew::Dataset DatasetParameter<a name="aws-properties-databrew-dataset-datasetparameter"></a>

Represents a dataset paramater that defines type and conditions for a parameter in the Amazon S3 path of the dataset\.

## Syntax<a name="aws-properties-databrew-dataset-datasetparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-dataset-datasetparameter-syntax.json"></a>

```
{
  "[CreateColumn](#cfn-databrew-dataset-datasetparameter-createcolumn)" : Boolean,
  "[DatetimeOptions](#cfn-databrew-dataset-datasetparameter-datetimeoptions)" : DatetimeOptions,
  "[Filter](#cfn-databrew-dataset-datasetparameter-filter)" : FilterExpression,
  "[Name](#cfn-databrew-dataset-datasetparameter-name)" : String,
  "[Type](#cfn-databrew-dataset-datasetparameter-type)" : String
}
```

### YAML<a name="aws-properties-databrew-dataset-datasetparameter-syntax.yaml"></a>

```
  [CreateColumn](#cfn-databrew-dataset-datasetparameter-createcolumn): Boolean
  [DatetimeOptions](#cfn-databrew-dataset-datasetparameter-datetimeoptions): 
    DatetimeOptions
  [Filter](#cfn-databrew-dataset-datasetparameter-filter): 
    FilterExpression
  [Name](#cfn-databrew-dataset-datasetparameter-name): String
  [Type](#cfn-databrew-dataset-datasetparameter-type): String
```

## Properties<a name="aws-properties-databrew-dataset-datasetparameter-properties"></a>

`CreateColumn`  <a name="cfn-databrew-dataset-datasetparameter-createcolumn"></a>
Optional boolean value that defines whether the captured value of this parameter should be loaded as an additional column in the dataset\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatetimeOptions`  <a name="cfn-databrew-dataset-datasetparameter-datetimeoptions"></a>
Additional parameter options such as a format and a timezone\. Required for datetime parameters\.  
*Required*: No  
*Type*: [DatetimeOptions](aws-properties-databrew-dataset-datetimeoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filter`  <a name="cfn-databrew-dataset-datasetparameter-filter"></a>
The optional filter expression structure to apply additional matching criteria to the parameter\.  
*Required*: No  
*Type*: [FilterExpression](aws-properties-databrew-dataset-filterexpression.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-databrew-dataset-datasetparameter-name"></a>
The name of the parameter that is used in the dataset's Amazon S3 path\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-databrew-dataset-datasetparameter-type"></a>
The type of the dataset parameter, can be one of a 'String', 'Number' or 'Datetime'\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)