# AWS::DMS::ReplicationTask<a name="aws-resource-dms-replicationtask"></a>

The `AWS::DMS::ReplicationTask` resource creates an AWS DMS replication task\.

## Syntax<a name="aws-resource-dms-replicationtask-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-replicationtask-syntax.json"></a>

```
{
  "Type" : "AWS::DMS::ReplicationTask",
  "Properties" : {
      "[CdcStartPosition](#cfn-dms-replicationtask-cdcstartposition)" : String,
      "[CdcStartTime](#cfn-dms-replicationtask-cdcstarttime)" : Double,
      "[CdcStopPosition](#cfn-dms-replicationtask-cdcstopposition)" : String,
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
  [CdcStartPosition](#cfn-dms-replicationtask-cdcstartposition): String
  [CdcStartTime](#cfn-dms-replicationtask-cdcstarttime): Double
  [CdcStopPosition](#cfn-dms-replicationtask-cdcstopposition): String
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

`CdcStartPosition`  <a name="cfn-dms-replicationtask-cdcstartposition"></a>
Indicates when you want a change data capture \(CDC\) operation to start\. Use either CdcStartPosition or CdcStartTime to specify when you want a CDC operation to start\. Specifying both values results in an error\.  
 The value can be in date, checkpoint, or LSN/SCN format\.  
Date Example: \-\-cdc\-start\-position “2018\-03\-08T12:12:12”  
Checkpoint Example: \-\-cdc\-start\-position "checkpoint:V1\#27\#mysql\-bin\-changelog\.157832:1975:\-1:2002:677883278264080:mysql\-bin\-changelog\.157832:1876\#0\#0\#\*\#0\#93"  
LSN Example: \-\-cdc\-start\-position “mysql\-bin\-changelog\.000024:373”  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CdcStartTime`  <a name="cfn-dms-replicationtask-cdcstarttime"></a>
Indicates the start time for a change data capture \(CDC\) operation\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CdcStopPosition`  <a name="cfn-dms-replicationtask-cdcstopposition"></a>
Indicates when you want a change data capture \(CDC\) operation to stop\. The value can be either server time or commit time\.  
Server time example: \-\-cdc\-stop\-position “server\_time:3018\-02\-09T12:12:12”  
Commit time example: \-\-cdc\-stop\-position “commit\_time: 3018\-02\-09T12:12:12 “  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MigrationType`  <a name="cfn-dms-replicationtask-migrationtype"></a>
The migration type\. Valid values: `full-load` \| `cdc` \| `full-load-and-cdc`   
*Required*: Yes  
*Type*: String  
*Allowed Values*: `cdc | full-load | full-load-and-cdc`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationInstanceArn`  <a name="cfn-dms-replicationtask-replicationinstancearn"></a>
The Amazon Resource Name \(ARN\) of a replication instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplicationTaskIdentifier`  <a name="cfn-dms-replicationtask-replicationtaskidentifier"></a>
An identifier for the replication task\.  
Constraints:  
+ Must contain from 1 to 255 alphanumeric characters or hyphens\.
+ First character must be a letter\.
+ Cannot end with a hyphen or contain two consecutive hyphens\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationTaskSettings`  <a name="cfn-dms-replicationtask-replicationtasksettings"></a>
Overall settings for the task, in JSON format\. For more information, see [Task Settings](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TaskSettings.html) in the *AWS Database Migration User Guide\.*   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceEndpointArn`  <a name="cfn-dms-replicationtask-sourceendpointarn"></a>
An Amazon Resource Name \(ARN\) that uniquely identifies the source endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableMappings`  <a name="cfn-dms-replicationtask-tablemappings"></a>
The table mappings for the task, in JSON format\. For more information, see [Table Mapping](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TableMapping.html) in the *AWS Database Migration User Guide\.*   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-dms-replicationtask-tags"></a>
One or more tags to be assigned to the replication task\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetEndpointArn`  <a name="cfn-dms-replicationtask-targetendpointarn"></a>
An Amazon Resource Name \(ARN\) that uniquely identifies the target endpoint\.  
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

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `cn-north-1`
- `cn-northwest-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
