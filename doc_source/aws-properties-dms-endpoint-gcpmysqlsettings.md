# AWS::DMS::Endpoint GcpMySQLSettings<a name="aws-properties-dms-endpoint-gcpmysqlsettings"></a>

Provides information that defines a GCP MySQL endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. These settings are much the same as the settings for any MySQL\-compatible endpoint\. For more information, see [ Extra connection attributes when using MySQL as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MySQL.html#CHAP_Source.MySQL.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-gcpmysqlsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-gcpmysqlsettings-syntax.json"></a>

```
{
  "[AfterConnectScript](#cfn-dms-endpoint-gcpmysqlsettings-afterconnectscript)" : String,
  "[CleanSourceMetadataOnMismatch](#cfn-dms-endpoint-gcpmysqlsettings-cleansourcemetadataonmismatch)" : Boolean,
  "[DatabaseName](#cfn-dms-endpoint-gcpmysqlsettings-databasename)" : String,
  "[EventsPollInterval](#cfn-dms-endpoint-gcpmysqlsettings-eventspollinterval)" : Integer,
  "[MaxFileSize](#cfn-dms-endpoint-gcpmysqlsettings-maxfilesize)" : Integer,
  "[ParallelLoadThreads](#cfn-dms-endpoint-gcpmysqlsettings-parallelloadthreads)" : Integer,
  "[Password](#cfn-dms-endpoint-gcpmysqlsettings-password)" : String,
  "[Port](#cfn-dms-endpoint-gcpmysqlsettings-port)" : Integer,
  "[SecretsManagerAccessRoleArn](#cfn-dms-endpoint-gcpmysqlsettings-secretsmanageraccessrolearn)" : String,
  "[SecretsManagerSecretId](#cfn-dms-endpoint-gcpmysqlsettings-secretsmanagersecretid)" : String,
  "[ServerName](#cfn-dms-endpoint-gcpmysqlsettings-servername)" : String,
  "[ServerTimezone](#cfn-dms-endpoint-gcpmysqlsettings-servertimezone)" : String,
  "[Username](#cfn-dms-endpoint-gcpmysqlsettings-username)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-gcpmysqlsettings-syntax.yaml"></a>

```
  [AfterConnectScript](#cfn-dms-endpoint-gcpmysqlsettings-afterconnectscript): String
  [CleanSourceMetadataOnMismatch](#cfn-dms-endpoint-gcpmysqlsettings-cleansourcemetadataonmismatch): Boolean
  [DatabaseName](#cfn-dms-endpoint-gcpmysqlsettings-databasename): String
  [EventsPollInterval](#cfn-dms-endpoint-gcpmysqlsettings-eventspollinterval): Integer
  [MaxFileSize](#cfn-dms-endpoint-gcpmysqlsettings-maxfilesize): Integer
  [ParallelLoadThreads](#cfn-dms-endpoint-gcpmysqlsettings-parallelloadthreads): Integer
  [Password](#cfn-dms-endpoint-gcpmysqlsettings-password): String
  [Port](#cfn-dms-endpoint-gcpmysqlsettings-port): Integer
  [SecretsManagerAccessRoleArn](#cfn-dms-endpoint-gcpmysqlsettings-secretsmanageraccessrolearn): String
  [SecretsManagerSecretId](#cfn-dms-endpoint-gcpmysqlsettings-secretsmanagersecretid): String
  [ServerName](#cfn-dms-endpoint-gcpmysqlsettings-servername): String
  [ServerTimezone](#cfn-dms-endpoint-gcpmysqlsettings-servertimezone): String
  [Username](#cfn-dms-endpoint-gcpmysqlsettings-username): String
```

## Properties<a name="aws-properties-dms-endpoint-gcpmysqlsettings-properties"></a>

`AfterConnectScript`  <a name="cfn-dms-endpoint-gcpmysqlsettings-afterconnectscript"></a>
Specifies a script to run immediately after AWS DMS connects to the endpoint\. The migration task continues running regardless if the SQL statement succeeds or fails\.  
For this parameter, provide the code of the script itself, not the name of a file containing the script\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CleanSourceMetadataOnMismatch`  <a name="cfn-dms-endpoint-gcpmysqlsettings-cleansourcemetadataonmismatch"></a>
Adjusts the behavior of AWS DMS when migrating from an SQL Server source database that is hosted as part of an Always On availability group cluster\. If you need AWS DMS to poll all the nodes in the Always On cluster for transaction backups, set this attribute to `false`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-dms-endpoint-gcpmysqlsettings-databasename"></a>
Database name for the endpoint\. For a MySQL source or target endpoint, don't explicitly specify the database using the `DatabaseName` request parameter on either the `CreateEndpoint` or `ModifyEndpoint` API call\. Specifying `DatabaseName` when you create or modify a MySQL endpoint replicates all the task tables to this single database\. For MySQL endpoints, you specify the database only when you specify the schema in the table\-mapping rules of the AWS DMS task\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventsPollInterval`  <a name="cfn-dms-endpoint-gcpmysqlsettings-eventspollinterval"></a>
Specifies how often to check the binary log for new changes/events when the database is idle\. The default is five seconds\.  
Example: `eventsPollInterval=5;`   
In the example, AWS DMS checks for changes in the binary logs every five seconds\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxFileSize`  <a name="cfn-dms-endpoint-gcpmysqlsettings-maxfilesize"></a>
Specifies the maximum size \(in KB\) of any \.csv file used to transfer data to a MySQL\-compatible database\.  
Example: `maxFileSize=512`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParallelLoadThreads`  <a name="cfn-dms-endpoint-gcpmysqlsettings-parallelloadthreads"></a>
Improves performance when loading data into the MySQL\-compatible target database\. Specifies how many threads to use to load the data into the MySQL\-compatible target database\. Setting a large number of threads can have an adverse effect on database performance, because a separate connection is required for each thread\. The default is one\.  
Example: `parallelLoadThreads=1`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-dms-endpoint-gcpmysqlsettings-password"></a>
Endpoint connection password\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-dms-endpoint-gcpmysqlsettings-port"></a>
The port used by the endpoint database\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerAccessRoleArn`  <a name="cfn-dms-endpoint-gcpmysqlsettings-secretsmanageraccessrolearn"></a>
The full Amazon Resource Name \(ARN\) of the IAM role that specifies AWS DMS as the trusted entity and grants the required permissions to access the value in `SecretsManagerSecret.` The role must allow the `iam:PassRole` action\. `SecretsManagerSecret` has the value of the AWS Secrets Manager secret that allows access to the MySQL endpoint\.  
You can specify one of two sets of values for these permissions\. You can specify the values for this setting and `SecretsManagerSecretId`\. Or you can specify clear\-text values for `UserName`, `Password`, `ServerName`, and `Port`\. You can't specify both\.  
For more information on creating this `SecretsManagerSecret`, the corresponding `SecretsManagerAccessRoleArn`, and the `SecretsManagerSecretId` required to access it, see [ Using secrets to access AWS Database Migration Service resources](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.html#security-iam-secretsmanager) in the *AWS Database Migration Service User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerSecretId`  <a name="cfn-dms-endpoint-gcpmysqlsettings-secretsmanagersecretid"></a>
The full ARN, partial ARN, or display name of the `SecretsManagerSecret` that contains the MySQL endpoint connection details\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerName`  <a name="cfn-dms-endpoint-gcpmysqlsettings-servername"></a>
Endpoint TCP port\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerTimezone`  <a name="cfn-dms-endpoint-gcpmysqlsettings-servertimezone"></a>
Specifies the time zone for the source MySQL database\. Don't enclose time zones in single quotation marks\.  
Example: `serverTimezone=US/Pacific;`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-dms-endpoint-gcpmysqlsettings-username"></a>
Endpoint connection user name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)