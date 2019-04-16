# AWS::IoTAnalytics::Dataset<a name="aws-resource-iotanalytics-dataset"></a>

The `AWS::IoTAnalytics::Dataset` resource retrieves data from a data store\. For more information, see [ How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*\. 

## Syntax<a name="aws-resource-iotanalytics-dataset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotanalytics-dataset-syntax.json"></a>

```
{
  "Type" : "AWS::IoTAnalytics::Dataset",
  "Properties" : {
    "[Actions](#cfn-iotanalytics-dataset-actions)" : [ [*Action*](aws-properties-iotanalytics-dataset-action.md), ... ],
    "[DatasetName](#cfn-iotanalytics-dataset-datasetname)" : String,
    "[RetentionPeriod](#cfn-iotanalytics-dataset-retentionperiod)" : [*RetentionPeriod*](aws-properties-iotanalytics-dataset-retentionperiod.md),
    "[Tags](#cfn-iotanalytics-dataset-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ],
    "[Triggers](#cfn-iotanalytics-dataset-triggers)" : [ [*Trigger*](aws-properties-iotanalytics-dataset-trigger.md), ... ]
  }
}
```

### YAML<a name="aws-resource-iotanalytics-dataset-syntax.yaml"></a>

```
Type: "AWS::IoTAnalytics::Dataset"
Properties:
  [Actions](#cfn-iotanalytics-dataset-actions): 
    - [*Action*](aws-properties-iotanalytics-dataset-action.md)
  [DatasetName](#cfn-iotanalytics-dataset-datasetname): String
  [RetentionPeriod](#cfn-iotanalytics-dataset-retentionperiod): 
    [*RetentionPeriod*](aws-properties-iotanalytics-dataset-retentionperiod.md)
  [Tags](#cfn-iotanalytics-dataset-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
  [Triggers](#cfn-iotanalytics-dataset-triggers): 
    - [*Trigger*](aws-properties-iotanalytics-dataset-trigger.md)
```

## Properties<a name="aws-resource-iotanalytics-dataset-properties"></a>

`Actions`  <a name="cfn-iotanalytics-dataset-actions"></a>
A list of actions that create the data set contents\.  
 *Required*: Yes  
 *Type*: List of [Action](aws-properties-iotanalytics-dataset-action.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DatasetName`  <a name="cfn-iotanalytics-dataset-datasetname"></a>
The name of the data set\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RetentionPeriod`  <a name="cfn-iotanalytics-dataset-retentionperiod"></a>
How long, in days, message data is kept for the data set\.  
 *Required*: No  
 *Type*: [RetentionPeriod](aws-properties-iotanalytics-dataset-retentionperiod.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-iotanalytics-dataset-tags"></a>
Metadata which can be used to manage the data set\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Triggers`  <a name="cfn-iotanalytics-dataset-triggers"></a>
A list of triggers\. A trigger causes data set contents to be populated at a specified time interval or when another data set's contents are created\. The list of triggers can be empty or contain up to five objects\.  
 *Required*: No  
 *Type*: List of [Trigger](aws-properties-iotanalytics-dataset-trigger.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="aws-resource-iotanalytics-dataset-examples"></a>

### Simple SQL Dataset<a name="aws-resource-iotanalytics-dataset-example1"></a>

The following example creates a simple SQL dataset\.

#### JSON<a name="aws-resource-iotanalytics-dataset-example1.json"></a>

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

#### YAML<a name="aws-resource-iotanalytics-dataset-example1.yaml"></a>

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

### Complex SQL Dataset<a name="aws-resource-iotanalytics-dataset-example2"></a>

The following example creates a complex SQL dataset\.

#### JSON<a name="aws-resource-iotanalytics-dataset-example2.json"></a>

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

#### YAML<a name="aws-resource-iotanalytics-dataset-example2.yaml"></a>

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

### Simple Container Dataset<a name="aws-resource-iotanalytics-dataset-example3"></a>

The following example creates a simple container dataset\.

#### JSON<a name="aws-resource-iotanalytics-dataset-example3.json"></a>

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

#### YAML<a name="aws-resource-iotanalytics-dataset-example3.yaml"></a>

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

### Complex Container Dataset<a name="aws-resource-iotanalytics-dataset-example4"></a>

The following example creates a complex container dataset\.

#### JSON<a name="aws-resource-iotanalytics-dataset-example4.json"></a>

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

#### YAML<a name="aws-resource-iotanalytics-dataset-example4.yaml"></a>

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

## See Also<a name="aws-resource-iotanalytics-dataset-seealso"></a>
+ [ How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*