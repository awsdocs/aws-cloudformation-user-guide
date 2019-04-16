# AWS::IoTAnalytics::Pipeline<a name="aws-resource-iotanalytics-pipeline"></a>

The `AWS::IoTAnalytics::Pipeline` resource consumes messages from one or more channels and processes the messages before storing them in a data store\. For more information, see [ How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*\. 

## Syntax<a name="aws-resource-iotanalytics-pipeline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotanalytics-pipeline-syntax.json"></a>

```
{
  "Type" : "AWS::IoTAnalytics::Pipeline",
  "Properties" : {
    "[PipelineActivities](#cfn-iotanalytics-pipeline-pipelineactivities)" : [ [*Activity*](aws-properties-iotanalytics-pipeline-activity.md), ... ],
    "[PipelineName](#cfn-iotanalytics-pipeline-pipelinename)" : String,
    "[Tags](#cfn-iotanalytics-pipeline-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ]
  }
}
```

### YAML<a name="aws-resource-iotanalytics-pipeline-syntax.yaml"></a>

```
Type: "AWS::IoTAnalytics::Pipeline"
Properties:
  [PipelineActivities](#cfn-iotanalytics-pipeline-pipelineactivities): 
    - [*Activity*](aws-properties-iotanalytics-pipeline-activity.md)
  [PipelineName](#cfn-iotanalytics-pipeline-pipelinename): String
  [Tags](#cfn-iotanalytics-pipeline-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-resource-iotanalytics-pipeline-properties"></a>

`PipelineActivities`  <a name="cfn-iotanalytics-pipeline-pipelineactivities"></a>
A list of pipeline activities which perform transformations on your messages, such as removing, renaming, or adding message attributes; filtering messages based on attribute value; invoking your Lambda functions on messages for advanced processing; or performing mathematical transformation to normalize device data\.  
 *Required*: Yes  
 *Type*: List of [Activity](aws-properties-iotanalytics-pipeline-activity.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PipelineName`  <a name="cfn-iotanalytics-pipeline-pipelinename"></a>
The name of the pipeline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-iotanalytics-pipeline-tags"></a>
Metadata which can be used to manage the pipeline\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="aws-resource-iotanalytics-pipeline-examples"></a>

### Simple Pipeline<a name="aws-resource-iotanalytics-pipeline-example1"></a>

The following example creates a simple pipeline\.

#### JSON<a name="aws-resource-iotanalytics-pipeline-example1.json"></a>

```
{
    "Description": "Create a simple Pipeline",
    "Resources": {
        "Pipeline": {
            "Type": "AWS::IoTAnalytics::Pipeline",
            "Properties": {
                "PipelineName": "SimplePipeline",
                "PipelineActivities": [
                    {
                        "Channel": {
                            "Name": "ChannelActivity",
                            "ChannelName": "SimpleChannel",
                            "Next": "DatastoreActivity"
                        },
                        "Datastore": {
                            "Name": "DatastoreActivity",
                            "DatastoreName": "SimpleDatastore"
                        }
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iotanalytics-pipeline-example1.yaml"></a>

```
---
Description: "Create a simple Pipeline"
Resources:
  Pipeline:
    Type: "AWS::IoTAnalytics::Pipeline"
    Properties:
      PipelineName: "SimplePipeline"
      PipelineActivities:
        -
          Channel:
            Name: "ChannelActivity"
            ChannelName: "SimpleChannel"
            Next: "DatastoreActivity"
          Datastore:
            Name: "DatastoreActivity"
            DatastoreName: "SimpleDatastore"
```

### Complex Pipeline<a name="aws-resource-iotanalytics-pipeline-example2"></a>

The following example creates a complex pipeline\.

#### JSON<a name="aws-resource-iotanalytics-pipeline-example2.json"></a>

```
{
    "Description": "Create a complex Pipeline",
    "Resources": {
        "Pipeline": {
            "Type": "AWS::IoTAnalytics::Pipeline",
            "Properties": {
                "PipelineName": "ComplexPipeline",
                "PipelineActivities": [
                    {
                        "Channel": {
                            "Name": "ChannelActivity",
                            "ChannelName": "Channel",
                            "Next": "LambdaActivity"
                        },
                        "Lambda": {
                            "Name": "LambdaActivity",
                            "LambdaName": "Lambda",
                            "BatchSize": 1,
                            "Next": "AddAttributesActivity"
                        },
                        "AddAttributes": {
                            "Name": "AddAttributesActivity",
                            "Attributes": {
                                "key1": "attribute1",
                                "key2": "attribute2"
                            },
                            "Next": "RemoveAttributesActivity"
                        },
                        "RemoveAttributes": {
                            "Name": "RemoveAttributesActivity",
                            "Attributes": [
                                "attribute1",
                                "attribute2"
                            ],
                            "Next": "SelectAttributesActivity"
                        },
                        "SelectAttributes": {
                            "Name": "SelectAttributesActivity",
                            "Attributes": [
                                "attribute1",
                                "attribute2"
                            ],
                            "Next": "FilterActivity"
                        },
                        "Filter": {
                            "Name": "FilterActivity",
                            "Filter": "attribute1 > 40 AND attribute2 < 20",
                            "Next": "MathActivity"
                        },
                        "Math": {
                            "Name": "MathActivity",
                            "Attribute": "attribute",
                            "Math": "attribute - 10",
                            "Next": "DeviceRegistryEnrichActivity"
                        },
                        "DeviceRegistryEnrich": {
                            "Name": "DeviceRegistryEnrichActivity",
                            "Attribute": "attribute",
                            "ThingName": "thingName",
                            "RoleArn": "arn:aws:iam::<your_Account_Id>:role/Enrich",
                            "Next": "DeviceShadowEnrichActivity"
                        },
                        "DeviceShadowEnrich": {
                            "Name": "DeviceShadowEnrichActivity",
                            "Attribute": "attribute",
                            "ThingName": "thingName",
                            "RoleArn": "arn:aws:iam::<your_Account_Id>:role/Enrich",
                            "Next": "DatastoreActivity"
                        },
                        "Datastore": {
                            "Name": "DatastoreActivity",
                            "DatastoreName": "Datastore"
                        }
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iotanalytics-pipeline-example2.yaml"></a>

```
---
Description: "Create a complex Pipeline"
Resources:
  Pipeline:
    Type: "AWS::IoTAnalytics::Pipeline"
    Properties:
      PipelineName: "ComplexPipeline"
      PipelineActivities:
        -
          Channel:
            Name: "ChannelActivity"
            ChannelName: "Channel"
            Next: "LambdaActivity"
          Lambda:
            Name: "LambdaActivity"
            LambdaName: "Lambda"
            BatchSize: 1
            Next: "AddAttributesActivity"
          AddAttributes:
            Name: "AddAttributesActivity"
            Attributes:
              key1: "attribute1"
              key2: "attribute2"
            Next: "RemoveAttributesActivity"
          RemoveAttributes:
            Name: "RemoveAttributesActivity"
            Attributes:
              -
                "attribute1"
              -
                "attribute2"
            Next: "SelectAttributesActivity"
          SelectAttributes:
            Name: "SelectAttributesActivity"
            Attributes:
              -
                "attribute1"
              -
                "attribute2"
            Next: "FilterActivity"
          Filter:
            Name: "FilterActivity"
            Filter: "attribute1 > 40 AND attribute2 < 20"
            Next: "MathActivity"
          Math:
            Name: "MathActivity"
            Attribute: "attribute"
            Math: "attribute - 10"
            Next: "DeviceRegistryEnrichActivity"
          DeviceRegistryEnrich:
            Name: "DeviceRegistryEnrichActivity"
            Attribute: "attribute"
            ThingName: "thingName"
            RoleArn: "arn:aws:iam::<your_Account_Id>:role/Enrich"
            Next: "DeviceShadowEnrichActivity"
          DeviceShadowEnrich:
            Name: "DeviceShadowEnrichActivity"
            Attribute: "attribute"
            ThingName: "thingName"
            RoleArn: "arn:aws:iam::<your_Account_Id>:role/Enrich"
            Next: "DatastoreActivity"
          Datastore:
            Name: "DatastoreActivity"
            DatastoreName: "Datastore"
```

## See Also<a name="aws-resource-iotanalytics-pipeline-seealso"></a>
+ [ How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*