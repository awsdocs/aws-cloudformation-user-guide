# AWS::IoTAnalytics::Pipeline<a name="aws-resource-iotanalytics-pipeline"></a>

The AWS::IoTAnalytics::Pipeline resource consumes messages from one or more channels and allows you to process the messages before storing them in a data store\. You must specify both a `channel` and a `datastore` activity and, optionally, as many as 23 additional activities in the `pipelineActivities` array\. For more information, see [ How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*\. 

## Syntax<a name="aws-resource-iotanalytics-pipeline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotanalytics-pipeline-syntax.json"></a>

```
{
  "Type" : "AWS::IoTAnalytics::Pipeline",
  "Properties" : {
      "[PipelineActivities](#cfn-iotanalytics-pipeline-pipelineactivities)" : [ Activity, ... ],
      "[PipelineName](#cfn-iotanalytics-pipeline-pipelinename)" : String,
      "[Tags](#cfn-iotanalytics-pipeline-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotanalytics-pipeline-syntax.yaml"></a>

```
Type: AWS::IoTAnalytics::Pipeline
Properties: 
  [PipelineActivities](#cfn-iotanalytics-pipeline-pipelineactivities): 
    - Activity
  [PipelineName](#cfn-iotanalytics-pipeline-pipelinename): String
  [Tags](#cfn-iotanalytics-pipeline-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotanalytics-pipeline-properties"></a>

`PipelineActivities`  <a name="cfn-iotanalytics-pipeline-pipelineactivities"></a>
A list of "PipelineActivity" objects\. Activities perform transformations on your messages, such as removing, renaming or adding message attributes; filtering messages based on attribute values; invoking your Lambda functions on messages for advanced processing; or performing mathematical transformations to normalize device data\.  
The list can be 2\-25 **PipelineActivity** objects and must contain both a `channel` and a `datastore` activity\. Each entry in the list must contain only one activity, for example:  
 `pipelineActivities = [ { "channel": { ... } }, { "lambda": { ... } }, ... ]`   
*Required*: Yes  
*Type*: List of [Activity](aws-properties-iotanalytics-pipeline-activity.md)  
*Maximum*: `25`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PipelineName`  <a name="cfn-iotanalytics-pipeline-pipelinename"></a>
The name of the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iotanalytics-pipeline-tags"></a>
Metadata which can be used to manage the pipeline\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-iotanalytics-pipeline--examples"></a>



### Simple Pipeline<a name="aws-resource-iotanalytics-pipeline--examples--Simple_Pipeline"></a>

The following example creates a simple pipeline\.

#### JSON<a name="aws-resource-iotanalytics-pipeline--examples--Simple_Pipeline--json"></a>

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

#### YAML<a name="aws-resource-iotanalytics-pipeline--examples--Simple_Pipeline--yaml"></a>

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

### Complex Pipeline<a name="aws-resource-iotanalytics-pipeline--examples--Complex_Pipeline"></a>

The following example creates a complex pipeline\.

#### JSON<a name="aws-resource-iotanalytics-pipeline--examples--Complex_Pipeline--json"></a>

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

#### YAML<a name="aws-resource-iotanalytics-pipeline--examples--Complex_Pipeline--yaml"></a>

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

## See also<a name="aws-resource-iotanalytics-pipeline--seealso"></a>
+  [How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide* 
+  [CreatePipeline](https://docs.aws.amazon.com/iotanalytics/latest/APIReference/API_CreatePipeline.html) in the *AWS IoT Analytics API Reference* 