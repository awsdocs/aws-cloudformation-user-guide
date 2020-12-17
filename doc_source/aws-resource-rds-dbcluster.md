# AWS::RDS::DBCluster<a name="aws-resource-rds-dbcluster"></a>

The `AWS::RDS::DBCluster` resource creates an Amazon Aurora DB cluster\. For more information, see [Managing an Amazon Aurora DB Cluster](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_Aurora.html) in the *Amazon Aurora User Guide*\.

**Note**  
You can only create this resource in AWS Regions where Amazon Aurora is supported\.

**Updating DB clusters**

When properties labeled "*Update requires:* [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)" are updated, AWS CloudFormation first creates a replacement DB cluster, then changes references from other dependent resources to point to the replacement DB cluster, and finally deletes the old DB cluster\.

**Important**  
We highly recommend that you take a snapshot of the database before updating the stack\. If you don't, you lose the data when AWS CloudFormation replaces your DB cluster\. To preserve your data, perform the following procedure:  
Deactivate any applications that are using the DB cluster so that there's no activity on the DB instance\.
Create a snapshot of the DB cluster\. For more information about creating DB snapshots, see [Creating a DB Cluster Snapshot](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_CreateSnapshotCluster.html)\.
If you want to restore your DB cluster using a DB cluster snapshot, modify the updated template with your DB cluster changes and add the `SnapshotIdentifier` property with the ID of the DB cluster snapshot that you want to use\.  
After you restore a DB cluster with a `SnapshotIdentifier` property, you must specify the same `SnapshotIdentifier` property for any future updates to the DB cluster\. When you specify this property for an update, the DB cluster is not restored from the DB cluster snapshot again, and the data in the database is not changed\. However, if you don't specify the `SnapshotIdentifier` property, an empty DB cluster is created, and the original DB cluster is deleted\. If you specify a property that is different from the previous snapshot restore property, a new DB cluster is restored from the specified `SnapshotIdentifier` property, and the original DB cluster is deleted\.
Update the stack\.

For more information about updating other properties of this resource, see ` [ModifyDBCluster](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBCluster.html)`\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.

**Deleting DB clusters**

The default `DeletionPolicy` for `AWS::RDS::DBCluster` resources is `Snapshot`\. For more information about how AWS CloudFormation deletes resources, see [ DeletionPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.

## Syntax<a name="aws-resource-rds-dbcluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbcluster-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBCluster",
  "Properties" : {
      "[AssociatedRoles](#cfn-rds-dbcluster-associatedroles)" : [ DBClusterRole, ... ],
      "[AvailabilityZones](#cfn-rds-dbcluster-availabilityzones)" : [ String, ... ],
      "[BacktrackWindow](#cfn-rds-dbcluster-backtrackwindow)" : Long,
      "[BackupRetentionPeriod](#cfn-rds-dbcluster-backuprententionperiod)" : Integer,
      "[DatabaseName](#cfn-rds-dbcluster-databasename)" : String,
      "[DBClusterIdentifier](#cfn-rds-dbcluster-dbclusteridentifier)" : String,
      "[DBClusterParameterGroupName](#cfn-rds-dbcluster-dbclusterparametergroupname)" : String,
      "[DBSubnetGroupName](#cfn-rds-dbcluster-dbsubnetgroupname)" : String,
      "[DeletionProtection](#cfn-rds-dbcluster-deletionprotection)" : Boolean,
      "[EnableCloudwatchLogsExports](#cfn-rds-dbcluster-enablecloudwatchlogsexports)" : [ String, ... ],
      "[EnableHttpEndpoint](#cfn-rds-dbcluster-enablehttpendpoint)" : Boolean,
      "[EnableIAMDatabaseAuthentication](#cfn-rds-dbcluster-enableiamdatabaseauthentication)" : Boolean,
      "[Engine](#cfn-rds-dbcluster-engine)" : String,
      "[EngineMode](#cfn-rds-dbcluster-enginemode)" : String,
      "[EngineVersion](#cfn-rds-dbcluster-engineversion)" : String,
      "[GlobalClusterIdentifier](#cfn-rds-dbcluster-globalclusteridentifier)" : String,
      "[KmsKeyId](#cfn-rds-dbcluster-kmskeyid)" : String,
      "[MasterUsername](#cfn-rds-dbcluster-masterusername)" : String,
      "[MasterUserPassword](#cfn-rds-dbcluster-masteruserpassword)" : String,
      "[Port](#cfn-rds-dbcluster-port)" : Integer,
      "[PreferredBackupWindow](#cfn-rds-dbcluster-preferredbackupwindow)" : String,
      "[PreferredMaintenanceWindow](#cfn-rds-dbcluster-preferredmaintenancewindow)" : String,
      "[ReplicationSourceIdentifier](#cfn-rds-dbcluster-replicationsourceidentifier)" : String,
      "[RestoreType](#cfn-rds-dbcluster-restoretype)" : String,
      "[ScalingConfiguration](#cfn-rds-dbcluster-scalingconfiguration)" : ScalingConfiguration,
      "[SnapshotIdentifier](#cfn-rds-dbcluster-snapshotidentifier)" : String,
      "[SourceDBClusterIdentifier](#cfn-rds-dbcluster-sourcedbclusteridentifier)" : String,
      "[SourceRegion](#cfn-rds-dbcluster-sourceregion)" : String,
      "[StorageEncrypted](#cfn-rds-dbcluster-storageencrypted)" : Boolean,
      "[Tags](#cfn-rds-dbcluster-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UseLatestRestorableTime](#cfn-rds-dbcluster-uselatestrestorabletime)" : Boolean,
      "[VpcSecurityGroupIds](#cfn-rds-dbcluster-vpcsecuritygroupids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-rds-dbcluster-syntax.yaml"></a>

```
Type: AWS::RDS::DBCluster
Properties: 
  [AssociatedRoles](#cfn-rds-dbcluster-associatedroles): 
    - DBClusterRole
  [AvailabilityZones](#cfn-rds-dbcluster-availabilityzones): 
    - String
  [BacktrackWindow](#cfn-rds-dbcluster-backtrackwindow): Long
  [BackupRetentionPeriod](#cfn-rds-dbcluster-backuprententionperiod): Integer
  [DatabaseName](#cfn-rds-dbcluster-databasename): String
  [DBClusterIdentifier](#cfn-rds-dbcluster-dbclusteridentifier): String
  [DBClusterParameterGroupName](#cfn-rds-dbcluster-dbclusterparametergroupname): String
  [DBSubnetGroupName](#cfn-rds-dbcluster-dbsubnetgroupname): String
  [DeletionProtection](#cfn-rds-dbcluster-deletionprotection): Boolean
  [EnableCloudwatchLogsExports](#cfn-rds-dbcluster-enablecloudwatchlogsexports): 
    - String
  [EnableHttpEndpoint](#cfn-rds-dbcluster-enablehttpendpoint): Boolean
  [EnableIAMDatabaseAuthentication](#cfn-rds-dbcluster-enableiamdatabaseauthentication): Boolean
  [Engine](#cfn-rds-dbcluster-engine): String
  [EngineMode](#cfn-rds-dbcluster-enginemode): String
  [EngineVersion](#cfn-rds-dbcluster-engineversion): String
  [GlobalClusterIdentifier](#cfn-rds-dbcluster-globalclusteridentifier): String
  [KmsKeyId](#cfn-rds-dbcluster-kmskeyid): String
  [MasterUsername](#cfn-rds-dbcluster-masterusername): String
  [MasterUserPassword](#cfn-rds-dbcluster-masteruserpassword): String
  [Port](#cfn-rds-dbcluster-port): Integer
  [PreferredBackupWindow](#cfn-rds-dbcluster-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-rds-dbcluster-preferredmaintenancewindow): String
  [ReplicationSourceIdentifier](#cfn-rds-dbcluster-replicationsourceidentifier): String
  [RestoreType](#cfn-rds-dbcluster-restoretype): String
  [ScalingConfiguration](#cfn-rds-dbcluster-scalingconfiguration): 
    ScalingConfiguration
  [SnapshotIdentifier](#cfn-rds-dbcluster-snapshotidentifier): String
  [SourceDBClusterIdentifier](#cfn-rds-dbcluster-sourcedbclusteridentifier): String
  [SourceRegion](#cfn-rds-dbcluster-sourceregion): String
  [StorageEncrypted](#cfn-rds-dbcluster-storageencrypted): Boolean
  [Tags](#cfn-rds-dbcluster-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UseLatestRestorableTime](#cfn-rds-dbcluster-uselatestrestorabletime): Boolean
  [VpcSecurityGroupIds](#cfn-rds-dbcluster-vpcsecuritygroupids): 
    - String
```

## Properties<a name="aws-resource-rds-dbcluster-properties"></a>

`AssociatedRoles`  <a name="cfn-rds-dbcluster-associatedroles"></a>
Provides a list of the AWS Identity and Access Management \(IAM\) roles that are associated with the DB cluster\. IAM roles that are associated with a DB cluster grant permission for the DB cluster to access other AWS services on your behalf\.  
*Required*: No  
*Type*: List of [DBClusterRole](aws-properties-rds-dbcluster-dbclusterrole.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZones`  <a name="cfn-rds-dbcluster-availabilityzones"></a>
A list of Availability Zones \(AZs\) where instances in the DB cluster can be created\. For information on AWS Regions and Availability Zones, see [Choosing the Regions and Availability Zones](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Concepts.RegionsAndAvailabilityZones.html) in the *Amazon Aurora User Guide*\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BacktrackWindow`  <a name="cfn-rds-dbcluster-backtrackwindow"></a>
The target backtrack window, in seconds\. To disable backtracking, set this value to 0\.   
Currently, Backtrack is only supported for Aurora MySQL DB clusters\.
Default: 0  
Constraints:  
+ If specified, this value must be set to a number from 0 to 259,200 \(72 hours\)\.
*Required*: No  
*Type*: Long  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackupRetentionPeriod`  <a name="cfn-rds-dbcluster-backuprententionperiod"></a>
The number of days for which automated backups are retained\.  
Default: 1  
Constraints:  
+ Must be a value from 1 to 35
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-rds-dbcluster-databasename"></a>
The name of your database\. If you don't provide a name, then Amazon RDS won't create a database in this DB cluster\. For naming constraints, see [Naming Constraints](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Limits.html#RDS_Limits.Constraints) in the *Amazon RDS User Guide*\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBClusterIdentifier`  <a name="cfn-rds-dbcluster-dbclusteridentifier"></a>
The DB cluster identifier\. This parameter is stored as a lowercase string\.  
Constraints:  
+ Must contain from 1 to 63 letters, numbers, or hyphens\.
+ First character must be a letter\.
+ Can't end with a hyphen or contain two consecutive hyphens\.
Example: `my-cluster1`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBClusterParameterGroupName`  <a name="cfn-rds-dbcluster-dbclusterparametergroupname"></a>
The name of the DB cluster parameter group to associate with this DB cluster\.  
If you apply a parameter group to an existing DB cluster, then its DB instances might need to reboot\. This can result in an outage while the DB instances are rebooting\.  
If you apply a change to parameter group associated with a stopped DB cluster, then the update stack waits until the DB cluster is started\.
 If this argument is omitted, `default.aurora5.6` is used\. If `default.aurora5.6` is used, specifying `aurora-mysql` or `aurora-postgresql` for the `Engine` property might result in an error\.
To list all of the available DB cluster parameter group names, use the following command:  
`aws rds describe-db-cluster-parameter-groups --query "DBClusterParameterGroups[].DBClusterParameterGroupName" --output text`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBSubnetGroupName`  <a name="cfn-rds-dbcluster-dbsubnetgroupname"></a>
A DB subnet group that you want to associate with this DB cluster\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeletionProtection`  <a name="cfn-rds-dbcluster-deletionprotection"></a>
A value that indicates whether the DB cluster has deletion protection enabled\. The database can't be deleted when deletion protection is enabled\. By default, deletion protection is disabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableCloudwatchLogsExports`  <a name="cfn-rds-dbcluster-enablecloudwatchlogsexports"></a>
The list of log types that need to be enabled for exporting to CloudWatch Logs\. The values in the list depend on the DB engine being used\. For more information, see [Publishing Database Logs to Amazon CloudWatch Logs](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_LogAccess.html#USER_LogAccess.Procedural.UploadtoCloudWatch) in the *Amazon Aurora User Guide*\.  
 **Aurora MySQL**   
Possible values are `audit`, `error`, `general`, and `slowquery`\.   
 **Aurora PostgreSQL**   
Possible values are `postgresql` and `upgrade`\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableHttpEndpoint`  <a name="cfn-rds-dbcluster-enablehttpendpoint"></a>
A value that indicates whether to enable the HTTP endpoint for an Aurora Serverless DB cluster\. By default, the HTTP endpoint is disabled\.  
When enabled, the HTTP endpoint provides a connectionless web service API for running SQL queries on the Aurora Serverless DB cluster\. You can also query your database from inside the RDS console with the query editor\.  
For more information, see [Using the Data API for Aurora Serverless](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/data-api.html) in the *Amazon Aurora User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableIAMDatabaseAuthentication`  <a name="cfn-rds-dbcluster-enableiamdatabaseauthentication"></a>
A value that indicates whether to enable mapping of AWS Identity and Access Management \(IAM\) accounts to database accounts\. By default, mapping is disabled\.  
For more information, see [ IAM Database Authentication](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/UsingWithRDS.IAMDBAuth.html) in the *Amazon Aurora User Guide\.*   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engine`  <a name="cfn-rds-dbcluster-engine"></a>
The name of the database engine to be used for this DB cluster\.  
Valid Values: `aurora` \(for MySQL 5\.6\-compatible Aurora\), `aurora-mysql` \(for MySQL 5\.7\-compatible Aurora\), and `aurora-postgresql`   
*Required*: Yes  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`EngineMode`  <a name="cfn-rds-dbcluster-enginemode"></a>
The DB engine mode of the DB cluster, either `provisioned` `serverless`, `parallelquery`, `global`, or `multimaster`\.  
The `parallelquery` engine mode isn't required for Aurora MySQL version 1\.23 and higher 1\.x versions, and version 2\.09 and higher 2\.x versions\.  
The `global` engine mode isn't required for Aurora MySQL version 1\.22 and higher 1\.x versions, and `global` engine mode isn't required for any 2\.x versions\.  
The `multimaster` engine mode only applies for DB clusters created with Aurora MySQL version 5\.6\.10a\.  
For Aurora PostgreSQL, the `global` engine mode isn't required, and both the `parallelquery` and the `multimaster` engine modes currently aren't supported\.  
Limitations and requirements apply to some DB engine modes\. For more information, see the following sections in the *Amazon Aurora User Guide*:  
+  [ Limitations of Aurora Serverless](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html#aurora-serverless.limitations) 
+  [ Limitations of Parallel Query](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-mysql-parallel-query.html#aurora-mysql-parallel-query-limitations) 
+  [ Limitations of Aurora Global Databases](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html#aurora-global-database.limitations) 
+  [ Limitations of Multi\-Master Clusters](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-multi-master.html#aurora-multi-master-limitations) 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineVersion`  <a name="cfn-rds-dbcluster-engineversion"></a>
The version number of the database engine to use\.  
To list all of the available engine versions for `aurora` \(for MySQL 5\.6\-compatible Aurora\), use the following command:  
`aws rds describe-db-engine-versions --engine aurora --query "DBEngineVersions[].EngineVersion"`  
To list all of the available engine versions for `aurora-mysql` \(for MySQL 5\.7\-compatible Aurora\), use the following command:  
`aws rds describe-db-engine-versions --engine aurora-mysql --query "DBEngineVersions[].EngineVersion"`  
To list all of the available engine versions for `aurora-postgresql`, use the following command:  
`aws rds describe-db-engine-versions --engine aurora-postgresql --query "DBEngineVersions[].EngineVersion"`  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`GlobalClusterIdentifier`  <a name="cfn-rds-dbcluster-globalclusteridentifier"></a>
 If you are configuring an Aurora global database cluster and want your Aurora DB cluster to be a member in the global database cluster, specify the global cluster ID of the global database cluster\.   
 If you aren't configuring a global database cluster, don't specify this property\.   
To remove the DB cluster from a global database cluster, specify an empty value for the `GlobalClusterIdentifier` property\.
For information about Aurora global databases, see [ Working with Amazon Aurora Global Databases](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html) in the *Amazon Aurora User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`KmsKeyId`  <a name="cfn-rds-dbcluster-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of the AWS Key Management Service master key that is used to encrypt the database instances in the DB cluster, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the `StorageEncrypted` property but don't specify this property, the default master key is used\. If you specify this property, you must set the `StorageEncrypted` property to `true`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUsername`  <a name="cfn-rds-dbcluster-masterusername"></a>
The name of the master user for the DB cluster\.  
If you specify the `SourceDBInstanceIdentifier` or `SnapshotIdentifier` property, don't specify this property\. The value is inherited from the source DB instance or snapshot\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUserPassword`  <a name="cfn-rds-dbcluster-masteruserpassword"></a>
The master password for the DB instance\.  
If you specify the `SourceDBInstanceIdentifier` or `SnapshotIdentifier` property, don't specify this property\. The value is inherited from the source DB instance or snapshot\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-rds-dbcluster-port"></a>
The port number on which the DB instances in the DB cluster accept connections\.  
Default:  
+ When `EngineMode` is `provisioned`, `3306` \(for both Aurora MySQL and Aurora PostgreSQL\)
+ When `EngineMode` is `serverless`:
  + `3306` when `Engine` is `aurora` or `aurora-mysql`
  + `5432` when `Engine` is `aurora-postgresql`
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredBackupWindow`  <a name="cfn-rds-dbcluster-preferredbackupwindow"></a>
The daily time range during which automated backups are created if automated backups are enabled using the `BackupRetentionPeriod` parameter\.   
The default is a 30\-minute window selected at random from an 8\-hour block of time for each AWS Region\. To see the time blocks available, see [ Adjusting the Preferred DB Cluster Maintenance Window](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_UpgradeDBInstance.Maintenance.html#AdjustingTheMaintenanceWindow.Aurora) in the *Amazon Aurora User Guide\.*   
Constraints:  
+ Must be in the format `hh24:mi-hh24:mi`\.
+ Must be in Universal Coordinated Time \(UTC\)\.
+ Must not conflict with the preferred maintenance window\.
+ Must be at least 30 minutes\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-rds-dbcluster-preferredmaintenancewindow"></a>
The weekly time range during which system maintenance can occur, in Universal Coordinated Time \(UTC\)\.  
Format: `ddd:hh24:mi-ddd:hh24:mi`   
The default is a 30\-minute window selected at random from an 8\-hour block of time for each AWS Region, occurring on a random day of the week\. To see the time blocks available, see [ Adjusting the Preferred DB Cluster Maintenance Window](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_UpgradeDBInstance.Maintenance.html#AdjustingTheMaintenanceWindow.Aurora) in the *Amazon Aurora User Guide\.*   
Valid Days: Mon, Tue, Wed, Thu, Fri, Sat, Sun\.  
Constraints: Minimum 30\-minute window\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationSourceIdentifier`  <a name="cfn-rds-dbcluster-replicationsourceidentifier"></a>
The Amazon Resource Name \(ARN\) of the source DB instance or DB cluster if this DB cluster is created as a read replica\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestoreType`  <a name="cfn-rds-dbcluster-restoretype"></a>
The type of restore to be performed\. You can specify one of the following values:  
+  `full-copy` \- The new DB cluster is restored as a full copy of the source DB cluster\.
+  `copy-on-write` \- The new DB cluster is restored as a clone of the source DB cluster\.
Constraints: You can't specify `copy-on-write` if the engine version of the source DB cluster is earlier than 1\.11\.  
If you don't specify a `RestoreType` value, then the new DB cluster is restored as a full copy of the source DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScalingConfiguration`  <a name="cfn-rds-dbcluster-scalingconfiguration"></a>
The `ScalingConfiguration` property type specifies the scaling configuration of an Aurora Serverless DB cluster\.  
*Required*: No  
*Type*: [ScalingConfiguration](aws-properties-rds-dbcluster-scalingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotIdentifier`  <a name="cfn-rds-dbcluster-snapshotidentifier"></a>
The identifier for the DB snapshot or DB cluster snapshot to restore from\.  
You can use either the name or the Amazon Resource Name \(ARN\) to specify a DB cluster snapshot\. However, you can use only the ARN to specify a DB snapshot\.  
After you restore a DB cluster with a `SnapshotIdentifier` property, you must specify the same `SnapshotIdentifier` property for any future updates to the DB cluster\. When you specify this property for an update, the DB cluster is not restored from the snapshot again, and the data in the database is not changed\. However, if you don't specify the `SnapshotIdentifier` property, an empty DB cluster is created, and the original DB cluster is deleted\. If you specify a property that is different from the previous snapshot restore property, a new DB cluster is restored from the specified `SnapshotIdentifier` property, and the original DB cluster is deleted\.  
If you specify the `SnapshotIdentifier` property to restore a DB cluster \(as opposed to specifying it for DB cluster updates\), then don't specify the following properties:  
+ `BackupRetentionPeriod`
+ `EnableHttpEndpoint`
+ `GlobalClusterIdentifier`
+ `MasterUsername`
+ `MasterUserPassword`
+ `PreferredBackupWindow`
+ `PreferredMaintenanceWindow`
+ `ReplicationSourceIdentifier`
+ `RestoreType`
+ `SourceDBClusterIdentifier`
+ `SourceRegion`
+ `StorageEncrypted`
+ `UseLatestRestorableTime`
Constraints:  
+ Must match the identifier of an existing Snapshot\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceDBClusterIdentifier`  <a name="cfn-rds-dbcluster-sourcedbclusteridentifier"></a>
The identifier of the source DB cluster from which to restore\.  
Constraints:  
+ Must match the identifier of an existing DBCluster\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceRegion`  <a name="cfn-rds-dbcluster-sourceregion"></a>
The AWS Region which contains the source DB cluster when replicating a DB cluster\. For example, `us-east-1`\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageEncrypted`  <a name="cfn-rds-dbcluster-storageencrypted"></a>
Indicates whether the DB cluster is encrypted\.  
If you specify the `SnapshotIdentifier` or `SourceDBInstanceIdentifier` property, don't specify this property\. The value is inherited from the snapshot or source DB instance\.   
If you specify the `KmsKeyId` property, then you must enable encryption\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-rds-dbcluster-tags"></a>
Tags to assign to the DB cluster\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseLatestRestorableTime`  <a name="cfn-rds-dbcluster-uselatestrestorabletime"></a>
A value that indicates whether to restore the DB cluster to the latest restorable backup time\. By default, the DB cluster is not restored to the latest restorable backup time\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcSecurityGroupIds`  <a name="cfn-rds-dbcluster-vpcsecuritygroupids"></a>
A list of EC2 VPC security groups to associate with this DB cluster\.  
If you plan to update the resource, don't specify VPC security groups in a shared VPC\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rds-dbcluster-return-values"></a>

### Ref<a name="aws-resource-rds-dbcluster-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the DB cluster as an uppercase string\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-rds-dbcluster-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-rds-dbcluster-return-values-fn--getatt-fn--getatt"></a>

`Endpoint.Address`  <a name="Endpoint.Address-fn::getatt"></a>
The connection endpoint for the DB cluster\. For example: `mystack-mydbcluster-123456789012.us-east-2.rds.amazonaws.com` 

`Endpoint.Port`  <a name="Endpoint.Port-fn::getatt"></a>
The port number that will accept connections on this DB cluster\. For example: `3306` 

`ReadEndpoint.Address`  <a name="ReadEndpoint.Address-fn::getatt"></a>
The reader endpoint for the DB cluster\. For example: `mystack-mydbcluster-ro-123456789012.us-east-2.rds.amazonaws.com` 

## Examples<a name="aws-resource-rds-dbcluster--examples"></a>

The following examples create DB clusters\.

**Note**  
For an example that adds a scaling policy for a DB cluster with Application Auto Scaling, see [Declaring a scaling policy for an Aurora DB cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html#w2ab1c19c22c15c21c11)\.

### Creating an Amazon Aurora DB cluster with two DB instances<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_DB_cluster_with_two_DB_instances"></a>

The following example creates an Amazon Aurora DB cluster and adds two DB instances to it\. Because Amazon RDS automatically assigns a writer and reader DB instances in the cluster, use the cluster endpoint to read and write data, not the individual DB instance endpoints\. 

**Note**  
The example uses the `time_zone` Aurora MySQL parameter\. For Aurora PostgreSQL, use the `timezone` parameter instead\.

#### JSON<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_DB_cluster_with_two_DB_instances--json"></a>

```
{
    "RDSCluster": {
        "Type": "AWS::RDS::DBCluster",
        "Properties": {
            "MasterUsername": {
                "Ref": "username"
            },
            "MasterUserPassword": {
                "Ref": "password"
            },
            "Engine": "aurora",
            "DBSubnetGroupName": {
                "Ref": "DBSubnetGroup"
            },
            "DBClusterParameterGroupName": {
                "Ref": "RDSDBClusterParameterGroup"
            }
        }
    },
    "RDSDBInstance1": {
        "Type": "AWS::RDS::DBInstance",
        "Properties": {
            "DBSubnetGroupName": {
                "Ref": "DBSubnetGroup"
            },
            "DBParameterGroupName": {
                "Ref": "RDSDBParameterGroup"
            },
            "Engine": "aurora",
            "DBClusterIdentifier": {
                "Ref": "RDSCluster"
            },
            "PubliclyAccessible": "true",
            "AvailabilityZone": {
                "Fn::GetAtt": [
                    "Subnet1",
                    "AvailabilityZone"
                ]
            },
            "DBInstanceClass": "db.r3.xlarge"
        }
    },
    "RDSDBInstance2": {
        "Type": "AWS::RDS::DBInstance",
        "Properties": {
            "DBSubnetGroupName": {
                "Ref": "DBSubnetGroup"
            },
            "DBParameterGroupName": {
                "Ref": "RDSDBParameterGroup"
            },
            "Engine": "aurora",
            "DBClusterIdentifier": {
                "Ref": "RDSCluster"
            },
            "PubliclyAccessible": "true",
            "AvailabilityZone": {
                "Fn::GetAtt": [
                    "Subnet2",
                    "AvailabilityZone"
                ]
            },
            "DBInstanceClass": "db.r3.xlarge"
        }
    },
    "RDSDBClusterParameterGroup": {
        "Type": "AWS::RDS::DBClusterParameterGroup",
        "Properties": {
            "Description": "CloudFormation Sample Aurora Cluster Parameter Group",
            "Family": "aurora5.6",
            "Parameters": {
                "time_zone": "US/Eastern"
            }
        }
    },
    "RDSDBParameterGroup": {
        "Type": "AWS::RDS::DBParameterGroup",
        "Properties": {
            "Description": "CloudFormation Sample Aurora Parameter Group",
            "Family": "aurora5.6",
            "Parameters": {
                "sql_mode": "IGNORE_SPACE",
                "max_allowed_packet": 1024,
                "innodb_buffer_pool_size": "{DBInstanceClassMemory*3/4}"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_DB_cluster_with_two_DB_instances--yaml"></a>

```
RDSCluster: 
  Properties: 
    DBClusterParameterGroupName: 
      Ref: RDSDBClusterParameterGroup
    DBSubnetGroupName: 
      Ref: DBSubnetGroup
    Engine: aurora
    MasterUserPassword: 
      Ref: password
    MasterUsername: 
      Ref: username
  Type: "AWS::RDS::DBCluster"
RDSDBClusterParameterGroup: 
  Properties: 
    Description: "CloudFormation Sample Aurora Cluster Parameter Group"
    Family: aurora5.6
    Parameters: 
      time_zone: US/Eastern
  Type: "AWS::RDS::DBClusterParameterGroup"
RDSDBInstance1: 
  Properties: 
    AvailabilityZone: 
      Fn::GetAtt:
        - Subnet1
        - AvailabilityZone
    DBClusterIdentifier: 
      Ref: RDSCluster
    DBInstanceClass: db.r3.xlarge
    DBParameterGroupName: 
      Ref: RDSDBParameterGroup
    DBSubnetGroupName: 
      Ref: DBSubnetGroup
    Engine: aurora
    PubliclyAccessible: "true"
  Type: "AWS::RDS::DBInstance"
RDSDBInstance2: 
  Properties: 
    AvailabilityZone: 
      Fn::GetAtt:
        - Subnet2
        - AvailabilityZone
    DBClusterIdentifier: 
      Ref: RDSCluster
    DBInstanceClass: db.r3.xlarge
    DBParameterGroupName: 
      Ref: RDSDBParameterGroup
    DBSubnetGroupName: 
      Ref: DBSubnetGroup
    Engine: aurora
    PubliclyAccessible: "true"
  Type: "AWS::RDS::DBInstance"
RDSDBParameterGroup:
  Type: 'AWS::RDS::DBParameterGroup'
  Properties:
    Description: CloudFormation Sample Aurora Parameter Group
    Family: aurora5.6
    Parameters:
      sql_mode: IGNORE_SPACE
      max_allowed_packet: 1024
      innodb_buffer_pool_size: '{DBInstanceClassMemory*3/4}'
```

### Creating an Amazon Aurora DB cluster that exports logs to Amazon CloudWatch Logs<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_DB_cluster_that_exports_logs_to_Amazon_CloudWatch_Logs"></a>

The following example creates an Amazon Aurora PostgreSQL DB cluster that exports logs to Amazon CloudWatch Logs\. For more information about exporting Aurora DB cluster logs to Amazon CloudWatch Logs, see [ Publishing Database Logs to Amazon CloudWatch Logs](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_LogAccess.html#USER_LogAccess.Procedural.UploadtoCloudWatch) in the *Amazon Aurora User Guide*\.

#### JSON<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_DB_cluster_that_exports_logs_to_Amazon_CloudWatch_Logs--json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",


  "Description" : "AWS CloudFormation Sample Template for sending Aurora DB cluster logs to CloudWatch Logs: Sample template showing how to create an Aurora PostgreSQL DB cluster that exports logs to CloudWatch Logs. **WARNING** This template enables log exports to CloudWatch Logs. You will be billed for the AWS resources used if you create a stack from this template.",


  "Parameters" : {
      "DBUsername" : {
        "NoEcho" : "true",
        "Description" : "Username for MySQL database access",

        "Type" : "String",
        "MinLength" : "1",
        "MaxLength" : "16",
        "AllowedPattern" : "[a-zA-Z][a-zA-Z0-9]*",
        "ConstraintDescription" : "must begin with a letter and contain only alphanumeric characters."
      },
      "DBPassword" : {
        "NoEcho" : "true",
        "Description" : "Password MySQL database access",

        "Type" : "String",
        "MinLength" : "8",

        "MaxLength" : "41",
        "AllowedPattern" : "[a-zA-Z0-9]*",
        "ConstraintDescription" : "must contain only alphanumeric characters."
      }
  },

  "Resources" : {
      "RDSCluster" : {
          "Type": "AWS::RDS::DBCluster",
          "Properties" : {
              "MasterUsername" : {
                  "Ref" : "DBUsername"
              },
              "MasterUserPassword" : {
                  "Ref" : "DBPassword"
              },
              "DBClusterIdentifier" : "aurora-postgresql-cluster",
              "Engine" : "aurora-postgresql",
              "EngineVersion" : "10.7",
              "DBClusterParameterGroupName" : "default.aurora-postgresql10",
              "EnableCloudwatchLogsExports" : ["postgresql"]
          }
      },
  "RDSDBInstance1": {
        "Type" : "AWS::RDS::DBInstance",
        "Properties" : {
            "DBInstanceIdentifier" : "aurora-postgresql-instance1",
            "Engine" : "aurora-postgresql",
            "DBClusterIdentifier" : {
                "Ref" : "RDSCluster"
            },
            "PubliclyAccessible" : "true",
            "DBInstanceClass" : "db.r4.large"
        }
    },
  "RDSDBInstance2": {
        "Type" : "AWS::RDS::DBInstance",
        "Properties" : {
            "DBInstanceIdentifier" : "aurora-postgresql-instance2",
            "Engine" : "aurora-postgresql",
            "DBClusterIdentifier" : {
                "Ref" : "RDSCluster"
            },
            "PubliclyAccessible" : "true",
            "DBInstanceClass" : "db.r4.large"
        }
    },
  }
}
```

#### YAML<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_DB_cluster_that_exports_logs_to_Amazon_CloudWatch_Logs--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: >-
  AWS CloudFormation Sample Template for sending Aurora DB cluster logs to
  CloudWatch Logs: Sample template showing how to create an Aurora PostgreSQL DB
  cluster that exports logs to CloudWatch Logs. **WARNING** This template
  enables log exports to CloudWatch Logs. You will be billed for the AWS
  resources used if you create a stack from this template.
Parameters:
  DBUsername:
    NoEcho: 'true'
    Description: Username for MySQL database access
    Type: String
    MinLength: '1'
    MaxLength: '16'
    AllowedPattern: '[a-zA-Z][a-zA-Z0-9]*'
    ConstraintDescription: must begin with a letter and contain only alphanumeric characters.
  DBPassword:
    NoEcho: 'true'
    Description: Password MySQL database access
    Type: String
    MinLength: '8'
    MaxLength: '41'
    AllowedPattern: '[a-zA-Z0-9]*'
    ConstraintDescription: must contain only alphanumeric characters.
Resources:
  RDSCluster:
    Type: 'AWS::RDS::DBCluster'
    Properties:
      MasterUsername: !Ref DBUsername
      MasterUserPassword: !Ref DBPassword
      DBClusterIdentifier: aurora-postgresql-cluster
      Engine: aurora-postgresql
      EngineVersion: '10.7'
      DBClusterParameterGroupName: default.aurora-postgresql10
      EnableCloudwatchLogsExports:
        - postgresql
  RDSDBInstance1:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      DBInstanceIdentifier: aurora-postgresql-instance1
      Engine: aurora-postgresql
      DBClusterIdentifier: !Ref RDSCluster
      PubliclyAccessible: 'true'
      DBInstanceClass: db.r4.large
  RDSDBInstance2:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      DBInstanceIdentifier: aurora-postgresql-instance2
      Engine: aurora-postgresql
      DBClusterIdentifier: !Ref RDSCluster
      PubliclyAccessible: 'true'
      DBInstanceClass: db.r4.large
```

### Creating an Amazon Aurora Serverless DB cluster<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_Serverless_DB_cluster"></a>

The following example creates an Amazon Aurora Serverless DB cluster\. An Aurora Serverless DB cluster is a DB cluster that automatically starts up, shuts down, and scales up or down its compute capacity based on your application's needs\. For more information about Aurora Serverless DB clusters, see [Using Amazon Aurora Serverless](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html) in the *Amazon Aurora User Guide*\.

**Note**  
This example creates an Aurora MySQL Serverless DB cluster by setting `Engine` to `aurora` and `EngineVersion` to `5.6.10a`\. To create an Aurora PostgreSQL Serverless DB cluster, set `Engine` to `aurora-postgresql` and `EngineVersion` to `10.7`\.

#### JSON<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_Serverless_DB_cluster--json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Description" : "AWS CloudFormation Sample Template AuroraServerlessDBCluster: Sample template showing how to create an Amazon Aurora Serverless DB cluster. **WARNING** This template creates an Amazon Aurora DB cluster. You will be billed for the AWS resources used if you create a stack from this template.",

  "Parameters" : {
      "DBUsername" : {
        "NoEcho" : "true",
        "Description" : "Username for MySQL database access",
        "Type" : "String",
        "MinLength" : "1",
        "MaxLength" : "16",
        "AllowedPattern" : "[a-zA-Z][a-zA-Z0-9]*",
        "ConstraintDescription" : "must begin with a letter and contain only alphanumeric characters."
      },
      "DBPassword" : {
        "NoEcho" : "true",
        "Description" : "Password MySQL database access",
        "Type" : "String",
        "MinLength" : "8",
        "MaxLength" : "41",
        "AllowedPattern" : "[a-zA-Z0-9]*",
        "ConstraintDescription" : "must contain only alphanumeric characters."
      }
  },
  "Resources" : {
      "RDSCluster" : {
          "Type": "AWS::RDS::DBCluster",
          "Properties" : {
              "MasterUsername" : {
                  "Ref": "DBUsername"
              },
              "MasterUserPassword" : {
                  "Ref": "DBPassword"
              },
              "DBClusterIdentifier" : "my-serverless-cluster",
              "Engine" : "aurora",
              "EngineVersion" : "5.6.10a",
              "EngineMode" : "serverless",
              "ScalingConfiguration" : {
                  "AutoPause" : true,
                  "MinCapacity" : 4,
                  "MaxCapacity" : 32,
                  "SecondsUntilAutoPause" : 1000
              }
          }
      }
  }
}
```

#### YAML<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_Serverless_DB_cluster--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: >-
  AWS CloudFormation Sample Template AuroraServerlessDBCluster: Sample template
  showing how to create an Amazon Aurora Serverless DB cluster. **WARNING** This
  template creates an Amazon Aurora DB cluster. You will be billed for the AWS
  resources used if you create a stack from this template.
Parameters:
  DBUsername:
    NoEcho: 'true'
    Description: Username for MySQL database access
    Type: String
    MinLength: '1'
    MaxLength: '16'
    AllowedPattern: '[a-zA-Z][a-zA-Z0-9]*'
    ConstraintDescription: must begin with a letter and contain only alphanumeric characters.
  DBPassword:
    NoEcho: 'true'
    Description: Password MySQL database access
    Type: String
    MinLength: '8'
    MaxLength: '41'
    AllowedPattern: '[a-zA-Z0-9]*'
    ConstraintDescription: must contain only alphanumeric characters.
Resources:
  RDSCluster:
    Type: 'AWS::RDS::DBCluster'
    Properties:
      MasterUsername: !Ref DBUsername
      MasterUserPassword: !Ref DBPassword
      DBClusterIdentifier: my-serverless-cluster
      Engine: aurora
      EngineVersion: 5.6.10a
      EngineMode: serverless
      ScalingConfiguration:
        AutoPause: true
        MinCapacity: 4
        MaxCapacity: 32
        SecondsUntilAutoPause: 1000
```