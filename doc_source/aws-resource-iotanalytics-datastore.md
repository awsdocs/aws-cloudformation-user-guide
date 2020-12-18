# AWS::IoTAnalytics::Datastore<a name="aws-resource-iotanalytics-datastore"></a>

AWS::IoTAnalytics::Datastore resource is a repository for messages\. For more information, see [ How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*\. 

## Syntax<a name="aws-resource-iotanalytics-datastore-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotanalytics-datastore-syntax.json"></a>

```
{
  "Type" : "AWS::IoTAnalytics::Datastore",
  "Properties" : {
      "[DatastoreName](#cfn-iotanalytics-datastore-datastorename)" : String,
      "[DatastoreStorage](#cfn-iotanalytics-datastore-datastorestorage)" : DatastoreStorage,
      "[RetentionPeriod](#cfn-iotanalytics-datastore-retentionperiod)" : RetentionPeriod,
      "[Tags](#cfn-iotanalytics-datastore-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotanalytics-datastore-syntax.yaml"></a>

```
Type: AWS::IoTAnalytics::Datastore
Properties: 
  [DatastoreName](#cfn-iotanalytics-datastore-datastorename): String
  [DatastoreStorage](#cfn-iotanalytics-datastore-datastorestorage): 
    DatastoreStorage
  [RetentionPeriod](#cfn-iotanalytics-datastore-retentionperiod): 
    RetentionPeriod
  [Tags](#cfn-iotanalytics-datastore-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotanalytics-datastore-properties"></a>

`DatastoreName`  <a name="cfn-iotanalytics-datastore-datastorename"></a>
The name of the data store\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatastoreStorage`  <a name="cfn-iotanalytics-datastore-datastorestorage"></a>
Where data store data is stored\.  
*Required*: No  
*Type*: [DatastoreStorage](aws-properties-iotanalytics-datastore-datastorestorage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetentionPeriod`  <a name="cfn-iotanalytics-datastore-retentionperiod"></a>
How long, in days, message data is kept for the data store\. When `customerManagedS3` storage is selected, this parameter is ignored\.  
*Required*: No  
*Type*: [RetentionPeriod](aws-properties-iotanalytics-datastore-retentionperiod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotanalytics-datastore-tags"></a>
Metadata which can be used to manage the data store\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-iotanalytics-datastore--examples"></a>



### Simple Datastore<a name="aws-resource-iotanalytics-datastore--examples--Simple_Datastore"></a>

The following example creates a simple datastore\.

#### JSON<a name="aws-resource-iotanalytics-datastore--examples--Simple_Datastore--json"></a>

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

#### YAML<a name="aws-resource-iotanalytics-datastore--examples--Simple_Datastore--yaml"></a>

```
---
Description: "Create a simple Datastore"
Resources:
  Datastore:
    Type: "AWS::IoTAnalytics::Datastore"
    Properties:
      DatastoreName: "SimpleDatastore"
```

### Complex Datastore<a name="aws-resource-iotanalytics-datastore--examples--Complex_Datastore"></a>

The following example creates a complex datastore\.

#### JSON<a name="aws-resource-iotanalytics-datastore--examples--Complex_Datastore--json"></a>

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

#### YAML<a name="aws-resource-iotanalytics-datastore--examples--Complex_Datastore--yaml"></a>

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

## See also<a name="aws-resource-iotanalytics-datastore--seealso"></a>
+  [How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide* 
+  [CreateDatastore](https://docs.aws.amazon.com/iotanalytics/latest/APIReference/API_CreateDatastore.html) in the *AWS IoT Analytics API Reference* 