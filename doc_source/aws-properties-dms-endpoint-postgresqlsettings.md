# AWS::DMS::Endpoint PostgreSqlSettings<a name="aws-properties-dms-endpoint-postgresqlsettings"></a>

Provides information that defines a PostgreSQL endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For information about other available settings, see [ Extra connection attributes when using PostgreSQL as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.PostgreSQL.html#CHAP_Source.PostgreSQL.ConnectionAttrib) and [ Extra connection attributes when using PostgreSQL as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.PostgreSQL.html#CHAP_Target.PostgreSQL.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-postgresqlsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-postgresqlsettings-syntax.json"></a>

```
{
  "[AfterConnectScript](#cfn-dms-endpoint-postgresqlsettings-afterconnectscript)" : String,
  "[CaptureDdls](#cfn-dms-endpoint-postgresqlsettings-captureddls)" : Boolean,
  "[DdlArtifactsSchema](#cfn-dms-endpoint-postgresqlsettings-ddlartifactsschema)" : String,
  "[ExecuteTimeout](#cfn-dms-endpoint-postgresqlsettings-executetimeout)" : Integer,
  "[FailTasksOnLobTruncation](#cfn-dms-endpoint-postgresqlsettings-failtasksonlobtruncation)" : Boolean,
  "[HeartbeatEnable](#cfn-dms-endpoint-postgresqlsettings-heartbeatenable)" : Boolean,
  "[HeartbeatFrequency](#cfn-dms-endpoint-postgresqlsettings-heartbeatfrequency)" : Integer,
  "[HeartbeatSchema](#cfn-dms-endpoint-postgresqlsettings-heartbeatschema)" : String,
  "[MaxFileSize](#cfn-dms-endpoint-postgresqlsettings-maxfilesize)" : Integer,
  "[PluginName](#cfn-dms-endpoint-postgresqlsettings-pluginname)" : String,
  "[SecretsManagerAccessRoleArn](#cfn-dms-endpoint-postgresqlsettings-secretsmanageraccessrolearn)" : String,
  "[SecretsManagerSecretId](#cfn-dms-endpoint-postgresqlsettings-secretsmanagersecretid)" : String,
  "[SlotName](#cfn-dms-endpoint-postgresqlsettings-slotname)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-postgresqlsettings-syntax.yaml"></a>

```
  [AfterConnectScript](#cfn-dms-endpoint-postgresqlsettings-afterconnectscript): String
  [CaptureDdls](#cfn-dms-endpoint-postgresqlsettings-captureddls): Boolean
  [DdlArtifactsSchema](#cfn-dms-endpoint-postgresqlsettings-ddlartifactsschema): String
  [ExecuteTimeout](#cfn-dms-endpoint-postgresqlsettings-executetimeout): Integer
  [FailTasksOnLobTruncation](#cfn-dms-endpoint-postgresqlsettings-failtasksonlobtruncation): Boolean
  [HeartbeatEnable](#cfn-dms-endpoint-postgresqlsettings-heartbeatenable): Boolean
  [HeartbeatFrequency](#cfn-dms-endpoint-postgresqlsettings-heartbeatfrequency): Integer
  [HeartbeatSchema](#cfn-dms-endpoint-postgresqlsettings-heartbeatschema): String
  [MaxFileSize](#cfn-dms-endpoint-postgresqlsettings-maxfilesize): Integer
  [PluginName](#cfn-dms-endpoint-postgresqlsettings-pluginname): String
  [SecretsManagerAccessRoleArn](#cfn-dms-endpoint-postgresqlsettings-secretsmanageraccessrolearn): String
  [SecretsManagerSecretId](#cfn-dms-endpoint-postgresqlsettings-secretsmanagersecretid): String
  [SlotName](#cfn-dms-endpoint-postgresqlsettings-slotname): String
```

## Properties<a name="aws-properties-dms-endpoint-postgresqlsettings-properties"></a>

`AfterConnectScript`  <a name="cfn-dms-endpoint-postgresqlsettings-afterconnectscript"></a>
For use with change data capture \(CDC\) only, this attribute has AWS DMS bypass foreign keys and user triggers to reduce the time it takes to bulk load data\.  
Example: `afterConnectScript=SET session_replication_role='replica'`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptureDdls`  <a name="cfn-dms-endpoint-postgresqlsettings-captureddls"></a>
To capture DDL events, AWS DMS creates various artifacts in the PostgreSQL database when the task starts\. You can later remove these artifacts\.  
If this value is set to `N`, you don't have to create tables or triggers on the source database\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DdlArtifactsSchema`  <a name="cfn-dms-endpoint-postgresqlsettings-ddlartifactsschema"></a>
The schema in which the operational DDL database artifacts are created\.  
Example: `ddlArtifactsSchema=xyzddlschema;`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecuteTimeout`  <a name="cfn-dms-endpoint-postgresqlsettings-executetimeout"></a>
Sets the client statement timeout for the PostgreSQL instance, in seconds\. The default value is 60 seconds\.  
Example: `executeTimeout=100;`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailTasksOnLobTruncation`  <a name="cfn-dms-endpoint-postgresqlsettings-failtasksonlobtruncation"></a>
When set to `true`, this value causes a task to fail if the actual size of a LOB column is greater than the specified `LobMaxSize`\.  
If task is set to Limited LOB mode and this option is set to true, the task fails instead of truncating the LOB data\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeartbeatEnable`  <a name="cfn-dms-endpoint-postgresqlsettings-heartbeatenable"></a>
The write\-ahead log \(WAL\) heartbeat feature mimics a dummy transaction\. By doing this, it prevents idle logical replication slots from holding onto old WAL logs, which can result in storage full situations on the source\. This heartbeat keeps `restart_lsn` moving and prevents storage full scenarios\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeartbeatFrequency`  <a name="cfn-dms-endpoint-postgresqlsettings-heartbeatfrequency"></a>
Sets the WAL heartbeat frequency \(in minutes\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeartbeatSchema`  <a name="cfn-dms-endpoint-postgresqlsettings-heartbeatschema"></a>
Sets the schema in which the heartbeat artifacts are created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxFileSize`  <a name="cfn-dms-endpoint-postgresqlsettings-maxfilesize"></a>
Specifies the maximum size \(in KB\) of any \.csv file used to transfer data to PostgreSQL\.  
Example: `maxFileSize=512`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PluginName`  <a name="cfn-dms-endpoint-postgresqlsettings-pluginname"></a>
Specifies the plugin to use to create a replication slot\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerAccessRoleArn`  <a name="cfn-dms-endpoint-postgresqlsettings-secretsmanageraccessrolearn"></a>
The full Amazon Resource Name \(ARN\) of the IAM role that specifies AWS DMS as the trusted entity and grants the required permissions to access the value in `SecretsManagerSecret`\. The role must allow the `iam:PassRole` action\. `SecretsManagerSecret` has the value of the AWS Secrets Manager secret that allows access to the PostgreSQL endpoint\.  
You can specify one of two sets of values for these permissions\. You can specify the values for this setting and `SecretsManagerSecretId`\. Or you can specify clear\-text values for `UserName`, `Password`, `ServerName`, and `Port`\. You can't specify both\.  
For more information on creating this `SecretsManagerSecret`, the corresponding `SecretsManagerAccessRoleArn`, and the `SecretsManagerSecretId` that is required to access it, see [ Using secrets to access AWS Database Migration Service resources](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.html#security-iam-secretsmanager) in the *AWS Database Migration Service User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerSecretId`  <a name="cfn-dms-endpoint-postgresqlsettings-secretsmanagersecretid"></a>
The full ARN, partial ARN, or display name of the `SecretsManagerSecret` that contains the PostgreSQL endpoint connection details\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotName`  <a name="cfn-dms-endpoint-postgresqlsettings-slotname"></a>
Sets the name of a previously created logical replication slot for a change data capture \(CDC\) load of the PostgreSQL source instance\.   
When used with the `CdcStartPosition` request parameter for the AWS DMS API , this attribute also makes it possible to use native CDC start points\. DMS verifies that the specified logical replication slot exists before starting the CDC load task\. It also verifies that the task was created with a valid setting of `CdcStartPosition`\. If the specified slot doesn't exist or the task doesn't have a valid `CdcStartPosition` setting, DMS raises an error\.  
For more information about setting the `CdcStartPosition` request parameter, see [Determining a CDC native start point](dms/latest/userguide/CHAP_Task.CDC.html#CHAP_Task.CDC.StartPoint.Native) in the * AWS Database Migration Service User Guide*\. For more information about using `CdcStartPosition`, see [CreateReplicationTask](https://docs.aws.amazon.com/dms/latest/APIReference/API_CreateReplicationTask.html), [StartReplicationTask](https://docs.aws.amazon.com/dms/latest/APIReference/API_StartReplicationTask.html), and [ModifyReplicationTask](https://docs.aws.amazon.com/dms/latest/APIReference/API_ModifyReplicationTask.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)