# AWS::DataPipeline::Pipeline<a name="aws-resource-datapipeline-pipeline"></a>

The AWS::DataPipeline::Pipeline resource specifies a data pipeline that you can use to automate the movement and transformation of data\. In each pipeline, you define pipeline objects, such as activities, schedules, data nodes, and resources\. For information about pipeline objects and components that you can use, see [Pipeline Object Reference](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-pipeline-objects.html) in the *AWS Data Pipeline Developer Guide*\.

The `AWS::DataPipeline::Pipeline` resource adds tasks, schedules, and preconditions to the specified pipeline\. You can use `PutPipelineDefinition` to populate a new pipeline\.

 `PutPipelineDefinition` also validates the configuration as it adds it to the pipeline\. Changes to the pipeline are saved unless one of the following validation errors exist in the pipeline\. 
+ An object is missing a name or identifier field\.
+ A string or reference field is empty\.
+ The number of objects in the pipeline exceeds the allowed maximum number of objects\.
+ The pipeline is in a FINISHED state\.

 Pipeline object definitions are passed to the [PutPipelineDefinition](https://docs.aws.amazon.com/datapipeline/latest/APIReference/API_PutPipelineDefinition.html) action and returned by the [GetPipelineDefinition](https://docs.aws.amazon.com/datapipeline/latest/APIReference/API_GetPipelineDefinition.html) action\. 

## Syntax<a name="aws-resource-datapipeline-pipeline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datapipeline-pipeline-syntax.json"></a>

```
{
  "Type" : "AWS::DataPipeline::Pipeline",
  "Properties" : {
      "[Activate](#cfn-datapipeline-pipeline-activate)" : Boolean,
      "[Description](#cfn-datapipeline-pipeline-description)" : String,
      "[Name](#cfn-datapipeline-pipeline-name)" : String,
      "[ParameterObjects](#cfn-datapipeline-pipeline-parameterobjects)" : [ ParameterObject, ... ],
      "[ParameterValues](#cfn-datapipeline-pipeline-parametervalues)" : [ ParameterValue, ... ],
      "[PipelineObjects](#cfn-datapipeline-pipeline-pipelineobjects)" : [ PipelineObject, ... ],
      "[PipelineTags](#cfn-datapipeline-pipeline-pipelinetags)" : [ PipelineTag, ... ]
    }
}
```

### YAML<a name="aws-resource-datapipeline-pipeline-syntax.yaml"></a>

```
Type: AWS::DataPipeline::Pipeline
Properties: 
  [Activate](#cfn-datapipeline-pipeline-activate): Boolean
  [Description](#cfn-datapipeline-pipeline-description): String
  [Name](#cfn-datapipeline-pipeline-name): String
  [ParameterObjects](#cfn-datapipeline-pipeline-parameterobjects): 
    - ParameterObject
  [ParameterValues](#cfn-datapipeline-pipeline-parametervalues): 
    - ParameterValue
  [PipelineObjects](#cfn-datapipeline-pipeline-pipelineobjects): 
    - PipelineObject
  [PipelineTags](#cfn-datapipeline-pipeline-pipelinetags): 
    - PipelineTag
```

## Properties<a name="aws-resource-datapipeline-pipeline-properties"></a>

`Activate`  <a name="cfn-datapipeline-pipeline-activate"></a>
Indicates whether to validate and start the pipeline or stop an active pipeline\. By default, the value is set to `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-datapipeline-pipeline-description"></a>
A description of the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-datapipeline-pipeline-name"></a>
The name of the pipeline\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ParameterObjects`  <a name="cfn-datapipeline-pipeline-parameterobjects"></a>
The parameter objects used with the pipeline\.  
*Required*: Yes  
*Type*: List of [ParameterObject](aws-properties-datapipeline-pipeline-parameterobjects.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterValues`  <a name="cfn-datapipeline-pipeline-parametervalues"></a>
The parameter values used with the pipeline\.  
*Required*: No  
*Type*: List of [ParameterValue](aws-properties-datapipeline-pipeline-parametervalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PipelineObjects`  <a name="cfn-datapipeline-pipeline-pipelineobjects"></a>
The objects that define the pipeline\. These objects overwrite the existing pipeline definition\. Not all objects, fields, and values can be updated\. For information about restrictions, see [Editing Your Pipeline](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-manage-pipeline-modify-console.html) in the *AWS Data Pipeline Developer Guide*\.  
*Required*: No  
*Type*: List of [PipelineObject](aws-properties-datapipeline-pipeline-pipelineobjects.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PipelineTags`  <a name="cfn-datapipeline-pipeline-pipelinetags"></a>
A list of arbitrary tags \(key\-value pairs\) to associate with the pipeline, which you can use to control permissions\. For more information, see [Controlling Access to Pipelines and Resources](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-control-access.html) in the *AWS Data Pipeline Developer Guide*\.  
*Required*: No  
*Type*: List of [PipelineTag](aws-properties-datapipeline-pipeline-pipelinetags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datapipeline-pipeline-return-values"></a>

### Ref<a name="aws-resource-datapipeline-pipeline-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the pipeline ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-datapipeline-pipeline--examples"></a>

The following data pipeline backs up data from an Amazon DynamoDB table to an Amazon S3 bucket\. The pipeline uses the `HiveCopyActivity` activity to copy the data, and runs it once a day\. The [roles](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-iam-roles.html) for the pipeline and the pipeline resource are declared elsewhere in the same template\.

### <a name="aws-resource-datapipeline-pipeline--examples--"></a>

#### JSON<a name="aws-resource-datapipeline-pipeline--examples----json"></a>

```
"DynamoDBInputS3OutputHive": {
  "Type": "AWS::DataPipeline::Pipeline",
  "Properties": {
    "Name": "DynamoDBInputS3OutputHive",
    "Description": "Pipeline to backup DynamoDB data to S3",
    "Activate": "true",
    "ParameterObjects": [
      {
        "Id": "myDDBReadThroughputRatio",
        "Attributes": [
          {
            "Key": "description",
            "StringValue": "DynamoDB read throughput ratio"
          },
          {
            "Key": "type",
            "StringValue": "Double"
          },
          {
            "Key": "default",
            "StringValue": "0.2"
          }
        ]
      },
      {
        "Id": "myOutputS3Loc",
        "Attributes": [
          {
            "Key": "description",
            "StringValue": "S3 output bucket"
          },
          {
            "Key": "type",
            "StringValue": "AWS::S3::ObjectKey"
          },
          {
            "Key": "default",
            "StringValue": { "Fn::Join" : [ "", [ "s3://", { "Ref": "S3OutputLoc" } ] ] }
          }
        ]
      },
      {
        "Id": "myDDBTableName",
        "Attributes": [
          {
            "Key": "description",
            "StringValue": "DynamoDB Table Name "
          },
          {
            "Key": "type",
            "StringValue": "String"
          }
        ]
      }
    ],
    "ParameterValues": [
      {
        "Id": "myDDBTableName",
        "StringValue": { "Ref": "TableName" }
      }
    ],
    "PipelineObjects": [
      {
        "Id": "S3BackupLocation",
        "Name": "Copy data to this S3 location",
        "Fields": [
          {
            "Key": "type",
            "StringValue": "S3DataNode"
          },
          {
            "Key": "dataFormat",
            "RefValue": "DDBExportFormat"
          },
          {
            "Key": "directoryPath",
            "StringValue": "#{myOutputS3Loc}/#{format(@scheduledStartTime, 'YYYY-MM-dd-HH-mm-ss')}"
          }
        ]
      },
      {
        "Id": "DDBSourceTable",
        "Name": "DDBSourceTable",
        "Fields": [
          {
            "Key": "tableName",
            "StringValue": "#{myDDBTableName}"
          },
          {
            "Key": "type",
            "StringValue": "DynamoDBDataNode"
          },
          {
            "Key": "dataFormat",
            "RefValue": "DDBExportFormat"
          },
          {
            "Key": "readThroughputPercent",
            "StringValue": "#{myDDBReadThroughputRatio}"
          }
        ]
      },
      {
        "Id": "DDBExportFormat",
        "Name": "DDBExportFormat",
        "Fields": [
          {
            "Key": "type",
            "StringValue": "DynamoDBExportDataFormat"
          }
        ]
      },
      {
        "Id": "TableBackupActivity",
        "Name": "TableBackupActivity",
        "Fields": [
          {
            "Key": "resizeClusterBeforeRunning",
            "StringValue": "true"
          },
          {
            "Key": "type",
            "StringValue": "HiveCopyActivity"
          },
          {
            "Key": "input",
            "RefValue": "DDBSourceTable"
          },
          {
            "Key": "runsOn",
            "RefValue": "EmrClusterForBackup"
          },
          {
            "Key": "output",
            "RefValue": "S3BackupLocation"
          }
        ]
      },
      {
        "Id": "DefaultSchedule",
        "Name": "RunOnce",
        "Fields": [
          {
            "Key": "occurrences",
            "StringValue": "1"
          },
          {
            "Key": "startAt",
            "StringValue": "FIRST_ACTIVATION_DATE_TIME"
          },
          {
            "Key": "type",
            "StringValue": "Schedule"
          },
          {
            "Key": "period",
            "StringValue": "1 Day"
          }
        ]
      },
      {
        "Id": "Default",
        "Name": "Default",
        "Fields": [
          {
            "Key": "type",
            "StringValue": "Default"
          },
          {
            "Key": "scheduleType",
            "StringValue": "cron"
          },
          {
            "Key": "failureAndRerunMode",
            "StringValue": "CASCADE"
          },
          {
            "Key": "role",
            "StringValue": "DataPipelineDefaultRole"
          },
          {
            "Key": "resourceRole",
            "StringValue": "DataPipelineDefaultResourceRole"
          },
          {
            "Key": "schedule",
            "RefValue": "DefaultSchedule"
          }
        ]
      },
      {
        "Id": "EmrClusterForBackup",
        "Name": "EmrClusterForBackup",
        "Fields": [
          {
            "Key": "terminateAfter",
            "StringValue": "2 Hours"
          },
          {
            "Key": "amiVersion",
            "StringValue": "3.3.2"
          },
          {
            "Key": "masterInstanceType",
            "StringValue": "m1.medium"
          },
          {
            "Key": "coreInstanceType",
            "StringValue": "m1.medium"
          },
          {
            "Key": "coreInstanceCount",
            "StringValue": "1"
          },
          {
            "Key": "type",
            "StringValue": "EmrCluster"
          }
        ]
      }
    ]
  }
}
```

### <a name="aws-resource-datapipeline-pipeline--examples--"></a>

#### YAML<a name="aws-resource-datapipeline-pipeline--examples----yaml"></a>

```
DynamoDBInputS3OutputHive: 
  Type: AWS::DataPipeline::Pipeline
  Properties: 
    Name: DynamoDBInputS3OutputHive
    Description: "Pipeline to backup DynamoDB data to S3"
    Activate: true
    ParameterObjects: 
      - 
        Id: "myDDBReadThroughputRatio"
        Attributes: 
          - 
            Key: "description"
            StringValue: "DynamoDB read throughput ratio"
          - 
            Key: "type"
            StringValue: "Double"
          - 
            Key: "default"
            StringValue: "0.2"
      - 
        Id: "myOutputS3Loc"
        Attributes: 
          - 
            Key: "description"
            StringValue: "S3 output bucket"
          - 
            Key: "type"
            StringValue: "AWS::S3::ObjectKey"
          - 
            Key: "default"
            StringValue: 
              Fn::Join: 
                - ""
                - 
                  - "s3://"
                  - 
                    Ref: "S3OutputLoc"
      - 
        Id: "myDDBTableName"
        Attributes: 
          - 
            Key: "description"
            StringValue: "DynamoDB Table Name "
          - 
            Key: "type"
            StringValue: "String"
    ParameterValues: 
      - 
        Id: "myDDBTableName"
        StringValue: 
          Ref: "TableName"
    PipelineObjects: 
      - 
        Id: "S3BackupLocation"
        Name: "Copy data to this S3 location"
        Fields: 
          - 
            Key: "type"
            StringValue: "S3DataNode"
          - 
            Key: "dataFormat"
            RefValue: "DDBExportFormat"
          - 
            Key: "directoryPath"
            StringValue: "#{myOutputS3Loc}/#{format(@scheduledStartTime, 'YYYY-MM-dd-HH-mm-ss')}"
      - 
        Id: "DDBSourceTable"
        Name: "DDBSourceTable"
        Fields: 
          - 
            Key: "tableName"
            StringValue: "#{myDDBTableName}"
          - 
            Key: "type"
            StringValue: "DynamoDBDataNode"
          - 
            Key: "dataFormat"
            RefValue: "DDBExportFormat"
          - 
            Key: "readThroughputPercent"
            StringValue: "#{myDDBReadThroughputRatio}"
      - 
        Id: "DDBExportFormat"
        Name: "DDBExportFormat"
        Fields: 
          - 
            Key: "type"
            StringValue: "DynamoDBExportDataFormat"
      - 
        Id: "TableBackupActivity"
        Name: "TableBackupActivity"
        Fields: 
          - 
            Key: "resizeClusterBeforeRunning"
            StringValue: "true"
          - 
            Key: "type"
            StringValue: "HiveCopyActivity"
          - 
            Key: "input"
            RefValue: "DDBSourceTable"
          - 
            Key: "runsOn"
            RefValue: "EmrClusterForBackup"
          - 
            Key: "output"
            RefValue: "S3BackupLocation"
      - 
        Id: "DefaultSchedule"
        Name: "RunOnce"
        Fields: 
          - 
            Key: "occurrences"
            StringValue: "1"
          - 
            Key: "startAt"
            StringValue: "FIRST_ACTIVATION_DATE_TIME"
          - 
            Key: "type"
            StringValue: "Schedule"
          - 
            Key: "period"
            StringValue: "1 Day"
      - 
        Id: "Default"
        Name: "Default"
        Fields: 
          - 
            Key: "type"
            StringValue: "Default"
          - 
            Key: "scheduleType"
            StringValue: "cron"
          - 
            Key: "failureAndRerunMode"
            StringValue: "CASCADE"
          - 
            Key: "role"
            StringValue: "DataPipelineDefaultRole"
          - 
            Key: "resourceRole"
            StringValue: "DataPipelineDefaultResourceRole"
          - 
            Key: "schedule"
            RefValue: "DefaultSchedule"
      - 
        Id: "EmrClusterForBackup"
        Name: "EmrClusterForBackup"
        Fields: 
          - 
            Key: "terminateAfter"
            StringValue: "2 Hours"
          - 
            Key: "amiVersion"
            StringValue: "3.3.2"
          - 
            Key: "masterInstanceType"
            StringValue: "m1.medium"
          - 
            Key: "coreInstanceType"
            StringValue: "m1.medium"
          - 
            Key: "coreInstanceCount"
            StringValue: "1"
          - 
            Key: "type"
            StringValue: "EmrCluster"
```

## See also<a name="aws-resource-datapipeline-pipeline--seealso"></a>
+  [Pipeline Object Reference](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-pipeline-objects.html) in the *AWS Data Pipeline Developer Guide*\.
+  [PutPipelineDefinition](https://docs.aws.amazon.com/datapipeline/latest/APIReference/API_PutPipelineDefinition.html) in the *AWS Data Pipeline API Reference*\.

