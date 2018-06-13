# AWS::DataPipeline::Pipeline<a name="aws-resource-datapipeline-pipeline"></a>

Creates a data pipeline that you can use to automate the movement and transformation of data\. In each pipeline, you define pipeline objects, such as activities, schedules, data nodes, and resources\. For information about pipeline objects and components that you can use, see [Pipeline Object Reference](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-pipeline-objects.html) in the *AWS Data Pipeline Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-datapipeline-pipeline-syntax)
+ [Properties](#w3ab2c21c10d321b9)
+ [Return Values](#w3ab2c21c10d321c11)
+ [Example](#w3ab2c21c10d321c13)

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
    "[ParameterObjects](#cfn-datapipeline-pipeline-parameterobjects)" : [ Parameter object, ... ],
    "[ParameterValues](#cfn-datapipeline-pipeline-parametervalues)" : [ Parameter value, ... ],
    "[PipelineObjects](#cfn-datapipeline-pipeline-pipelineobjects)" : [ Pipeline object, ... ],
    "[PipelineTags](#cfn-datapipeline-pipeline-pipelinetags)" : [ Pipeline tag, ... ]
  }
}
```

### YAML<a name="aws-resource-datapipeline-pipeline-syntax.yaml"></a>

```
Type: "AWS::DataPipeline::Pipeline"
Properties:
  [Activate](#cfn-datapipeline-pipeline-activate): Boolean
  [Description](#cfn-datapipeline-pipeline-description): String
  [Name](#cfn-datapipeline-pipeline-name): String
  [ParameterObjects](#cfn-datapipeline-pipeline-parameterobjects):
    - Parameter object
  [ParameterValues](#cfn-datapipeline-pipeline-parametervalues):
    - Parameter value
  [PipelineObjects](#cfn-datapipeline-pipeline-pipelineobjects):
    - Pipeline object
  [PipelineTags](#cfn-datapipeline-pipeline-pipelinetags):
    - Pipeline tag
```

## Properties<a name="w3ab2c21c10d321b9"></a>

`Activate`  <a name="cfn-datapipeline-pipeline-activate"></a>
Indicates whether to validate and start the pipeline or stop an active pipeline\. By default, the value is set to `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-datapipeline-pipeline-description"></a>
A description for the pipeline\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`Name`  <a name="cfn-datapipeline-pipeline-name"></a>
A name for the pipeline\. Because AWS CloudFormation assigns each new pipeline a unique identifier, you can use the same name for multiple pipelines that are associated with your AWS account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ParameterObjects`  <a name="cfn-datapipeline-pipeline-parameterobjects"></a>
Defines the variables that are in the pipeline definition\. For more information, see [Creating a Pipeline Using Parameterized Templates](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-custom-templates.html) in the *AWS Data Pipeline Developer Guide*\.  
*Required*: No  
*Type*: [AWS Data Pipeline Pipeline ParameterObjects](aws-properties-datapipeline-pipeline-parameterobjects.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ParameterValues`  <a name="cfn-datapipeline-pipeline-parametervalues"></a>
Defines the values for the parameters that are defined in the `ParameterObjects` property\. For more information, see [Creating a Pipeline Using Parameterized Templates](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-custom-templates.html) in the *AWS Data Pipeline Developer Guide*\.  
*Required*: No  
*Type*: [AWS Data Pipeline Pipeline ParameterValues](aws-properties-datapipeline-pipeline-parametervalues.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PipelineObjects`  <a name="cfn-datapipeline-pipeline-pipelineobjects"></a>
A list of pipeline objects that make up the pipeline\. For more information about pipeline objects and a description of each object, see [Pipeline Object Reference](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-pipeline-objects.html) in the *AWS Data Pipeline Developer Guide*\.  
*Required*: Yes  
*Type*: A list of [AWS Data Pipeline PipelineObject](aws-properties-datapipeline-pipeline-pipelineobjects.md)  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. Not all objects, fields, and values can be updated\. Restrictions on what can be updated are documented in [Editing Your Pipelines](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-manage-pipeline-modify-console.html) in the *AWS Data Pipeline Developer Guide*\.

`PipelineTags`  <a name="cfn-datapipeline-pipeline-pipelinetags"></a>
A list of arbitrary tags \(key\-value pairs\) to associate with the pipeline, which you can use to control permissions\. For more information, see [Controlling Access to Pipelines and Resources](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-control-access.html) in the *AWS Data Pipeline Developer Guide*\.  
*Required*: No  
*Type*: [AWS Data Pipeline Pipeline PipelineTags](aws-properties-datapipeline-pipeline-pipelinetags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d321c11"></a>

### Ref<a name="w3ab2c21c10d321c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

 When you specify an `AWS::DataPipeline::Pipeline` resource as an argument to the `Ref` function, AWS CloudFormation returns the pipeline ID\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d321c13"></a>

The following data pipeline backs up data from an Amazon DynamoDB \(DynamoDB\) table to an Amazon Simple Storage Service \(Amazon S3\) bucket\. The pipeline uses the `HiveCopyActivity` activity to copy the data, and runs it once a day\. The [roles](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-iam-roles.html) for the pipeline and the pipeline resource are declared elsewhere in the same template\.

### JSON<a name="aws-resource-datapipeline-pipeline-example.json"></a>

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

### YAML<a name="aws-resource-datapipeline-pipeline-example.yaml"></a>

```
DynamoDBInputS3OutputHive: 
  Type: "AWS::DataPipeline::Pipeline"
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