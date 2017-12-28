# AWS::DMS::ReplicationTask<a name="aws-resource-dms-replicationtask"></a>

The `AWS::DMS::ReplicationTask` resource creates an AWS DMS replication task\.


+ [Syntax](#aws-resource-dms-replicationtask-syntax)
+ [Properties](#aws-resource-dms-replicationtask-prop)
+ [Return Value](#w3ab2c21c10d331c11)
+ [Example](#aws-resource-dms-replicationtask-example)
+ [See Also](#w3ab2c21c10d331c15)

## Syntax<a name="aws-resource-dms-replicationtask-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-replicationtask-syntax.json"></a>

```
{
  "Type": "AWS::DMS::ReplicationTask",
  "Properties": {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-cdcstarttime)": Timestamp,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-migrationtype)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-replicationinstancearn)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-replicationtaskidentifier)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-replicationstasksettings)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-sourceendpointarn)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-tablemappings)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-tags)": [ Resource Tag, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-targetendpointarn)": String
  }
}
```

### YAML<a name="aws-resource-dms-replicationtask-syntax.yaml"></a>

```
Type: "AWS::DMS::ReplicationTask"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-cdcstarttime): Timestamp
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-migrationtype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-replicationinstancearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-replicationtaskidentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-replicationstasksettings): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-sourceendpointarn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-tablemappings): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-tags): 
    - Resource Tag
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationtask-targetendpointarn): String
```

## Properties<a name="aws-resource-dms-replicationtask-prop"></a>

`CdcStartTime`  
The start time for the Change Data Capture \(CDC\) operation\.  
*Required: *No  
*Type: *Number, epic value in milliseconds  
*Update requires*: No interruption

`MigrationType`  
The migration type\.  
`Valid Values`: `full-load`, `cdc`, `full-load-and-cdc`  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`ReplicationInstanceArn`  
The Amazon Resource Name \(ARN\) of the replication instance\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`ReplicationTaskIdentifier`  
The ARN string that uniquely identifies the endpoint\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`ReplicationTaskSettings`  
Settings for the task, such as target metadata settings\. For a complete list of task settings, see [Task Settings for AWS Database Migration Service Tasks](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TaskSettings.html) in the *AWS Database Migration Service User Guide*\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption 

`SourceEndpointArn`  
The ARN string that uniquely identifies the endpoint\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`TableMappings`  
The JSON that contains additional parameter values\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`Tags`  
The tags that you want to attach to the migration task\.  
*Required: *No  
*Type*: List of resource tags in key\-value format  
*Update requires*: Replacement 

`TargetEndpointArn`  
The ARN string that uniquely identifies the endpoint\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

## Return Value<a name="w3ab2c21c10d331c11"></a>

### Ref<a name="w3ab2c21c10d331c11b2"></a>

When you pass the logical ID of an `AWS::DMS::ReplicationTask` resource to the intrinsic `Ref` function, the function returns the replication task ARN\.

For more information about using the `Ref` function, see Ref\.

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

## See Also<a name="w3ab2c21c10d331c15"></a>

+ [CreateReplicationTask](http://docs.aws.amazon.com/dms/latest/APIReference/API_CreateReplicationTask.html) in the *AWS Database Migration Service API Reference*\.

+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)