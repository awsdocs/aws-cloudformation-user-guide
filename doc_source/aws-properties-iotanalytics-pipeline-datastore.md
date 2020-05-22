# AWS::IoTAnalytics::Pipeline Datastore<a name="aws-properties-iotanalytics-pipeline-datastore"></a>

The datastore activity that specifies where to store the processed data\.

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
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotanalytics-pipeline-datastore-name"></a>
The name of the datastore activity\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)