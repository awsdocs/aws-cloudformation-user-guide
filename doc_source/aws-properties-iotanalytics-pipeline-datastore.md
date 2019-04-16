# AWS IoT Analytics Pipeline Datastore<a name="aws-properties-iotanalytics-pipeline-datastore"></a>

<a name="aws-properties-iotanalytics-pipeline-datastore-description"></a>The `Datastore` property type specifies where to store the processed message data for an AWS IoT Analytics pipeline\.

<a name="aws-properties-iotanalytics-pipeline-datastore-inheritance"></a> `Datastore` is a property of the [Activity](aws-properties-iotanalytics-pipeline-activity.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-datastore-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-datastore-syntax.json"></a>

```
{
  "[DatastoreName](#cfn-iotanalytics-pipeline-datastore-datastorename)" : String,
  "[Name](#cfn-iotanalytics-pipeline-datastore-name)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-datastore-syntax.yaml"></a>

```
[DatastoreName](#cfn-iotanalytics-pipeline-datastore-datastorename): String
[Name](#cfn-iotanalytics-pipeline-datastore-name): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-datastore-properties"></a>

`DatastoreName`  <a name="cfn-iotanalytics-pipeline-datastore-datastorename"></a>
The name of the data store where processed messages are stored\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-iotanalytics-pipeline-datastore-name"></a>
The name of the 'datastore' activity\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-pipeline-datastore-seealso"></a>
+ [CreatePipeline](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createpipeline) in the *IoT Analytics User Guide*