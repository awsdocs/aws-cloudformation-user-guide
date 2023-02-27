# AWS::DMS::Endpoint MicrosoftSqlServerSettings<a name="aws-properties-dms-endpoint-microsoftsqlserversettings"></a>

Provides information that defines a Microsoft SQL Server endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For information about other available settings, see [ Extra connection attributes when using SQL Server as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.SQLServer.html#CHAP_Source.SQLServer.ConnectionAttrib) and [ Extra connection attributes when using SQL Server as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.SQLServer.html#CHAP_Target.SQLServer.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-microsoftsqlserversettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-microsoftsqlserversettings-syntax.json"></a>

```
{
  "[BcpPacketSize](#cfn-dms-endpoint-microsoftsqlserversettings-bcppacketsize)" : Integer,
  "[ControlTablesFileGroup](#cfn-dms-endpoint-microsoftsqlserversettings-controltablesfilegroup)" : String,
  "[QuerySingleAlwaysOnNode](#cfn-dms-endpoint-microsoftsqlserversettings-querysinglealwaysonnode)" : Boolean,
  "[ReadBackupOnly](#cfn-dms-endpoint-microsoftsqlserversettings-readbackuponly)" : Boolean,
  "[SafeguardPolicy](#cfn-dms-endpoint-microsoftsqlserversettings-safeguardpolicy)" : String,
  "[SecretsManagerAccessRoleArn](#cfn-dms-endpoint-microsoftsqlserversettings-secretsmanageraccessrolearn)" : String,
  "[SecretsManagerSecretId](#cfn-dms-endpoint-microsoftsqlserversettings-secretsmanagersecretid)" : String,
  "[UseBcpFullLoad](#cfn-dms-endpoint-microsoftsqlserversettings-usebcpfullload)" : Boolean,
  "[UseThirdPartyBackupDevice](#cfn-dms-endpoint-microsoftsqlserversettings-usethirdpartybackupdevice)" : Boolean
}
```

### YAML<a name="aws-properties-dms-endpoint-microsoftsqlserversettings-syntax.yaml"></a>

```
  [BcpPacketSize](#cfn-dms-endpoint-microsoftsqlserversettings-bcppacketsize): Integer
  [ControlTablesFileGroup](#cfn-dms-endpoint-microsoftsqlserversettings-controltablesfilegroup): String
  [QuerySingleAlwaysOnNode](#cfn-dms-endpoint-microsoftsqlserversettings-querysinglealwaysonnode): Boolean
  [ReadBackupOnly](#cfn-dms-endpoint-microsoftsqlserversettings-readbackuponly): Boolean
  [SafeguardPolicy](#cfn-dms-endpoint-microsoftsqlserversettings-safeguardpolicy): String
  [SecretsManagerAccessRoleArn](#cfn-dms-endpoint-microsoftsqlserversettings-secretsmanageraccessrolearn): String
  [SecretsManagerSecretId](#cfn-dms-endpoint-microsoftsqlserversettings-secretsmanagersecretid): String
  [UseBcpFullLoad](#cfn-dms-endpoint-microsoftsqlserversettings-usebcpfullload): Boolean
  [UseThirdPartyBackupDevice](#cfn-dms-endpoint-microsoftsqlserversettings-usethirdpartybackupdevice): Boolean
```

## Properties<a name="aws-properties-dms-endpoint-microsoftsqlserversettings-properties"></a>

`BcpPacketSize`  <a name="cfn-dms-endpoint-microsoftsqlserversettings-bcppacketsize"></a>
The maximum size of the packets \(in bytes\) used to transfer data using BCP\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ControlTablesFileGroup`  <a name="cfn-dms-endpoint-microsoftsqlserversettings-controltablesfilegroup"></a>
Specifies a file group for the AWS DMS internal tables\. When the replication task starts, all the internal AWS DMS control tables \(awsdms\_ apply\_exception, awsdms\_apply, awsdms\_changes\) are created for the specified file group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QuerySingleAlwaysOnNode`  <a name="cfn-dms-endpoint-microsoftsqlserversettings-querysinglealwaysonnode"></a>
Cleans and recreates table metadata information on the replication instance when a mismatch occurs\. An example is a situation where running an alter DDL statement on a table might result in different information about the table cached in the replication instance\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadBackupOnly`  <a name="cfn-dms-endpoint-microsoftsqlserversettings-readbackuponly"></a>
When this attribute is set to `Y`, AWS DMS only reads changes from transaction log backups and doesn't read from the active transaction log file during ongoing replication\. Setting this parameter to `Y` enables you to control active transaction log file growth during full load and ongoing replication tasks\. However, it can add some source latency to ongoing replication\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SafeguardPolicy`  <a name="cfn-dms-endpoint-microsoftsqlserversettings-safeguardpolicy"></a>
Use this attribute to minimize the need to access the backup log and enable AWS DMS to prevent truncation using one of the following two methods\.  
 *Start transactions in the database:* This is the default method\. When this method is used, AWS DMS prevents TLOG truncation by mimicking a transaction in the database\. As long as such a transaction is open, changes that appear after the transaction started aren't truncated\. If you need Microsoft Replication to be enabled in your database, then you must choose this method\.  
 *Exclusively use sp\_repldone within a single task*: When this method is used, AWS DMS reads the changes and then uses sp\_repldone to mark the TLOG transactions as ready for truncation\. Although this method doesn't involve any transactional activities, it can only be used when Microsoft Replication isn't running\. Also, when using this method, only one AWS DMS task can access the database at any given time\. Therefore, if you need to run parallel AWS DMS tasks against the same database, use the default method\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerAccessRoleArn`  <a name="cfn-dms-endpoint-microsoftsqlserversettings-secretsmanageraccessrolearn"></a>
The full Amazon Resource Name \(ARN\) of the IAM role that specifies AWS DMS as the trusted entity and grants the required permissions to access the value in `SecretsManagerSecret`\. The role must allow the `iam:PassRole` action\. `SecretsManagerSecret` has the value of the AWS Secrets Manager secret that allows access to the SQL Server endpoint\.  
You can specify one of two sets of values for these permissions\. You can specify the values for this setting and `SecretsManagerSecretId`\. Or you can specify clear\-text values for `UserName`, `Password`, `ServerName`, and `Port`\. You can't specify both\.  
For more information on creating this `SecretsManagerSecret`, the corresponding `SecretsManagerAccessRoleArn`, and the `SecretsManagerSecretId` that is required to access it, see [ Using secrets to access AWS Database Migration Service resources](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.html#security-iam-secretsmanager) in the *AWS Database Migration Service User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerSecretId`  <a name="cfn-dms-endpoint-microsoftsqlserversettings-secretsmanagersecretid"></a>
The full ARN, partial ARN, or display name of the `SecretsManagerSecret` that contains the MicrosoftSQLServer endpoint connection details\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseBcpFullLoad`  <a name="cfn-dms-endpoint-microsoftsqlserversettings-usebcpfullload"></a>
Use this to attribute to transfer data for full\-load operations using BCP\. When the target table contains an identity column that does not exist in the source table, you must disable the use BCP for loading table option\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseThirdPartyBackupDevice`  <a name="cfn-dms-endpoint-microsoftsqlserversettings-usethirdpartybackupdevice"></a>
When this attribute is set to `Y`, DMS processes third\-party transaction log backups if they are created in native format\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)