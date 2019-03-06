# AWS IoT Analytics Pipeline Filter<a name="aws-properties-iotanalytics-pipeline-filter"></a>

<a name="aws-properties-iotanalytics-pipeline-filter-description"></a>The `Filter` property type specifies a filter for a message based on its attributes for an AWS IoT Analytics pipeline\.

<a name="aws-properties-iotanalytics-pipeline-filter-inheritance"></a> `Filter` is a property of the [Activity](aws-properties-iotanalytics-pipeline-activity.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-filter-syntax.json"></a>

```
{
  "[Filter](#cfn-iotanalytics-pipeline-filter-filter)" : String,
  "[Name](#cfn-iotanalytics-pipeline-filter-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-filter-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-filter-syntax.yaml"></a>

```
[Filter](#cfn-iotanalytics-pipeline-filter-filter): String
[Name](#cfn-iotanalytics-pipeline-filter-name): String
[Next](#cfn-iotanalytics-pipeline-filter-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-filter-properties"></a>

`Filter`  <a name="cfn-iotanalytics-pipeline-filter-filter"></a>
Filters a message based on its attributes\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-iotanalytics-pipeline-filter-name"></a>
The name of the 'filter' activity\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Next`  <a name="cfn-iotanalytics-pipeline-filter-next"></a>
The next activity in the pipeline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-pipeline-filter-seealso"></a>
+ [ Filter Activity](https://docs.aws.amazon.com/iotanalytics/latest/userguide/pipeline-activities.html#aws-iot-analytics-pipeline-activities-filter) in the *AWS IoT Analytics User Guide*