# AWS::DMS::ReplicationTask<a name="aws-resource-dms-replicationtask"></a>

The `AWS::DMS::ReplicationTask` resource creates an AWS DMS replication task\.

**Topics**
+ [Syntax](#aws-resource-dms-replicationtask-syntax)
+ [Properties](#aws-resource-dms-replicationtask-prop)
+ [Return Value](#w3ab2c21c10d368c11)
+ [Example](#aws-resource-dms-replicationtask-example)
+ [See Also](#w3ab2c21c10d368c15)

## Syntax<a name="aws-resource-dms-replicationtask-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-replicationtask-syntax.json"></a>

```
{
  "Type": "AWS::DMS::ReplicationTask",
  "Properties": {
    "[CdcStartTime](#cfn-dms-replicationtask-cdcstarttime)": Timestamp,
    "[MigrationType](#cfn-dms-replicationtask-migrationtype)": String,
    "[ReplicationInstanceArn](#cfn-dms-replicationtask-replicationinstancearn)": String,
    "[ReplicationTaskIdentifier](#cfn-dms-replicationtask-replicationtaskidentifier)": String,
    "[ReplicationTaskSettings](#cfn-dms-replicationtask-replicationstasksettings)": String,
    "[SourceEndpointArn](#cfn-dms-replicationtask-sourceendpointarn)": String,
    "[TableMappings](#cfn-dms-replicationtask-tablemappings)": String,
    "[Tags](#cfn-dms-replicationtask-tags)": [ Resource Tag, ... ],
    "[TargetEndpointArn](#cfn-dms-replicationtask-targetendpointarn)": String
  }
}
```

### YAML<a name="aws-resource-dms-replicationtask-syntax.yaml"></a>

```
Type: "AWS::DMS::ReplicationTask"
Properties:
  [CdcStartTime](#cfn-dms-replicationtask-cdcstarttime): Timestamp
  [MigrationType](#cfn-dms-replicationtask-migrationtype): String
  [ReplicationInstanceArn](#cfn-dms-replicationtask-replicationinstancearn): String
  [ReplicationTaskIdentifier](#cfn-dms-replicationtask-replicationtaskidentifier): String
  [ReplicationTaskSettings](#cfn-dms-replicationtask-replicationstasksettings): String
  [SourceEndpointArn](#cfn-dms-replicationtask-sourceendpointarn): String
  [TableMappings](#cfn-dms-replicationtask-tablemappings): String
  [Tags](#cfn-dms-replicationtask-tags): 
    - Resource Tag
  [TargetEndpointArn](#cfn-dms-replicationtask-targetendpointarn): String
```

## Properties<a name="aws-resource-dms-replicationtask-prop"></a>

`CdcStartTime`  <a name="cfn-dms-replicationtask-cdcstarttime"></a>
The start time for the Change Data Capture \(CDC\) operation\.  
*Required*: No  
*Type: *Number, epic value in milliseconds  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MigrationType`  <a name="cfn-dms-replicationtask-migrationtype"></a>
The migration type\.  
`Valid Values`: `full-load`, `cdc`, `full-load-and-cdc`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ReplicationInstanceArn`  <a name="cfn-dms-replicationtask-replicationinstancearn"></a>
The Amazon Resource Name \(ARN\) of the replication instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ReplicationTaskIdentifier`  <a name="cfn-dms-replicationtask-replicationtaskidentifier"></a>
The ARN string that uniquely identifies the endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ReplicationTaskSettings`  <a name="cfn-dms-replicationtask-replicationstasksettings"></a>
Settings for the task, such as target metadata settings\. For a complete list of task settings, see [Task Settings for AWS Database Migration Service Tasks](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TaskSettings.html) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SourceEndpointArn`  <a name="cfn-dms-replicationtask-sourceendpointarn"></a>
The ARN string that uniquely identifies the endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TableMappings`  <a name="cfn-dms-replicationtask-tablemappings"></a>
The JSON that contains additional parameter values\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-dms-replicationtask-tags"></a>
The tags that you want to attach to the migration task\.  
*Required*: No  
*Type*: List of [resource tags](aws-properties-resource-tags.md) in key\-value format  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TargetEndpointArn`  <a name="cfn-dms-replicationtask-targetendpointarn"></a>
The ARN string that uniquely identifies the endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10d368c11"></a>

### Ref<a name="w3ab2c21c10d368c11b2"></a>

When you pass the logical ID of an `AWS::DMS::ReplicationTask` resource to the intrinsic `Ref` function, the function returns the replication task ARN\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-dms-replicationtask-example"></a>

### JSON<a name="aws-resource-dms-replicationtask-example.json"></a>

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

### YAML<a name="aws-resource-dms-replicationtask-example.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myReplicationTask:
    Type: "AWS::DMS::ReplicationTask"
    Properties:
      SourceEndpointArn: !Ref SourceEndpoint
      TargetEndpointArn: !Ref TargetEndpoint
      ReplicationInstanceArn: !Ref ReplicationInstance
      MigrationType: "full-load"
      TableMappings: "{
        \"rules\": [
          {
            \"rule-type\": \"selection\",
            \"rule-id\": \"1\",
            \"rule-name\": \"1\",
            \"object-locator\": {
              \"schema-name\": \"%\",
              \"table-name\": \"%\"
            },
            \"rule-action\": \"include\"
          }
        ]
      }"
```

## See Also<a name="w3ab2c21c10d368c15"></a>
+ [CreateReplicationTask](http://docs.aws.amazon.com/dms/latest/APIReference/API_CreateReplicationTask.html) in the *AWS Database Migration Service API Reference*\.
+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)