# AWS::DMS::ReplicationConfig<a name="aws-resource-dms-replicationconfig"></a>



## Syntax<a name="aws-resource-dms-replicationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-replicationconfig-syntax.json"></a>

```
{
  "Type" : "AWS::DMS::ReplicationConfig",
  "Properties" : {
      "[ComputeConfig](#cfn-dms-replicationconfig-computeconfig)" : ComputeConfig,
      "[ReplicationConfigArn](#cfn-dms-replicationconfig-replicationconfigarn)" : String,
      "[ReplicationConfigIdentifier](#cfn-dms-replicationconfig-replicationconfigidentifier)" : String,
      "[ReplicationSettings](#cfn-dms-replicationconfig-replicationsettings)" : Json,
      "[ReplicationType](#cfn-dms-replicationconfig-replicationtype)" : String,
      "[ResourceIdentifier](#cfn-dms-replicationconfig-resourceidentifier)" : String,
      "[SourceEndpointArn](#cfn-dms-replicationconfig-sourceendpointarn)" : String,
      "[SupplementalSettings](#cfn-dms-replicationconfig-supplementalsettings)" : Json,
      "[TableMappings](#cfn-dms-replicationconfig-tablemappings)" : Json,
      "[Tags](#cfn-dms-replicationconfig-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TargetEndpointArn](#cfn-dms-replicationconfig-targetendpointarn)" : String
    }
}
```

### YAML<a name="aws-resource-dms-replicationconfig-syntax.yaml"></a>

```
Type: AWS::DMS::ReplicationConfig
Properties: 
  [ComputeConfig](#cfn-dms-replicationconfig-computeconfig): 
    ComputeConfig
  [ReplicationConfigArn](#cfn-dms-replicationconfig-replicationconfigarn): String
  [ReplicationConfigIdentifier](#cfn-dms-replicationconfig-replicationconfigidentifier): String
  [ReplicationSettings](#cfn-dms-replicationconfig-replicationsettings): Json
  [ReplicationType](#cfn-dms-replicationconfig-replicationtype): String
  [ResourceIdentifier](#cfn-dms-replicationconfig-resourceidentifier): String
  [SourceEndpointArn](#cfn-dms-replicationconfig-sourceendpointarn): String
  [SupplementalSettings](#cfn-dms-replicationconfig-supplementalsettings): Json
  [TableMappings](#cfn-dms-replicationconfig-tablemappings): Json
  [Tags](#cfn-dms-replicationconfig-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TargetEndpointArn](#cfn-dms-replicationconfig-targetendpointarn): String
```

## Properties<a name="aws-resource-dms-replicationconfig-properties"></a>

`ComputeConfig`  <a name="cfn-dms-replicationconfig-computeconfig"></a>
Configuration parameters for provisioning an AWS DMS Serverless replication\.  
*Required*: No  
*Type*: [ComputeConfig](aws-properties-dms-replicationconfig-computeconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationConfigArn`  <a name="cfn-dms-replicationconfig-replicationconfigarn"></a>
The Amazon Resource Name \(ARN\) of this AWS DMS Serverless replication configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationConfigIdentifier`  <a name="cfn-dms-replicationconfig-replicationconfigidentifier"></a>
A unique identifier that you want to use to create a `ReplicationConfigArn` that is returned as part of the output from this action\. You can then pass this output `ReplicationConfigArn` as the value of the `ReplicationConfigArn` option for other actions to identify both AWS DMS Serverless replications and replication configurations that you want those actions to operate on\. For some actions, you can also use either this unique identifier or a corresponding ARN in action filters to identify the specific replication and replication configuration to operate on\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationSettings`  <a name="cfn-dms-replicationconfig-replicationsettings"></a>
Optional JSON settings for AWS DMS Serverless replications that are provisioned using this replication configuration\. For example, see [ Change processing tuning settings](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TaskSettings.ChangeProcessingTuning.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationType`  <a name="cfn-dms-replicationconfig-replicationtype"></a>
The type of AWS DMS Serverless replication to provision using this replication configuration\.  
Possible values:  
+  `"full-load"` 
+  `"cdc"` 
+  `"full-load-and-cdc"` 
*Required*: No  
*Type*: String  
*Allowed values*: `cdc | full-load | full-load-and-cdc`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceIdentifier`  <a name="cfn-dms-replicationconfig-resourceidentifier"></a>
Optional unique value or name that you set for a given resource that can be used to construct an Amazon Resource Name \(ARN\) for that resource\. For more information, see [ Fine\-grained access control using resource names and tags](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.html#CHAP_Security.FineGrainedAccess)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceEndpointArn`  <a name="cfn-dms-replicationconfig-sourceendpointarn"></a>
The Amazon Resource Name \(ARN\) of the source endpoint for this AWS DMS Serverless replication configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupplementalSettings`  <a name="cfn-dms-replicationconfig-supplementalsettings"></a>
Optional JSON settings for specifying supplemental data\. For more information, see [ Specifying supplemental data for task settings](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.TaskData.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableMappings`  <a name="cfn-dms-replicationconfig-tablemappings"></a>
JSON table mappings for AWS DMS Serverless replications that are provisioned using this replication configuration\. For more information, see [ Specifying table selection and transformations rules using JSON](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TableMapping.SelectionTransformation.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-dms-replicationconfig-tags"></a>
One or more optional tags associated with resources used by the AWS DMS Serverless replication\. For more information, see [ Tagging resources in AWS Database Migration Service](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tagging.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetEndpointArn`  <a name="cfn-dms-replicationconfig-targetendpointarn"></a>
The Amazon Resource Name \(ARN\) of the target endpoint for this AWS DMS serverless replication configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-dms-replicationconfig-return-values"></a>

### Ref<a name="aws-resource-dms-replicationconfig-return-values-ref"></a>