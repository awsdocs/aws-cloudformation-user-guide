# AWS::DMS::Endpoint OracleSettings<a name="aws-properties-dms-endpoint-oraclesettings"></a>

Provides information that defines an Oracle endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For information about other available settings, see [ Extra connection attributes when using Oracle as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.ConnectionAttrib) and [ Extra connection attributes when using Oracle as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Oracle.html#CHAP_Target.Oracle.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-oraclesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-oraclesettings-syntax.json"></a>

```
{
  "[AccessAlternateDirectly](#cfn-dms-endpoint-oraclesettings-accessalternatedirectly)" : Boolean,
  "[AdditionalArchivedLogDestId](#cfn-dms-endpoint-oraclesettings-additionalarchivedlogdestid)" : Integer,
  "[AddSupplementalLogging](#cfn-dms-endpoint-oraclesettings-addsupplementallogging)" : Boolean,
  "[AllowSelectNestedTables](#cfn-dms-endpoint-oraclesettings-allowselectnestedtables)" : Boolean,
  "[ArchivedLogDestId](#cfn-dms-endpoint-oraclesettings-archivedlogdestid)" : Integer,
  "[ArchivedLogsOnly](#cfn-dms-endpoint-oraclesettings-archivedlogsonly)" : Boolean,
  "[AsmPassword](#cfn-dms-endpoint-oraclesettings-asmpassword)" : String,
  "[AsmServer](#cfn-dms-endpoint-oraclesettings-asmserver)" : String,
  "[AsmUser](#cfn-dms-endpoint-oraclesettings-asmuser)" : String,
  "[CharLengthSemantics](#cfn-dms-endpoint-oraclesettings-charlengthsemantics)" : String,
  "[DirectPathNoLog](#cfn-dms-endpoint-oraclesettings-directpathnolog)" : Boolean,
  "[DirectPathParallelLoad](#cfn-dms-endpoint-oraclesettings-directpathparallelload)" : Boolean,
  "[EnableHomogenousTablespace](#cfn-dms-endpoint-oraclesettings-enablehomogenoustablespace)" : Boolean,
  "[ExtraArchivedLogDestIds](#cfn-dms-endpoint-oraclesettings-extraarchivedlogdestids)" : [ Integer, ... ],
  "[FailTasksOnLobTruncation](#cfn-dms-endpoint-oraclesettings-failtasksonlobtruncation)" : Boolean,
  "[NumberDatatypeScale](#cfn-dms-endpoint-oraclesettings-numberdatatypescale)" : Integer,
  "[OraclePathPrefix](#cfn-dms-endpoint-oraclesettings-oraclepathprefix)" : String,
  "[ParallelAsmReadThreads](#cfn-dms-endpoint-oraclesettings-parallelasmreadthreads)" : Integer,
  "[ReadAheadBlocks](#cfn-dms-endpoint-oraclesettings-readaheadblocks)" : Integer,
  "[ReadTableSpaceName](#cfn-dms-endpoint-oraclesettings-readtablespacename)" : Boolean,
  "[ReplacePathPrefix](#cfn-dms-endpoint-oraclesettings-replacepathprefix)" : Boolean,
  "[RetryInterval](#cfn-dms-endpoint-oraclesettings-retryinterval)" : Integer,
  "[SecretsManagerAccessRoleArn](#cfn-dms-endpoint-oraclesettings-secretsmanageraccessrolearn)" : String,
  "[SecretsManagerOracleAsmAccessRoleArn](#cfn-dms-endpoint-oraclesettings-secretsmanageroracleasmaccessrolearn)" : String,
  "[SecretsManagerOracleAsmSecretId](#cfn-dms-endpoint-oraclesettings-secretsmanageroracleasmsecretid)" : String,
  "[SecretsManagerSecretId](#cfn-dms-endpoint-oraclesettings-secretsmanagersecretid)" : String,
  "[SecurityDbEncryption](#cfn-dms-endpoint-oraclesettings-securitydbencryption)" : String,
  "[SecurityDbEncryptionName](#cfn-dms-endpoint-oraclesettings-securitydbencryptionname)" : String,
  "[SpatialDataOptionToGeoJsonFunctionName](#cfn-dms-endpoint-oraclesettings-spatialdataoptiontogeojsonfunctionname)" : String,
  "[StandbyDelayTime](#cfn-dms-endpoint-oraclesettings-standbydelaytime)" : Integer,
  "[UseAlternateFolderForOnline](#cfn-dms-endpoint-oraclesettings-usealternatefolderforonline)" : Boolean,
  "[UseBFile](#cfn-dms-endpoint-oraclesettings-usebfile)" : Boolean,
  "[UseDirectPathFullLoad](#cfn-dms-endpoint-oraclesettings-usedirectpathfullload)" : Boolean,
  "[UseLogminerReader](#cfn-dms-endpoint-oraclesettings-uselogminerreader)" : Boolean,
  "[UsePathPrefix](#cfn-dms-endpoint-oraclesettings-usepathprefix)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-oraclesettings-syntax.yaml"></a>

```
  [AccessAlternateDirectly](#cfn-dms-endpoint-oraclesettings-accessalternatedirectly): Boolean
  [AdditionalArchivedLogDestId](#cfn-dms-endpoint-oraclesettings-additionalarchivedlogdestid): Integer
  [AddSupplementalLogging](#cfn-dms-endpoint-oraclesettings-addsupplementallogging): Boolean
  [AllowSelectNestedTables](#cfn-dms-endpoint-oraclesettings-allowselectnestedtables): Boolean
  [ArchivedLogDestId](#cfn-dms-endpoint-oraclesettings-archivedlogdestid): Integer
  [ArchivedLogsOnly](#cfn-dms-endpoint-oraclesettings-archivedlogsonly): Boolean
  [AsmPassword](#cfn-dms-endpoint-oraclesettings-asmpassword): String
  [AsmServer](#cfn-dms-endpoint-oraclesettings-asmserver): String
  [AsmUser](#cfn-dms-endpoint-oraclesettings-asmuser): String
  [CharLengthSemantics](#cfn-dms-endpoint-oraclesettings-charlengthsemantics): String
  [DirectPathNoLog](#cfn-dms-endpoint-oraclesettings-directpathnolog): Boolean
  [DirectPathParallelLoad](#cfn-dms-endpoint-oraclesettings-directpathparallelload): Boolean
  [EnableHomogenousTablespace](#cfn-dms-endpoint-oraclesettings-enablehomogenoustablespace): Boolean
  [ExtraArchivedLogDestIds](#cfn-dms-endpoint-oraclesettings-extraarchivedlogdestids): 
    - Integer
  [FailTasksOnLobTruncation](#cfn-dms-endpoint-oraclesettings-failtasksonlobtruncation): Boolean
  [NumberDatatypeScale](#cfn-dms-endpoint-oraclesettings-numberdatatypescale): Integer
  [OraclePathPrefix](#cfn-dms-endpoint-oraclesettings-oraclepathprefix): String
  [ParallelAsmReadThreads](#cfn-dms-endpoint-oraclesettings-parallelasmreadthreads): Integer
  [ReadAheadBlocks](#cfn-dms-endpoint-oraclesettings-readaheadblocks): Integer
  [ReadTableSpaceName](#cfn-dms-endpoint-oraclesettings-readtablespacename): Boolean
  [ReplacePathPrefix](#cfn-dms-endpoint-oraclesettings-replacepathprefix): Boolean
  [RetryInterval](#cfn-dms-endpoint-oraclesettings-retryinterval): Integer
  [SecretsManagerAccessRoleArn](#cfn-dms-endpoint-oraclesettings-secretsmanageraccessrolearn): String
  [SecretsManagerOracleAsmAccessRoleArn](#cfn-dms-endpoint-oraclesettings-secretsmanageroracleasmaccessrolearn): String
  [SecretsManagerOracleAsmSecretId](#cfn-dms-endpoint-oraclesettings-secretsmanageroracleasmsecretid): String
  [SecretsManagerSecretId](#cfn-dms-endpoint-oraclesettings-secretsmanagersecretid): String
  [SecurityDbEncryption](#cfn-dms-endpoint-oraclesettings-securitydbencryption): String
  [SecurityDbEncryptionName](#cfn-dms-endpoint-oraclesettings-securitydbencryptionname): String
  [SpatialDataOptionToGeoJsonFunctionName](#cfn-dms-endpoint-oraclesettings-spatialdataoptiontogeojsonfunctionname): String
  [StandbyDelayTime](#cfn-dms-endpoint-oraclesettings-standbydelaytime): Integer
  [UseAlternateFolderForOnline](#cfn-dms-endpoint-oraclesettings-usealternatefolderforonline): Boolean
  [UseBFile](#cfn-dms-endpoint-oraclesettings-usebfile): Boolean
  [UseDirectPathFullLoad](#cfn-dms-endpoint-oraclesettings-usedirectpathfullload): Boolean
  [UseLogminerReader](#cfn-dms-endpoint-oraclesettings-uselogminerreader): Boolean
  [UsePathPrefix](#cfn-dms-endpoint-oraclesettings-usepathprefix): String
```

## Properties<a name="aws-properties-dms-endpoint-oraclesettings-properties"></a>

`AccessAlternateDirectly`  <a name="cfn-dms-endpoint-oraclesettings-accessalternatedirectly"></a>
Set this attribute to `false` in order to use the Binary Reader to capture change data for an Amazon RDS for Oracle as the source\. This tells the DMS instance to not access redo logs through any specified path prefix replacement using direct file access\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdditionalArchivedLogDestId`  <a name="cfn-dms-endpoint-oraclesettings-additionalarchivedlogdestid"></a>
Set this attribute with `ArchivedLogDestId` in a primary/ standby setup\. This attribute is useful in the case of a switchover\. In this case, AWS DMS needs to know which destination to get archive redo logs from to read changes\. This need arises because the previous primary instance is now a standby instance after switchover\.  
Although AWS DMS supports the use of the Oracle `RESETLOGS` option to open the database, never use `RESETLOGS` unless necessary\. For additional information about `RESETLOGS`, see [RMAN Data Repair Concepts](https://docs.oracle.com/en/database/oracle/oracle-database/19/bradv/rman-data-repair-concepts.html#GUID-1805CCF7-4AF2-482D-B65A-998192F89C2B) in the *Oracle Database Backup and Recovery User's Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AddSupplementalLogging`  <a name="cfn-dms-endpoint-oraclesettings-addsupplementallogging"></a>
Set this attribute to set up table\-level supplemental logging for the Oracle database\. This attribute enables PRIMARY KEY supplemental logging on all tables selected for a migration task\.  
If you use this option, you still need to enable database\-level supplemental logging\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowSelectNestedTables`  <a name="cfn-dms-endpoint-oraclesettings-allowselectnestedtables"></a>
Set this attribute to `true` to enable replication of Oracle tables containing columns that are nested tables or defined types\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ArchivedLogDestId`  <a name="cfn-dms-endpoint-oraclesettings-archivedlogdestid"></a>
Specifies the ID of the destination for the archived redo logs\. This value should be the same as a number in the dest\_id column of the v$archived\_log view\. If you work with an additional redo log destination, use the `AdditionalArchivedLogDestId` option to specify the additional destination ID\. Doing this improves performance by ensuring that the correct logs are accessed from the outset\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ArchivedLogsOnly`  <a name="cfn-dms-endpoint-oraclesettings-archivedlogsonly"></a>
When this field is set to `Y`, AWS DMS only accesses the archived redo logs\. If the archived redo logs are stored on Automatic Storage Management \(ASM\) only, the AWS DMS user account needs to be granted ASM privileges\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AsmPassword`  <a name="cfn-dms-endpoint-oraclesettings-asmpassword"></a>
For an Oracle source endpoint, your Oracle Automatic Storage Management \(ASM\) password\. You can set this value from the ` asm_user_password ` value\. You set this value as part of the comma\-separated value that you set to the `Password` request parameter when you create the endpoint to access transaction logs using Binary Reader\. For more information, see [Configuration for change data capture \(CDC\) on an Oracle source database](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.CDC.Configuration)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AsmServer`  <a name="cfn-dms-endpoint-oraclesettings-asmserver"></a>
For an Oracle source endpoint, your ASM server address\. You can set this value from the `asm_server` value\. You set `asm_server` as part of the extra connection attribute string to access an Oracle server with Binary Reader that uses ASM\. For more information, see [Configuration for change data capture \(CDC\) on an Oracle source database](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.CDC.Configuration)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AsmUser`  <a name="cfn-dms-endpoint-oraclesettings-asmuser"></a>
For an Oracle source endpoint, your ASM user name\. You can set this value from the `asm_user` value\. You set `asm_user` as part of the extra connection attribute string to access an Oracle server with Binary Reader that uses ASM\. For more information, see [Configuration for change data capture \(CDC\) on an Oracle source database](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.CDC.Configuration)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CharLengthSemantics`  <a name="cfn-dms-endpoint-oraclesettings-charlengthsemantics"></a>
Specifies whether the length of a character column is in bytes or in characters\. To indicate that the character column length is in characters, set this attribute to `CHAR`\. Otherwise, the character column length is in bytes\.  
Example: `charLengthSemantics=CHAR;`   
*Required*: No  
*Type*: String  
*Allowed values*: `byte | char | default`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DirectPathNoLog`  <a name="cfn-dms-endpoint-oraclesettings-directpathnolog"></a>
When set to `true`, this attribute helps to increase the commit rate on the Oracle target database by writing directly to tables and not writing a trail to database logs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DirectPathParallelLoad`  <a name="cfn-dms-endpoint-oraclesettings-directpathparallelload"></a>
When set to `true`, this attribute specifies a parallel load when `useDirectPathFullLoad` is set to `Y`\. This attribute also only applies when you use the AWS DMS parallel load feature\. Note that the target table cannot have any constraints or indexes\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableHomogenousTablespace`  <a name="cfn-dms-endpoint-oraclesettings-enablehomogenoustablespace"></a>
Set this attribute to enable homogenous tablespace replication and create existing tables or indexes under the same tablespace on the target\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExtraArchivedLogDestIds`  <a name="cfn-dms-endpoint-oraclesettings-extraarchivedlogdestids"></a>
Specifies the IDs of one more destinations for one or more archived redo logs\. These IDs are the values of the `dest_id` column in the `v$archived_log` view\. Use this setting with the `archivedLogDestId` extra connection attribute in a primary\-to\-single setup or a primary\-to\-multiple\-standby setup\.   
This setting is useful in a switchover when you use an Oracle Data Guard database as a source\. In this case, AWS DMS needs information about what destination to get archive redo logs from to read changes\. AWS DMS needs this because after the switchover the previous primary is a standby instance\. For example, in a primary\-to\-single standby setup you might apply the following settings\.   
 `archivedLogDestId=1; ExtraArchivedLogDestIds=[2]`   
In a primary\-to\-multiple\-standby setup, you might apply the following settings\.  
 `archivedLogDestId=1; ExtraArchivedLogDestIds=[2,3,4]`   
Although AWS DMS supports the use of the Oracle `RESETLOGS` option to open the database, never use `RESETLOGS` unless it's necessary\. For more information about `RESETLOGS`, see [ RMAN Data Repair Concepts](https://docs.oracle.com/en/database/oracle/oracle-database/19/bradv/rman-data-repair-concepts.html#GUID-1805CCF7-4AF2-482D-B65A-998192F89C2B) in the *Oracle Database Backup and Recovery User's Guide*\.  
*Required*: No  
*Type*: List of Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailTasksOnLobTruncation`  <a name="cfn-dms-endpoint-oraclesettings-failtasksonlobtruncation"></a>
When set to `true`, this attribute causes a task to fail if the actual size of an LOB column is greater than the specified `LobMaxSize`\.  
If a task is set to limited LOB mode and this option is set to `true`, the task fails instead of truncating the LOB data\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberDatatypeScale`  <a name="cfn-dms-endpoint-oraclesettings-numberdatatypescale"></a>
Specifies the number scale\. You can select a scale up to 38, or you can select FLOAT\. By default, the NUMBER data type is converted to precision 38, scale 10\.  
Example: `numberDataTypeScale=12`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OraclePathPrefix`  <a name="cfn-dms-endpoint-oraclesettings-oraclepathprefix"></a>
Set this string attribute to the required value in order to use the Binary Reader to capture change data for an Amazon RDS for Oracle as the source\. This value specifies the default Oracle root used to access the redo logs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParallelAsmReadThreads`  <a name="cfn-dms-endpoint-oraclesettings-parallelasmreadthreads"></a>
Set this attribute to change the number of threads that DMS configures to perform a change data capture \(CDC\) load using Oracle Automatic Storage Management \(ASM\)\. You can specify an integer value between 2 \(the default\) and 8 \(the maximum\)\. Use this attribute together with the `readAheadBlocks` attribute\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadAheadBlocks`  <a name="cfn-dms-endpoint-oraclesettings-readaheadblocks"></a>
Set this attribute to change the number of read\-ahead blocks that DMS configures to perform a change data capture \(CDC\) load using Oracle Automatic Storage Management \(ASM\)\. You can specify an integer value between 1000 \(the default\) and 200,000 \(the maximum\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadTableSpaceName`  <a name="cfn-dms-endpoint-oraclesettings-readtablespacename"></a>
When set to `true`, this attribute supports tablespace replication\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplacePathPrefix`  <a name="cfn-dms-endpoint-oraclesettings-replacepathprefix"></a>
Set this attribute to true in order to use the Binary Reader to capture change data for an Amazon RDS for Oracle as the source\. This setting tells DMS instance to replace the default Oracle root with the specified `usePathPrefix` setting to access the redo logs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryInterval`  <a name="cfn-dms-endpoint-oraclesettings-retryinterval"></a>
Specifies the number of seconds that the system waits before resending a query\.  
Example: `retryInterval=6;`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerAccessRoleArn`  <a name="cfn-dms-endpoint-oraclesettings-secretsmanageraccessrolearn"></a>
The full Amazon Resource Name \(ARN\) of the IAM role that specifies AWS DMS as the trusted entity and grants the required permissions to access the value in `SecretsManagerSecret`\. The role must allow the `iam:PassRole` action\. `SecretsManagerSecret` has the value of the AWS Secrets Manager secret that allows access to the Oracle endpoint\.  
You can specify one of two sets of values for these permissions\. You can specify the values for this setting and `SecretsManagerSecretId`\. Or you can specify clear\-text values for `UserName`, `Password`, `ServerName`, and `Port`\. You can't specify both\.  
For more information on creating this `SecretsManagerSecret`, the corresponding `SecretsManagerAccessRoleArn`, and the `SecretsManagerSecretId` that is required to access it, see [ Using secrets to access AWS Database Migration Service resources](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.html#security-iam-secretsmanager) in the *AWS Database Migration Service User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerOracleAsmAccessRoleArn`  <a name="cfn-dms-endpoint-oraclesettings-secretsmanageroracleasmaccessrolearn"></a>
Required only if your Oracle endpoint uses Advanced Storage Manager \(ASM\)\. The full ARN of the IAM role that specifies AWS DMS as the trusted entity and grants the required permissions to access the `SecretsManagerOracleAsmSecret`\. This `SecretsManagerOracleAsmSecret` has the secret value that allows access to the Oracle ASM of the endpoint\.  
You can specify one of two sets of values for these permissions\. You can specify the values for this setting and `SecretsManagerOracleAsmSecretId`\. Or you can specify clear\-text values for `AsmUserName`, `AsmPassword`, and `AsmServerName`\. You can't specify both\.  
For more information on creating this `SecretsManagerOracleAsmSecret`, the corresponding `SecretsManagerOracleAsmAccessRoleArn`, and the `SecretsManagerOracleAsmSecretId` that is required to access it, see [ Using secrets to access AWS Database Migration Service resources](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.html#security-iam-secretsmanager) in the *AWS Database Migration Service User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerOracleAsmSecretId`  <a name="cfn-dms-endpoint-oraclesettings-secretsmanageroracleasmsecretid"></a>
Required only if your Oracle endpoint uses Advanced Storage Manager \(ASM\)\. The full ARN, partial ARN, or display name of the `SecretsManagerOracleAsmSecret` that contains the Oracle ASM connection details for the Oracle endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerSecretId`  <a name="cfn-dms-endpoint-oraclesettings-secretsmanagersecretid"></a>
The full ARN, partial ARN, or display name of the `SecretsManagerSecret` that contains the Oracle endpoint connection details\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityDbEncryption`  <a name="cfn-dms-endpoint-oraclesettings-securitydbencryption"></a>
For an Oracle source endpoint, the transparent data encryption \(TDE\) password required by AWM DMS to access Oracle redo logs encrypted by TDE using Binary Reader\. It is also the ` TDE_Password ` part of the comma\-separated value you set to the `Password` request parameter when you create the endpoint\. The `SecurityDbEncryptian` setting is related to this `SecurityDbEncryptionName` setting\. For more information, see [ Supported encryption methods for using Oracle as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.Encryption) in the * AWS Database Migration Service User Guide*\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityDbEncryptionName`  <a name="cfn-dms-endpoint-oraclesettings-securitydbencryptionname"></a>
For an Oracle source endpoint, the name of a key used for the transparent data encryption \(TDE\) of the columns and tablespaces in an Oracle source database that is encrypted using TDE\. The key value is the value of the `SecurityDbEncryption` setting\. For more information on setting the key name value of `SecurityDbEncryptionName`, see the information and example for setting the `securityDbEncryptionName` extra connection attribute in [ Supported encryption methods for using Oracle as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.Encryption) in the * AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpatialDataOptionToGeoJsonFunctionName`  <a name="cfn-dms-endpoint-oraclesettings-spatialdataoptiontogeojsonfunctionname"></a>
Use this attribute to convert `SDO_GEOMETRY` to `GEOJSON` format\. By default, DMS calls the `SDO2GEOJSON` custom function if present and accessible\. Or you can create your own custom function that mimics the operation of `SDOGEOJSON` and set `SpatialDataOptionToGeoJsonFunctionName` to call it instead\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StandbyDelayTime`  <a name="cfn-dms-endpoint-oraclesettings-standbydelaytime"></a>
Use this attribute to specify a time in minutes for the delay in standby sync\. If the source is an Oracle Active Data Guard standby database, use this attribute to specify the time lag between primary and standby databases\.  
In AWS DMS, you can create an Oracle CDC task that uses an Active Data Guard standby instance as a source for replicating ongoing changes\. Doing this eliminates the need to connect to an active database that might be in production\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseAlternateFolderForOnline`  <a name="cfn-dms-endpoint-oraclesettings-usealternatefolderforonline"></a>
Set this attribute to `true` in order to use the Binary Reader to capture change data for an Amazon RDS for Oracle as the source\. This tells the DMS instance to use any specified prefix replacement to access all online redo logs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseBFile`  <a name="cfn-dms-endpoint-oraclesettings-usebfile"></a>
Set this attribute to Y to capture change data using the Binary Reader utility\. Set `UseLogminerReader` to N to set this attribute to Y\. To use Binary Reader with Amazon RDS for Oracle as the source, you set additional attributes\. For more information about using this setting with Oracle Automatic Storage Management \(ASM\), see [ Using Oracle LogMiner or AWS DMS Binary Reader for CDC](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.CDC)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseDirectPathFullLoad`  <a name="cfn-dms-endpoint-oraclesettings-usedirectpathfullload"></a>
Set this attribute to Y to have AWS DMS use a direct path full load\. Specify this value to use the direct path protocol in the Oracle Call Interface \(OCI\)\. By using this OCI protocol, you can bulk\-load Oracle target tables during a full load\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseLogminerReader`  <a name="cfn-dms-endpoint-oraclesettings-uselogminerreader"></a>
Set this attribute to Y to capture change data using the Oracle LogMiner utility \(the default\)\. Set this attribute to N if you want to access the redo logs as a binary file\. When you set `UseLogminerReader` to N, also set `UseBfile` to Y\. For more information on this setting and using Oracle ASM, see [ Using Oracle LogMiner or AWS DMS Binary Reader for CDC](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.CDC) in the * AWS DMS User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UsePathPrefix`  <a name="cfn-dms-endpoint-oraclesettings-usepathprefix"></a>
Set this string attribute to the required value in order to use the Binary Reader to capture change data for an Amazon RDS for Oracle as the source\. This value specifies the path prefix used to replace the default Oracle root to access the redo logs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)