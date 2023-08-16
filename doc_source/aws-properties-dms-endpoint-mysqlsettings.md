# AWS::DMS::Endpoint MySqlSettings<a name="aws-properties-dms-endpoint-mysqlsettings"></a>

Provides information that defines a MySQL endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For information about other available settings, see [ Extra connection attributes when using MySQL as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MySQL.html#CHAP_Source.MySQL.ConnectionAttrib) and [ Extra connection attributes when using a MySQL\-compatible database as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.MySQL.html#CHAP_Target.MySQL.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-mysqlsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-mysqlsettings-syntax.json"></a>

```
{
  "[AfterConnectScript](#cfn-dms-endpoint-mysqlsettings-afterconnectscript)" : String,
  "[CleanSourceMetadataOnMismatch](#cfn-dms-endpoint-mysqlsettings-cleansourcemetadataonmismatch)" : Boolean,
  "[EventsPollInterval](#cfn-dms-endpoint-mysqlsettings-eventspollinterval)" : Integer,
  "[MaxFileSize](#cfn-dms-endpoint-mysqlsettings-maxfilesize)" : Integer,
  "[ParallelLoadThreads](#cfn-dms-endpoint-mysqlsettings-parallelloadthreads)" : Integer,
  "[SecretsManagerAccessRoleArn](#cfn-dms-endpoint-mysqlsettings-secretsmanageraccessrolearn)" : String,
  "[SecretsManagerSecretId](#cfn-dms-endpoint-mysqlsettings-secretsmanagersecretid)" : String,
  "[ServerTimezone](#cfn-dms-endpoint-mysqlsettings-servertimezone)" : String,
  "[TargetDbType](#cfn-dms-endpoint-mysqlsettings-targetdbtype)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-mysqlsettings-syntax.yaml"></a>

```
  [AfterConnectScript](#cfn-dms-endpoint-mysqlsettings-afterconnectscript): String
  [CleanSourceMetadataOnMismatch](#cfn-dms-endpoint-mysqlsettings-cleansourcemetadataonmismatch): Boolean
  [EventsPollInterval](#cfn-dms-endpoint-mysqlsettings-eventspollinterval): Integer
  [MaxFileSize](#cfn-dms-endpoint-mysqlsettings-maxfilesize): Integer
  [ParallelLoadThreads](#cfn-dms-endpoint-mysqlsettings-parallelloadthreads): Integer
  [SecretsManagerAccessRoleArn](#cfn-dms-endpoint-mysqlsettings-secretsmanageraccessrolearn): String
  [SecretsManagerSecretId](#cfn-dms-endpoint-mysqlsettings-secretsmanagersecretid): String
  [ServerTimezone](#cfn-dms-endpoint-mysqlsettings-servertimezone): String
  [TargetDbType](#cfn-dms-endpoint-mysqlsettings-targetdbtype): String
```

## Properties<a name="aws-properties-dms-endpoint-mysqlsettings-properties"></a>

`AfterConnectScript`  <a name="cfn-dms-endpoint-mysqlsettings-afterconnectscript"></a>
Specifies a script to run immediately after AWS DMS connects to the endpoint\. The migration task continues running regardless if the SQL statement succeeds or fails\.  
For this parameter, provide the code of the script itself, not the name of a file containing the script\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CleanSourceMetadataOnMismatch`  <a name="cfn-dms-endpoint-mysqlsettings-cleansourcemetadataonmismatch"></a>
Cleans and recreates table metadata information on the replication instance when a mismatch occurs\. For example, in a situation where running an alter DDL on the table could result in different information about the table cached in the replication instance\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventsPollInterval`  <a name="cfn-dms-endpoint-mysqlsettings-eventspollinterval"></a>
Specifies how often to check the binary log for new changes/events when the database is idle\. The default is five seconds\.  
Example: `eventsPollInterval=5;`   
In the example, AWS DMS checks for changes in the binary logs every five seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxFileSize`  <a name="cfn-dms-endpoint-mysqlsettings-maxfilesize"></a>
Specifies the maximum size \(in KB\) of any \.csv file used to transfer data to a MySQL\-compatible database\.  
Example: `maxFileSize=512`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParallelLoadThreads`  <a name="cfn-dms-endpoint-mysqlsettings-parallelloadthreads"></a>
Improves performance when loading data into the MySQL\-compatible target database\. Specifies how many threads to use to load the data into the MySQL\-compatible target database\. Setting a large number of threads can have an adverse effect on database performance, because a separate connection is required for each thread\. The default is one\.  
Example: `parallelLoadThreads=1`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerAccessRoleArn`  <a name="cfn-dms-endpoint-mysqlsettings-secretsmanageraccessrolearn"></a>
The full Amazon Resource Name \(ARN\) of the IAM role that specifies AWS DMS as the trusted entity and grants the required permissions to access the value in `SecretsManagerSecret`\. The role must allow the `iam:PassRole` action\. `SecretsManagerSecret` has the value of the AWS Secrets Manager secret that allows access to the MySQL endpoint\.  
You can specify one of two sets of values for these permissions\. You can specify the values for this setting and `SecretsManagerSecretId`\. Or you can specify clear\-text values for `UserName`, `Password`, `ServerName`, and `Port`\. You can't specify both\.  
For more information on creating this `SecretsManagerSecret`, the corresponding `SecretsManagerAccessRoleArn`, and the `SecretsManagerSecretId` that is required to access it, see [ Using secrets to access AWS Database Migration Service resources](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.html#security-iam-secretsmanager) in the *AWS Database Migration Service User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerSecretId`  <a name="cfn-dms-endpoint-mysqlsettings-secretsmanagersecretid"></a>
The full ARN, partial ARN, or display name of the `SecretsManagerSecret` that contains the MySQL endpoint connection details\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerTimezone`  <a name="cfn-dms-endpoint-mysqlsettings-servertimezone"></a>
Specifies the time zone for the source MySQL database\.  
Example: `serverTimezone=US/Pacific;`   
Note: Do not enclose time zones in single quotes\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetDbType`  <a name="cfn-dms-endpoint-mysqlsettings-targetdbtype"></a>
Specifies where to migrate source tables on the target, either to a single database or multiple databases\. If you specify `SPECIFIC_DATABASE`, specify the database name using the `DatabaseName` parameter of the `Endpoint` object\.  
Example: `targetDbType=MULTIPLE_DATABASES`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)