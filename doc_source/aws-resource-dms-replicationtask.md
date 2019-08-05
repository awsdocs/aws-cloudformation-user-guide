# AWS::DMS::ReplicationTask<a name="aws-resource-dms-replicationtask"></a>

The `AWS::DMS::ReplicationTask` resource creates an AWS DMS replication task\.

## Syntax<a name="aws-resource-dms-replicationtask-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-replicationtask-syntax.json"></a>

```
{
  "Type" : "AWS::DMS::ReplicationTask",
  "Properties" : {
      "[CdcStartTime](#cfn-dms-replicationtask-cdcstarttime)" : Double,
      "[MigrationType](#cfn-dms-replicationtask-migrationtype)" : String,
      "[ReplicationInstanceArn](#cfn-dms-replicationtask-replicationinstancearn)" : String,
      "[ReplicationTaskIdentifier](#cfn-dms-replicationtask-replicationtaskidentifier)" : String,
      "[ReplicationTaskSettings](#cfn-dms-replicationtask-replicationtasksettings)" : String,
      "[SourceEndpointArn](#cfn-dms-replicationtask-sourceendpointarn)" : String,
      "[TableMappings](#cfn-dms-replicationtask-tablemappings)" : String,
      "[Tags](#cfn-dms-replicationtask-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TargetEndpointArn](#cfn-dms-replicationtask-targetendpointarn)" : String
    }
}
```

### YAML<a name="aws-resource-dms-replicationtask-syntax.yaml"></a>

```
Type: AWS::DMS::ReplicationTask
Properties:
  [CdcStartTime](#cfn-dms-replicationtask-cdcstarttime): Double
  [MigrationType](#cfn-dms-replicationtask-migrationtype): String
  [ReplicationInstanceArn](#cfn-dms-replicationtask-replicationinstancearn): String
  [ReplicationTaskIdentifier](#cfn-dms-replicationtask-replicationtaskidentifier): String
  [ReplicationTaskSettings](#cfn-dms-replicationtask-replicationtasksettings): String
  [SourceEndpointArn](#cfn-dms-replicationtask-sourceendpointarn): String
  [TableMappings](#cfn-dms-replicationtask-tablemappings): String
  [Tags](#cfn-dms-replicationtask-tags):
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TargetEndpointArn](#cfn-dms-replicationtask-targetendpointarn): String
```

## Properties<a name="aws-resource-dms-replicationtask-properties"></a>

`CdcStartTime`  <a name="cfn-dms-replicationtask-cdcstarttime"></a>
Indicates the start time for a change data capture \(CDC\) operation\.
*Required*: No
*Type*: Double
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MigrationType`  <a name="cfn-dms-replicationtask-migrationtype"></a>
The migration type\.
*Required*: Yes
*Type*: String
*Allowed Values*: `cdc | full-load | full-load-and-cdc`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationInstanceArn`  <a name="cfn-dms-replicationtask-replicationinstancearn"></a>
The Amazon Resource Name \(ARN\) of the replication instance\.
*Required*: Yes
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplicationTaskIdentifier`  <a name="cfn-dms-replicationtask-replicationtaskidentifier"></a>
The replication task identifier\.
Constraints:
+ Must contain from 1 to 255 alphanumeric characters or hyphens\.
+ First character must be a letter\.
+ Cannot end with a hyphen or contain two consecutive hyphens\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationTaskSettings`  <a name="cfn-dms-replicationtask-replicationtasksettings"></a>
Settings for the task, such as target metadata settings\. For a complete list of task settings, see [Task Settings for AWS Database Migration Service Tasks](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TaskSettings.html) in the *AWS Database Migration User Guide\.*
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceEndpointArn`  <a name="cfn-dms-replicationtask-sourceendpointarn"></a>
The Amazon Resource Name \(ARN\) string that uniquely identifies the endpoint\.
*Required*: Yes
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableMappings`  <a name="cfn-dms-replicationtask-tablemappings"></a>
When using the AWS CLI or boto3, provide the path of the JSON file that contains the table mappings\. Precede the path with "file://"\. When working with the DMS API, provide the JSON as the parameter value\.
For example, \-\-table\-mappings file://mappingfile\.json
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-dms-replicationtask-tags"></a>
Tags to be added to the replication instance\.
*Required*: No
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetEndpointArn`  <a name="cfn-dms-replicationtask-targetendpointarn"></a>
The Amazon Resource Name \(ARN\) string that uniquely identifies the endpoint\.
*Required*: Yes
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-dms-replicationtask-return-values"></a>

### Ref<a name="aws-resource-dms-replicationtask-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the replication task ARN\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-dms-replicationtask--examples"></a>

### <a name="aws-resource-dms-replicationtask--examples--"></a>

#### JSON<a name="aws-resource-dms-replicationtask--examples----json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "myReplicationTask": {
            "Type": "AWS::DMS::ReplicationTask",
            "Properties": {
                "SourceEndpointArn": 11,
                "TargetEndpointArn": "12ff",
                "ReplicationInstanceArn": "ert1",
                "MigrationType": "full-load",
                "TableMappings": "{ \"rules\": [ { \"rule-type\": \"selection\", \"rule-id\": \"1\", \"rule-name\": \"1\", \"object-locator\": { \"schema-name\": \"%\", \"table-name\": \"%\" }, \"rule-action\": \"include\" } ] }"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-dms-replicationtask--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myReplicationTask:
    Properties:
      MigrationType: full-load
      ReplicationInstanceArn: ReplicationInstance
      SourceEndpointArn: SourceEndpoint
      TableMappings: "{ \"rules\": [ { \"rule-type\": \"selection\", \"rule-id\": \"1\", \"rule-name\": \"1\", \"object-locator\": { \"schema-name\": \"%\", \"table-name\": \"%\" }, \"rule-action\": \"include\" } ] }"
      TargetEndpointArn: TargetEndpoint
    Type: "AWS::DMS::ReplicationTask"
```

## See Also<a name="aws-resource-dms-replicationtask--seealso"></a>
+  [CreateReplicationTask](https://docs.aws.amazon.com/dms/latest/APIReference/API_CreateReplicationTask.html) in the *AWS Database Migration Service API Reference*
+  [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)
