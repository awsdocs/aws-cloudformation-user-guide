# AWS::IoTAnalytics::Dataset<a name="aws-resource-iotanalytics-dataset"></a>

The AWS::IoTAnalytics::Dataset resource stores data retrieved from a data store by applying a "queryAction" \(an SQL query\) or a "containerAction" \(executing a containerized application\)\. The data set can be populated manually by calling "CreateDatasetContent" or automatically according to a "trigger" you specify\. For more information, see [ How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*\. 

## Syntax<a name="aws-resource-iotanalytics-dataset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotanalytics-dataset-syntax.json"></a>

```
{
  "Type" : "AWS::IoTAnalytics::Dataset",
  "Properties" : {
      "[Actions](#cfn-iotanalytics-dataset-actions)" : [ Action, ... ],
      "[ContentDeliveryRules](#cfn-iotanalytics-dataset-contentdeliveryrules)" : [ DatasetContentDeliveryRule, ... ],
      "[DatasetName](#cfn-iotanalytics-dataset-datasetname)" : String,
      "[RetentionPeriod](#cfn-iotanalytics-dataset-retentionperiod)" : RetentionPeriod,
      "[Tags](#cfn-iotanalytics-dataset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Triggers](#cfn-iotanalytics-dataset-triggers)" : [ Trigger, ... ],
      "[VersioningConfiguration](#cfn-iotanalytics-dataset-versioningconfiguration)" : VersioningConfiguration
    }
}
```

### YAML<a name="aws-resource-iotanalytics-dataset-syntax.yaml"></a>

```
Type: AWS::IoTAnalytics::Dataset
Properties: 
  [Actions](#cfn-iotanalytics-dataset-actions): 
    - Action
  [ContentDeliveryRules](#cfn-iotanalytics-dataset-contentdeliveryrules): 
    - DatasetContentDeliveryRule
  [DatasetName](#cfn-iotanalytics-dataset-datasetname): String
  [RetentionPeriod](#cfn-iotanalytics-dataset-retentionperiod): 
    RetentionPeriod
  [Tags](#cfn-iotanalytics-dataset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Triggers](#cfn-iotanalytics-dataset-triggers): 
    - Trigger
  [VersioningConfiguration](#cfn-iotanalytics-dataset-versioningconfiguration): 
    VersioningConfiguration
```

## Properties<a name="aws-resource-iotanalytics-dataset-properties"></a>

`Actions`  <a name="cfn-iotanalytics-dataset-actions"></a>
The `DatasetAction` objects that automatically create the data set contents\.  
*Required*: Yes  
*Type*: List of [Action](aws-properties-iotanalytics-dataset-action.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentDeliveryRules`  <a name="cfn-iotanalytics-dataset-contentdeliveryrules"></a>
When dataset contents are created they are delivered to destinations specified here\.  
*Required*: No  
*Type*: List of [DatasetContentDeliveryRule](aws-properties-iotanalytics-dataset-datasetcontentdeliveryrule.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatasetName`  <a name="cfn-iotanalytics-dataset-datasetname"></a>
The name of the data set\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RetentionPeriod`  <a name="cfn-iotanalytics-dataset-retentionperiod"></a>
Optional\. How long, in days, message data is kept for the data set\.  
*Required*: No  
*Type*: [RetentionPeriod](aws-properties-iotanalytics-dataset-retentionperiod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotanalytics-dataset-tags"></a>
Metadata which can be used to manage the data set\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Triggers`  <a name="cfn-iotanalytics-dataset-triggers"></a>
The `DatasetTrigger` objects that specify when the data set is automatically updated\.  
*Required*: No  
*Type*: List of [Trigger](aws-properties-iotanalytics-dataset-trigger.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersioningConfiguration`  <a name="cfn-iotanalytics-dataset-versioningconfiguration"></a>
Optional\. How many versions of dataset contents are kept\. If not specified or set to null, only the latest version plus the latest succeeded version \(if they are different\) are kept for the time period specified by the `retentionPeriod` parameter\. For more information, see [Keeping Multiple Versions of AWS IoT Analytics Data Sets](https://docs.aws.amazon.com/iotanalytics/latest/userguide/getting-started.html#aws-iot-analytics-dataset-versions) in the *AWS IoT Analytics User Guide*\.  
*Required*: No  
*Type*: [VersioningConfiguration](aws-properties-iotanalytics-dataset-versioningconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-iotanalytics-dataset--examples"></a>



### Simple SQL Dataset<a name="aws-resource-iotanalytics-dataset--examples--Simple_SQL_Dataset"></a>

The following example creates a simple SQL dataset\.

#### JSON<a name="aws-resource-iotanalytics-dataset--examples--Simple_SQL_Dataset--json"></a>

```
{
    "Description": "Create a simple SQL Dataset",
    "Resources": {
        "Dataset": {
            "Type": "AWS::IoTAnalytics::Dataset",
            "Properties": {
                "DatasetName": "SimpleSQLDataset",
                "Actions": [
                    {
                        "ActionName": "SqlAction",
                        "QueryAction": {
                            "SqlQuery": "select * from Datastore"
                        }
                    }
                ],
                "Triggers": [
                    {
                        "Schedule": {
                            "ScheduleExpression": "cron(0 12 * * ? *)"
                        }
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iotanalytics-dataset--examples--Simple_SQL_Dataset--yaml"></a>

```
---
Description: "Create a simple SQL Dataset"
Resources:
  Dataset:
    Type: "AWS::IoTAnalytics::Dataset"
    Properties:
      DatasetName: "SimpleSQLDataset"
      Actions:
        -
          ActionName: "SqlAction"
          QueryAction:
            SqlQuery: "select * from Datastore"
      Triggers:
        -
          Schedule:
            ScheduleExpression: "cron(0 12 * * ? *)"
```

### Complex SQL Dataset<a name="aws-resource-iotanalytics-dataset--examples--Complex_SQL_Dataset"></a>

The following example creates a complex SQL dataset\.

#### JSON<a name="aws-resource-iotanalytics-dataset--examples--Complex_SQL_Dataset--json"></a>

```
{
    "Description": "Create a complex SQL Dataset",
    "Resources": {
        "Dataset": {
            "Type": "AWS::IoTAnalytics::Dataset",
            "Properties": {
                "DatasetName": "ComplexSQLDataset",
                "Actions": [
                    {
                        "ActionName": "SqlAction",
                        "QueryAction": {
                            "SqlQuery": "select * from Datastore",
                            "Filters": [
                                {
                                    "DeltaTime": {
                                        "OffsetSeconds": 1,
                                        "TimeExpression": "timestamp"
                                    }
                                }
                            ]
                        }
                    }
                ],
                "Triggers": [
                    {
                        "Schedule": {
                            "ScheduleExpression": "cron(0 12 * * ? *)"
                        }
                    }
                ],
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

#### YAML<a name="aws-resource-iotanalytics-dataset--examples--Complex_SQL_Dataset--yaml"></a>

```
---
Description: "Create a complex SQL Dataset"
Resources:
  Dataset:
    Type: "AWS::IoTAnalytics::Dataset"
    Properties:
      DatasetName: "ComplexSQLDataset"
      Actions:
        -
          ActionName: "SqlAction"
          QueryAction:
            SqlQuery: "select * from Datastore"
            Filters:
              -
                DeltaTime:
                  OffsetSeconds: 1
                  TimeExpression: "timestamp"
      Triggers:
        -
          Schedule:
            ScheduleExpression: "cron(0 12 * * ? *)"
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

### Simple Container Dataset<a name="aws-resource-iotanalytics-dataset--examples--Simple_Container_Dataset"></a>

The following example creates a simple Container dataset\.

#### JSON<a name="aws-resource-iotanalytics-dataset--examples--Simple_Container_Dataset--json"></a>

```
{
    "Description": "Create a simple container Dataset",
    "Resources": {
        "ContainerDataset": {
            "Type": "AWS::IoTAnalytics::Dataset",
            "Properties": {
                "DatasetName": "SimpleContainerDataset",
                "Actions": [
                    {
                        "ActionName": "ContainerAction",
                        "ContainerAction": {
                            "Image": "<your_Account_Id>.dkr.ecr.us-east-1.amazonaws.com/sampleimage",
                            "ExecutionRoleArn": "arn:aws:iam::<your_Account_Id>:role/ExecutionRole",
                            "ResourceConfiguration": {
                                "ComputeType": "ACU_1",
                                "VolumeSizeInGB": 10
                            },
                            "Variables": [
                                {
                                    "VariableName": "Variable1",
                                    "StringValue": "StringValue"
                                }
                            ]
                        }
                    }
                ],
                "Triggers": [
                    {
                        "Schedule": {
                            "ScheduleExpression": "cron(0 12 * * ? *)"
                        }
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iotanalytics-dataset--examples--Simple_Container_Dataset--yaml"></a>

```
---
Description: "Create a simple container Dataset"
Resources:
  ContainerDataset:
    Type: "AWS::IoTAnalytics::Dataset"
    Properties:
      DatasetName: "SimpleContainerDataset"
      Actions:
        - ActionName: ContainerAction
          ContainerAction:
            Image: "<your_Account_Id>.dkr.ecr.us-east-1.amazonaws.com/sampleimage" 
            ExecutionRoleArn: "arn:aws:iam::<your_Account_Id>:role/ExecutionRole"
            ResourceConfiguration:
              ComputeType: "ACU_1"
              VolumeSizeInGB: 10
            Variables:
              - VariableName: "Variable1"
                StringValue: StringValue
      Triggers:
        -
          Schedule:
            ScheduleExpression: "cron(0 12 * * ? *)"
```

### Complex Container Dataset<a name="aws-resource-iotanalytics-dataset--examples--Complex_Container_Dataset"></a>

The following example creates a complex Container dataset\.

#### JSON<a name="aws-resource-iotanalytics-dataset--examples--Complex_Container_Dataset--json"></a>

```
{
    "Description": "Create a complex container Dataset",
    "Resources": {
        "TriggeringDataset": {
            "Type": "AWS::IoTAnalytics::Dataset",
            "Properties": {
                "DatasetName": "TriggeringDataset",
                "Actions": [
                    {
                        "ActionName": "SqlAction",
                        "QueryAction": {
                            "SqlQuery": "select * from Datastore"
                        }
                    }
                ]
            }
        },
        "ContainerDataset": {
            "Type": "AWS::IoTAnalytics::Dataset",
            "DependsOn": "TriggeringDataset",
            "Properties": {
                "DatasetName": "ComplexContainerDataset",
                "Actions": [
                    {
                        "ActionName": "ContainerAction",
                        "ContainerAction": {
                            "Image": "<your_Account_Id>.dkr.ecr.us-east-1.amazonaws.com/sampleimage",
                            "ExecutionRoleArn": "arn:aws:iam::<your_Account_Id>:role/ExecutionRole",
                            "ResourceConfiguration": {
                                "ComputeType": "ACU_1",
                                "VolumeSizeInGB": 10
                            },
                            "Variables": [
                                {
                                    "VariableName": "Variable1",
                                    "StringValue": "StringValue"
                                },
                                {
                                    "VariableName": "Variable2",
                                    "DoubleValue": 1
                                },
                                {
                                    "VariableName": "Variable3",
                                    "DatasetContentVersionValue": {
                                        "DatasetName": "BasicDataset"
                                    }
                                },
                                {
                                    "VariableName": "Variable4",
                                    "OutputFileUriValue": {
                                        "FileName": "fileName"
                                    }
                                }
                            ]
                        }
                    }
                ],
                "Triggers": [
                    {
                        "TriggeringDataset": {
                            "DatasetName": "TriggeringDataset"
                        }
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iotanalytics-dataset--examples--Complex_Container_Dataset--yaml"></a>

```
---
Description: "Create a complex container Dataset"
Resources:
  TriggeringDataset:
    Type: "AWS::IoTAnalytics::Dataset"
    Properties:
      DatasetName: "TriggeringDataset"
      Actions:
        -
          ActionName: "SqlAction"
          QueryAction:
            SqlQuery: "select * from Datastore"

  ContainerDataset:
    Type: "AWS::IoTAnalytics::Dataset"
    DependsOn: TriggeringDataset
    Properties:
      DatasetName: "ComplexContainerDataset"
      Actions:
        -
          ActionName: "ContainerAction"
          ContainerAction:
            Image: "<your_Account_Id>.dkr.ecr.us-east-1.amazonaws.com/sampleimage" 
            ExecutionRoleArn: "arn:aws:iam::<your_Account_Id>:role/ExecutionRole"
            ResourceConfiguration:
              ComputeType: "ACU_1"
              VolumeSizeInGB: 10
            Variables:
              -
                VariableName: "Variable1"
                StringValue: "StringValue"
              -
                VariableName: "Variable2"
                DoubleValue: 1
              -
                VariableName: "Variable3"
                DatasetContentVersionValue:
                  DatasetName: "BasicDataset"
              -
                VariableName: "Variable4"
                OutputFileUriValue:
                  FileName: "fileName"
      Triggers:
        -
          TriggeringDataset:
            DatasetName: "TriggeringDataset"
```

## See also<a name="aws-resource-iotanalytics-dataset--seealso"></a>
+  [How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide* 
+  [CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/APIReference/API_CreateDataset.html) in the *AWS IoT Analytics API Reference* 