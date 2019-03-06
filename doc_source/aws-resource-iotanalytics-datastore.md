# AWS::IoTAnalytics::Datastore<a name="aws-resource-iotanalytics-datastore"></a>

The `AWS::IoTAnalytics::Datastore` resource is a repository for messages\. For more information, see [ How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*\. 

## Syntax<a name="aws-resource-iotanalytics-datastore-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotanalytics-datastore-syntax.json"></a>

```
{
  "Type" : "AWS::IoTAnalytics::Datastore",
  "Properties" : {
    "[DatastoreName](#cfn-iotanalytics-datastore-datastorename)" : String,
    "[RetentionPeriod](#cfn-iotanalytics-datastore-retentionperiod)" : [*RetentionPeriod*](aws-properties-iotanalytics-datastore-retentionperiod.md),
    "[Tags](#cfn-iotanalytics-datastore-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ]
  }
}
```

### YAML<a name="aws-resource-iotanalytics-datastore-syntax.yaml"></a>

```
Type: "AWS::IoTAnalytics::Datastore"
Properties:
  [DatastoreName](#cfn-iotanalytics-datastore-datastorename): String
  [RetentionPeriod](#cfn-iotanalytics-datastore-retentionperiod): 
    [*RetentionPeriod*](aws-properties-iotanalytics-datastore-retentionperiod.md)
  [Tags](#cfn-iotanalytics-datastore-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-resource-iotanalytics-datastore-properties"></a>

`DatastoreName`  <a name="cfn-iotanalytics-datastore-datastorename"></a>
The name of the data store\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RetentionPeriod`  <a name="cfn-iotanalytics-datastore-retentionperiod"></a>
How long, in days, message data is kept for the data store\.  
 *Required*: No  
 *Type*: [RetentionPeriod](aws-properties-iotanalytics-datastore-retentionperiod.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-iotanalytics-datastore-tags"></a>
Metadata which can be used to manage the data store\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="aws-resource-iotanalytics-datastore-examples"></a>

### Simple Datastore<a name="aws-resource-iotanalytics-datastore-example1"></a>

The following example creates a simple datastore\.

#### JSON<a name="aws-resource-iotanalytics-datastore-example1.json"></a>

```
{
    "Description": "Create a simple Datastore",
    "Resources": {
        "Datastore": {
            "Type": "AWS::IoTAnalytics::Datastore",
            "Properties": {
                "DatastoreName": "SimpleDatastore"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iotanalytics-datastore-example1.yaml"></a>

```
---
Description: "Create a simple Datastore"
Resources:
  Datastore:
    Type: "AWS::IoTAnalytics::Datastore"
    Properties:
      DatastoreName: "SimpleDatastore"
```

### Complex Datastore<a name="aws-resource-iotanalytics-datastore-example2"></a>

The following example creates a complex datastore\.

#### JSON<a name="aws-resource-iotanalytics-datastore-example2.json"></a>

```
{
    "Description": "Create a complex Datastore",
    "Resources": {
        "Datastore": {
            "Type": "AWS::IoTAnalytics::Datastore",
            "Properties": {
                "DatastoreName": "ComplexDatastore",
                "RetentionPeriod": {
                    "Unlimited": false,
                    "NumberOfDays": 10
                },
                "Tags": [
                    {
                        "Key": "keyname1",
                        "Value": "value1"
                    },
                    {
                        "Key": "keyname2",
                        "Value": "value2"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iotanalytics-datastore-example2.yaml"></a>

```
---
Description: "Create a complex Datastore"
Resources:
  Datastore:
    Type: "AWS::IoTAnalytics::Datastore"
    Properties:
      DatastoreName: "ComplexDatastore"
      RetentionPeriod:
        Unlimited: false
        NumberOfDays: 10
      Tags:
        -
          Key: "keyname1"
          Value: "value1"
        -
          Key: "keyname2"
          Value: "value2"
```

## See Also<a name="aws-resource-iotanalytics-datastore-seealso"></a>
+ [ How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*