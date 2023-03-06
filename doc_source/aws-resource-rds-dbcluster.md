# AWS::RDS::DBCluster<a name="aws-resource-rds-dbcluster"></a>

The `AWS::RDS::DBCluster` resource creates an Amazon Aurora DB cluster or Multi\-AZ DB cluster\.

For more information about creating an Aurora DB cluster, see [ Creating an Amazon Aurora DB cluster](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.CreateInstance.html) in the *Amazon Aurora User Guide*\.

For more information about creating a Multi\-AZ DB cluster, see [Creating a Multi\-AZ DB cluster](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/create-multi-az-db-cluster.html) in the *Amazon RDS User Guide*\.

**Note**  
You can only create this resource in AWS Regions where Amazon Aurora or Multi\-AZ DB clusters are supported\.

**Updating DB clusters**

When properties labeled "*Update requires:* [ Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)" are updated, AWS CloudFormation first creates a replacement DB cluster, then changes references from other dependent resources to point to the replacement DB cluster, and finally deletes the old DB cluster\.

**Important**  
We highly recommend that you take a snapshot of the database before updating the stack\. If you don't, you lose the data when AWS CloudFormation replaces your DB cluster\. To preserve your data, perform the following procedure:  
Deactivate any applications that are using the DB cluster so that there's no activity on the DB instance\.
Create a snapshot of the DB cluster\. For more information, see [Creating a DB Cluster Snapshot](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_CreateSnapshotCluster.html)\.
If you want to restore your DB cluster using a DB cluster snapshot, modify the updated template with your DB cluster changes and add the `SnapshotIdentifier` property with the ID of the DB cluster snapshot that you want to use\.  
After you restore a DB cluster with a `SnapshotIdentifier` property, you must specify the same `SnapshotIdentifier` property for any future updates to the DB cluster\. When you specify this property for an update, the DB cluster is not restored from the DB cluster snapshot again, and the data in the database is not changed\. However, if you don't specify the `SnapshotIdentifier` property, an empty DB cluster is created, and the original DB cluster is deleted\. If you specify a property that is different from the previous snapshot restore property, a new DB cluster is restored from the specified `SnapshotIdentifier` property, and the original DB cluster is deleted\.
Update the stack\.

Currently, when you are updating the stack for an Aurora Serverless DB cluster, you can't include changes to any other properties when you specify one of the following properties: `PreferredBackupWindow`, `PreferredMaintenanceWindow`, and `Port`\. This limitation doesn't apply to provisioned DB clusters\.

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
      "[AllocatedStorage](#cfn-rds-dbcluster-allocatedstorage)" : Integer,
      "[AssociatedRoles](#cfn-rds-dbcluster-associatedroles)" : [ DBClusterRole, ... ],
      "[AutoMinorVersionUpgrade](#cfn-rds-dbcluster-autominorversionupgrade)" : Boolean,
      "[AvailabilityZones](#cfn-rds-dbcluster-availabilityzones)" : [ String, ... ],
      "[BacktrackWindow](#cfn-rds-dbcluster-backtrackwindow)" : Integer,
      "[BackupRetentionPeriod](#cfn-rds-dbcluster-backupretentionperiod)" : Integer,
      "[CopyTagsToSnapshot](#cfn-rds-dbcluster-copytagstosnapshot)" : Boolean,
      "[DatabaseName](#cfn-rds-dbcluster-databasename)" : String,
      "[DBClusterIdentifier](#cfn-rds-dbcluster-dbclusteridentifier)" : String,
      "[DBClusterInstanceClass](#cfn-rds-dbcluster-dbclusterinstanceclass)" : String,
      "[DBClusterParameterGroupName](#cfn-rds-dbcluster-dbclusterparametergroupname)" : String,
      "[DBInstanceParameterGroupName](#cfn-rds-dbcluster-dbinstanceparametergroupname)" : String,
      "[DBSubnetGroupName](#cfn-rds-dbcluster-dbsubnetgroupname)" : String,
      "[DBSystemId](#cfn-rds-dbcluster-dbsystemid)" : String,
      "[DeletionProtection](#cfn-rds-dbcluster-deletionprotection)" : Boolean,
      "[Domain](#cfn-rds-dbcluster-domain)" : String,
      "[DomainIAMRoleName](#cfn-rds-dbcluster-domainiamrolename)" : String,
      "[EnableCloudwatchLogsExports](#cfn-rds-dbcluster-enablecloudwatchlogsexports)" : [ String, ... ],
      "[EnableHttpEndpoint](#cfn-rds-dbcluster-enablehttpendpoint)" : Boolean,
      "[EnableIAMDatabaseAuthentication](#cfn-rds-dbcluster-enableiamdatabaseauthentication)" : Boolean,
      "[Engine](#cfn-rds-dbcluster-engine)" : String,
      "[EngineMode](#cfn-rds-dbcluster-enginemode)" : String,
      "[EngineVersion](#cfn-rds-dbcluster-engineversion)" : String,
      "[GlobalClusterIdentifier](#cfn-rds-dbcluster-globalclusteridentifier)" : String,
      "[Iops](#cfn-rds-dbcluster-iops)" : Integer,
      "[KmsKeyId](#cfn-rds-dbcluster-kmskeyid)" : String,
      "[ManageMasterUserPassword](#cfn-rds-dbcluster-managemasteruserpassword)" : Boolean,
      "[MasterUsername](#cfn-rds-dbcluster-masterusername)" : String,
      "[MasterUserPassword](#cfn-rds-dbcluster-masteruserpassword)" : String,
      "[MasterUserSecret](#cfn-rds-dbcluster-masterusersecret)" : MasterUserSecret,
      "[MonitoringInterval](#cfn-rds-dbcluster-monitoringinterval)" : Integer,
      "[MonitoringRoleArn](#cfn-rds-dbcluster-monitoringrolearn)" : String,
      "[NetworkType](#cfn-rds-dbcluster-networktype)" : String,
      "[PerformanceInsightsEnabled](#cfn-rds-dbcluster-performanceinsightsenabled)" : Boolean,
      "[PerformanceInsightsKmsKeyId](#cfn-rds-dbcluster-performanceinsightskmskeyid)" : String,
      "[PerformanceInsightsRetentionPeriod](#cfn-rds-dbcluster-performanceinsightsretentionperiod)" : Integer,
      "[Port](#cfn-rds-dbcluster-port)" : Integer,
      "[PreferredBackupWindow](#cfn-rds-dbcluster-preferredbackupwindow)" : String,
      "[PreferredMaintenanceWindow](#cfn-rds-dbcluster-preferredmaintenancewindow)" : String,
      "[PubliclyAccessible](#cfn-rds-dbcluster-publiclyaccessible)" : Boolean,
      "[ReplicationSourceIdentifier](#cfn-rds-dbcluster-replicationsourceidentifier)" : String,
      "[RestoreType](#cfn-rds-dbcluster-restoretype)" : String,
      "[ScalingConfiguration](#cfn-rds-dbcluster-scalingconfiguration)" : ScalingConfiguration,
      "[ServerlessV2ScalingConfiguration](#cfn-rds-dbcluster-serverlessv2scalingconfiguration)" : ServerlessV2ScalingConfiguration,
      "[SnapshotIdentifier](#cfn-rds-dbcluster-snapshotidentifier)" : String,
      "[SourceDBClusterIdentifier](#cfn-rds-dbcluster-sourcedbclusteridentifier)" : String,
      "[SourceRegion](#cfn-rds-dbcluster-sourceregion)" : String,
      "[StorageEncrypted](#cfn-rds-dbcluster-storageencrypted)" : Boolean,
      "[StorageType](#cfn-rds-dbcluster-storagetype)" : String,
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
  [AllocatedStorage](#cfn-rds-dbcluster-allocatedstorage): Integer
  [AssociatedRoles](#cfn-rds-dbcluster-associatedroles): 
    - DBClusterRole
  [AutoMinorVersionUpgrade](#cfn-rds-dbcluster-autominorversionupgrade): Boolean
  [AvailabilityZones](#cfn-rds-dbcluster-availabilityzones): 
    - String
  [BacktrackWindow](#cfn-rds-dbcluster-backtrackwindow): Integer
  [BackupRetentionPeriod](#cfn-rds-dbcluster-backupretentionperiod): Integer
  [CopyTagsToSnapshot](#cfn-rds-dbcluster-copytagstosnapshot): Boolean
  [DatabaseName](#cfn-rds-dbcluster-databasename): String
  [DBClusterIdentifier](#cfn-rds-dbcluster-dbclusteridentifier): String
  [DBClusterInstanceClass](#cfn-rds-dbcluster-dbclusterinstanceclass): String
  [DBClusterParameterGroupName](#cfn-rds-dbcluster-dbclusterparametergroupname): String
  [DBInstanceParameterGroupName](#cfn-rds-dbcluster-dbinstanceparametergroupname): String
  [DBSubnetGroupName](#cfn-rds-dbcluster-dbsubnetgroupname): String
  [DBSystemId](#cfn-rds-dbcluster-dbsystemid): String
  [DeletionProtection](#cfn-rds-dbcluster-deletionprotection): Boolean
  [Domain](#cfn-rds-dbcluster-domain): String
  [DomainIAMRoleName](#cfn-rds-dbcluster-domainiamrolename): String
  [EnableCloudwatchLogsExports](#cfn-rds-dbcluster-enablecloudwatchlogsexports): 
    - String
  [EnableHttpEndpoint](#cfn-rds-dbcluster-enablehttpendpoint): Boolean
  [EnableIAMDatabaseAuthentication](#cfn-rds-dbcluster-enableiamdatabaseauthentication): Boolean
  [Engine](#cfn-rds-dbcluster-engine): String
  [EngineMode](#cfn-rds-dbcluster-enginemode): String
  [EngineVersion](#cfn-rds-dbcluster-engineversion): String
  [GlobalClusterIdentifier](#cfn-rds-dbcluster-globalclusteridentifier): String
  [Iops](#cfn-rds-dbcluster-iops): Integer
  [KmsKeyId](#cfn-rds-dbcluster-kmskeyid): String
  [ManageMasterUserPassword](#cfn-rds-dbcluster-managemasteruserpassword): Boolean
  [MasterUsername](#cfn-rds-dbcluster-masterusername): String
  [MasterUserPassword](#cfn-rds-dbcluster-masteruserpassword): String
  [MasterUserSecret](#cfn-rds-dbcluster-masterusersecret): 
    MasterUserSecret
  [MonitoringInterval](#cfn-rds-dbcluster-monitoringinterval): Integer
  [MonitoringRoleArn](#cfn-rds-dbcluster-monitoringrolearn): String
  [NetworkType](#cfn-rds-dbcluster-networktype): String
  [PerformanceInsightsEnabled](#cfn-rds-dbcluster-performanceinsightsenabled): Boolean
  [PerformanceInsightsKmsKeyId](#cfn-rds-dbcluster-performanceinsightskmskeyid): String
  [PerformanceInsightsRetentionPeriod](#cfn-rds-dbcluster-performanceinsightsretentionperiod): Integer
  [Port](#cfn-rds-dbcluster-port): Integer
  [PreferredBackupWindow](#cfn-rds-dbcluster-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-rds-dbcluster-preferredmaintenancewindow): String
  [PubliclyAccessible](#cfn-rds-dbcluster-publiclyaccessible): Boolean
  [ReplicationSourceIdentifier](#cfn-rds-dbcluster-replicationsourceidentifier): String
  [RestoreType](#cfn-rds-dbcluster-restoretype): String
  [ScalingConfiguration](#cfn-rds-dbcluster-scalingconfiguration): 
    ScalingConfiguration
  [ServerlessV2ScalingConfiguration](#cfn-rds-dbcluster-serverlessv2scalingconfiguration): 
    ServerlessV2ScalingConfiguration
  [SnapshotIdentifier](#cfn-rds-dbcluster-snapshotidentifier): String
  [SourceDBClusterIdentifier](#cfn-rds-dbcluster-sourcedbclusteridentifier): String
  [SourceRegion](#cfn-rds-dbcluster-sourceregion): String
  [StorageEncrypted](#cfn-rds-dbcluster-storageencrypted): Boolean
  [StorageType](#cfn-rds-dbcluster-storagetype): String
  [Tags](#cfn-rds-dbcluster-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UseLatestRestorableTime](#cfn-rds-dbcluster-uselatestrestorabletime): Boolean
  [VpcSecurityGroupIds](#cfn-rds-dbcluster-vpcsecuritygroupids): 
    - String
```

## Properties<a name="aws-resource-rds-dbcluster-properties"></a>

`AllocatedStorage`  <a name="cfn-rds-dbcluster-allocatedstorage"></a>
The amount of storage in gibibytes \(GiB\) to allocate to each DB instance in the Multi\-AZ DB cluster\.  
This setting is required to create a Multi\-AZ DB cluster\.  
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssociatedRoles`  <a name="cfn-rds-dbcluster-associatedroles"></a>
Provides a list of the AWS Identity and Access Management \(IAM\) roles that are associated with the DB cluster\. IAM roles that are associated with a DB cluster grant permission for the DB cluster to access other Amazon Web Services on your behalf\.  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: List of [DBClusterRole](aws-properties-rds-dbcluster-dbclusterrole.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoMinorVersionUpgrade`  <a name="cfn-rds-dbcluster-autominorversionupgrade"></a>
A value that indicates whether minor engine upgrades are applied automatically to the DB cluster during the maintenance window\. By default, minor engine upgrades are applied automatically\.  
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZones`  <a name="cfn-rds-dbcluster-availabilityzones"></a>
A list of Availability Zones \(AZs\) where instances in the DB cluster can be created\. For information on AWS Regions and Availability Zones, see [Choosing the Regions and Availability Zones](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Concepts.RegionsAndAvailabilityZones.html) in the *Amazon Aurora User Guide*\.   
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BacktrackWindow`  <a name="cfn-rds-dbcluster-backtrackwindow"></a>
The target backtrack window, in seconds\. To disable backtracking, set this value to 0\.   
Currently, Backtrack is only supported for Aurora MySQL DB clusters\.
Default: 0  
Constraints:  
+ If specified, this value must be set to a number from 0 to 259,200 \(72 hours\)\.
Valid for: Aurora MySQL DB clusters only  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackupRetentionPeriod`  <a name="cfn-rds-dbcluster-backupretentionperiod"></a>
The number of days for which automated backups are retained\.  
Default: 1  
Constraints:  
+ Must be a value from 1 to 35
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CopyTagsToSnapshot`  <a name="cfn-rds-dbcluster-copytagstosnapshot"></a>
A value that indicates whether to copy all tags from the DB cluster to snapshots of the DB cluster\. The default is not to copy them\.  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-rds-dbcluster-databasename"></a>
The name of your database\. If you don't provide a name, then Amazon RDS won't create a database in this DB cluster\. For naming constraints, see [Naming Constraints](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_Limits.html#RDS_Limits.Constraints) in the *Amazon Aurora User Guide*\.   
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
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
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBClusterInstanceClass`  <a name="cfn-rds-dbcluster-dbclusterinstanceclass"></a>
The compute and memory capacity of each DB instance in the Multi\-AZ DB cluster, for example db\.m6gd\.xlarge\. Not all DB instance classes are available in all AWS Regions, or for all database engines\.  
For the full list of DB instance classes and availability for your engine, see [DB instance class](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.DBInstanceClass.html) in the *Amazon RDS User Guide*\.  
This setting is required to create a Multi\-AZ DB cluster\.  
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBClusterParameterGroupName`  <a name="cfn-rds-dbcluster-dbclusterparametergroupname"></a>
The name of the DB cluster parameter group to associate with this DB cluster\.  
If you apply a parameter group to an existing DB cluster, then its DB instances might need to reboot\. This can result in an outage while the DB instances are rebooting\.  
If you apply a change to parameter group associated with a stopped DB cluster, then the update stack waits until the DB cluster is started\.
To list all of the available DB cluster parameter group names, use the following command:  
`aws rds describe-db-cluster-parameter-groups --query "DBClusterParameterGroups[].DBClusterParameterGroupName" --output text`  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBInstanceParameterGroupName`  <a name="cfn-rds-dbcluster-dbinstanceparametergroupname"></a>
The name of the DB parameter group to apply to all instances of the DB cluster\.  
When you apply a parameter group using the `DBInstanceParameterGroupName` parameter, the DB cluster isn't rebooted automatically\. Also, parameter changes are applied immediately rather than during the next maintenance window\.
Default: The existing name setting  
Constraints:  
+ The DB parameter group must be in the same DB parameter group family as this DB cluster\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBSubnetGroupName`  <a name="cfn-rds-dbcluster-dbsubnetgroupname"></a>
A DB subnet group that you want to associate with this DB cluster\.   
If you are restoring a DB cluster to a point in time with `RestoreType` set to `copy-on-write`, and don't specify a DB subnet group name, then the DB cluster is restored with a default DB subnet group\.  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBSystemId`  <a name="cfn-rds-dbcluster-dbsystemid"></a>
Reserved for future use\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeletionProtection`  <a name="cfn-rds-dbcluster-deletionprotection"></a>
A value that indicates whether the DB cluster has deletion protection enabled\. The database can't be deleted when deletion protection is enabled\. By default, deletion protection is disabled\.  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Domain`  <a name="cfn-rds-dbcluster-domain"></a>
Indicates the directory ID of the Active Directory to create the DB cluster\.  
For Amazon Aurora DB clusters, Amazon RDS can use Kerberos authentication to authenticate users that connect to the DB cluster\.  
For more information, see [Kerberos authentication](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/kerberos-authentication.html) in the *Amazon Aurora User Guide*\.  
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainIAMRoleName`  <a name="cfn-rds-dbcluster-domainiamrolename"></a>
Specifies the name of the IAM role to use when making API calls to the Directory Service\.  
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableCloudwatchLogsExports`  <a name="cfn-rds-dbcluster-enablecloudwatchlogsexports"></a>
The list of log types that need to be enabled for exporting to CloudWatch Logs\. The values in the list depend on the DB engine being used\. For more information, see [ Publishing Database Logs to Amazon CloudWatch Logs](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_LogAccess.html#USER_LogAccess.Procedural.UploadtoCloudWatch) in the *Amazon Aurora User Guide*\.  
 **Aurora MySQL**   
Valid values: `audit`, `error`, `general`, `slowquery`   
 **Aurora PostgreSQL**   
Valid values: `postgresql`   
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableHttpEndpoint`  <a name="cfn-rds-dbcluster-enablehttpendpoint"></a>
A value that indicates whether to enable the HTTP endpoint for an Aurora Serverless DB cluster\. By default, the HTTP endpoint is disabled\.  
When enabled, the HTTP endpoint provides a connectionless web service API for running SQL queries on the Aurora Serverless DB cluster\. You can also query your database from inside the RDS console with the query editor\.  
For more information, see [Using the Data API for Aurora Serverless](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/data-api.html) in the *Amazon Aurora User Guide*\.  
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableIAMDatabaseAuthentication`  <a name="cfn-rds-dbcluster-enableiamdatabaseauthentication"></a>
A value that indicates whether to enable mapping of AWS Identity and Access Management \(IAM\) accounts to database accounts\. By default, mapping is disabled\.  
For more information, see [ IAM Database Authentication](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/UsingWithRDS.IAMDBAuth.html) in the *Amazon Aurora User Guide\.*   
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engine`  <a name="cfn-rds-dbcluster-engine"></a>
The name of the database engine to be used for this DB cluster\.  
Valid Values:   
+ `aurora` \(for MySQL 5\.6\-compatible Aurora\)
+ `aurora-mysql` \(for MySQL 5\.7\-compatible and MySQL 8\.0\-compatible Aurora\)
+ `aurora-postgresql`
+ `mysql`
+ `postgres`
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`EngineMode`  <a name="cfn-rds-dbcluster-enginemode"></a>
The DB engine mode of the DB cluster, either `provisioned`, `serverless`, `parallelquery`, `global`, or `multimaster`\.  
The `parallelquery` engine mode isn't required for Aurora MySQL version 1\.23 and higher 1\.x versions, and version 2\.09 and higher 2\.x versions\.  
The `global` engine mode isn't required for Aurora MySQL version 1\.22 and higher 1\.x versions, and `global` engine mode isn't required for any 2\.x versions\.  
The `multimaster` engine mode only applies for DB clusters created with Aurora MySQL version 5\.6\.10a\.  
For Aurora PostgreSQL, the `global` engine mode isn't required, and both the `parallelquery` and the `multimaster` engine modes currently aren't supported\.  
Limitations and requirements apply to some DB engine modes\. For more information, see the following sections in the *Amazon Aurora User Guide*:  
+  [ Limitations of Aurora Serverless](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html#aurora-serverless.limitations) 
+  [ Limitations of Parallel Query](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-mysql-parallel-query.html#aurora-mysql-parallel-query-limitations) 
+  [ Limitations of Aurora Global Databases](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html#aurora-global-database.limitations) 
+  [ Limitations of Multi\-Master Clusters](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-multi-master.html#aurora-multi-master-limitations) 
Valid for: Aurora DB clusters only  
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
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`GlobalClusterIdentifier`  <a name="cfn-rds-dbcluster-globalclusteridentifier"></a>
 If you are configuring an Aurora global database cluster and want your Aurora DB cluster to be a secondary member in the global database cluster, specify the global cluster ID of the global database cluster\. To define the primary database cluster of the global cluster, use the [AWS::RDS::GlobalCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-globalcluster.html) resource\.   
 If you aren't configuring a global database cluster, don't specify this property\.   
To remove the DB cluster from a global database cluster, specify an empty value for the `GlobalClusterIdentifier` property\.
For information about Aurora global databases, see [ Working with Amazon Aurora Global Databases](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html) in the *Amazon Aurora User Guide*\.  
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Iops`  <a name="cfn-rds-dbcluster-iops"></a>
The amount of Provisioned IOPS \(input/output operations per second\) to be initially allocated for each DB instance in the Multi\-AZ DB cluster\.  
For information about valid IOPS values, see [Amazon RDS Provisioned IOPS storage](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Storage.html#USER_PIOPS) in the *Amazon RDS User Guide*\.  
This setting is required to create a Multi\-AZ DB cluster\.  
Constraints: Must be a multiple between \.5 and 50 of the storage amount for the DB cluster\.  
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-rds-dbcluster-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of the AWS KMS key that is used to encrypt the database instances in the DB cluster, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the `StorageEncrypted` property but don't specify this property, the default KMS key is used\. If you specify this property, you must set the `StorageEncrypted` property to `true`\.  
If you specify the `SnapshotIdentifier` property, the `StorageEncrypted` property value is inherited from the snapshot, and if the DB cluster is encrypted, the specified `KmsKeyId` property is used\.  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ManageMasterUserPassword`  <a name="cfn-rds-dbcluster-managemasteruserpassword"></a>
A value that indicates whether to manage the master user password with AWS Secrets Manager\.  
For more information, see [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-secrets-manager.html) in the *Amazon RDS User Guide* and [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-secrets-manager.html) in the *Amazon Aurora User Guide\.*   
Constraints:  
+ Can't manage the master user password with AWS Secrets Manager if `MasterUserPassword` is specified\.
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUsername`  <a name="cfn-rds-dbcluster-masterusername"></a>
The name of the master user for the DB cluster\.  
If you specify the `SourceDBClusterIdentifier`, `SnapshotIdentifier`, or `GlobalClusterIdentifier` property, don't specify this property\. The value is inherited from the source DB cluster, the snapshot, or the primary DB cluster for the global database cluster, respectively\.
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`MasterUserPassword`  <a name="cfn-rds-dbcluster-masteruserpassword"></a>
The master password for the DB instance\.  
If you specify the `SourceDBClusterIdentifier`, `SnapshotIdentifier`, or `GlobalClusterIdentifier` property, don't specify this property\. The value is inherited from the source DB cluster, the snapshot, or the primary DB cluster for the global database cluster, respectively\.
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUserSecret`  <a name="cfn-rds-dbcluster-masterusersecret"></a>
Contains the secret managed by RDS in AWS Secrets Manager for the master user password\.  
For more information, see [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-secrets-manager.html) in the *Amazon RDS User Guide* and [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-secrets-manager.html) in the *Amazon Aurora User Guide\.*   
*Required*: No  
*Type*: [MasterUserSecret](aws-properties-rds-dbcluster-masterusersecret.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringInterval`  <a name="cfn-rds-dbcluster-monitoringinterval"></a>
The interval, in seconds, between points when Enhanced Monitoring metrics are collected for the DB cluster\. To turn off collecting Enhanced Monitoring metrics, specify 0\. The default is 0\.  
If `MonitoringRoleArn` is specified, also set `MonitoringInterval` to a value other than 0\.  
Valid Values: `0, 1, 5, 10, 15, 30, 60`   
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringRoleArn`  <a name="cfn-rds-dbcluster-monitoringrolearn"></a>
The Amazon Resource Name \(ARN\) for the IAM role that permits RDS to send Enhanced Monitoring metrics to Amazon CloudWatch Logs\. An example is `arn:aws:iam:123456789012:role/emaccess`\. For information on creating a monitoring role, see [Setting up and enabling Enhanced Monitoring](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Monitoring.OS.html#USER_Monitoring.OS.Enabling) in the *Amazon RDS User Guide*\.  
If `MonitoringInterval` is set to a value other than 0, supply a `MonitoringRoleArn` value\.  
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkType`  <a name="cfn-rds-dbcluster-networktype"></a>
The network type of the DB cluster\.  
Valid values:  
+  `IPV4` 
+  `DUAL` 
The network type is determined by the `DBSubnetGroup` specified for the DB cluster\. A `DBSubnetGroup` can support only the IPv4 protocol or the IPv4 and IPv6 protocols \(`DUAL`\)\.  
For more information, see [ Working with a DB instance in a VPC](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_VPC.WorkingWithRDSInstanceinaVPC.html) in the *Amazon Aurora User Guide\.*   
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerformanceInsightsEnabled`  <a name="cfn-rds-dbcluster-performanceinsightsenabled"></a>
A value that indicates whether to turn on Performance Insights for the DB cluster\.  
For more information, see [ Using Amazon Performance Insights](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PerfInsights.html) in the *Amazon RDS User Guide*\.  
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerformanceInsightsKmsKeyId`  <a name="cfn-rds-dbcluster-performanceinsightskmskeyid"></a>
The AWS KMS key identifier for encryption of Performance Insights data\.  
The AWS KMS key identifier is the key ARN, key ID, alias ARN, or alias name for the KMS key\.  
If you don't specify a value for `PerformanceInsightsKMSKeyId`, then Amazon RDS uses your default KMS key\. There is a default KMS key for your AWS account\. Your AWS account has a different default KMS key for each AWS Region\.  
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerformanceInsightsRetentionPeriod`  <a name="cfn-rds-dbcluster-performanceinsightsretentionperiod"></a>
The number of days to retain Performance Insights data\. The default is 7 days\. The following values are valid:  
+ 7
+  *month* \* 31, where *month* is a number of months from 1\-23
+ 731
For example, the following values are valid:  
+ 93 \(3 months \* 31\)
+ 341 \(11 months \* 31\)
+ 589 \(19 months \* 31\)
+ 731
If you specify a retention period such as 94, which isn't a valid value, RDS issues an error\.  
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-rds-dbcluster-port"></a>
The port number on which the DB instances in the DB cluster accept connections\.  
Default:  
+ When `EngineMode` is `provisioned`, `3306` \(for both Aurora MySQL and Aurora PostgreSQL\)
+ When `EngineMode` is `serverless`:
  + `3306` when `Engine` is `aurora` or `aurora-mysql`
  + `5432` when `Engine` is `aurora-postgresql`
The `No interruption` on update behavior only applies to DB clusters\. If you are updating a DB instance, see [Port](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-port) for the AWS::RDS::DBInstance resource\.
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredBackupWindow`  <a name="cfn-rds-dbcluster-preferredbackupwindow"></a>
The daily time range during which automated backups are created\. For more information, see [ Backup Window](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Managing.Backups.html#Aurora.Managing.Backups.BackupWindow) in the *Amazon Aurora User Guide\.*   
Constraints:  
+ Must be in the format `hh24:mi-hh24:mi`\.
+ Must be in Universal Coordinated Time \(UTC\)\.
+ Must not conflict with the preferred maintenance window\.
+ Must be at least 30 minutes\.
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-rds-dbcluster-preferredmaintenancewindow"></a>
The weekly time range during which system maintenance can occur, in Universal Coordinated Time \(UTC\)\.  
Format: `ddd:hh24:mi-ddd:hh24:mi`   
The default is a 30\-minute window selected at random from an 8\-hour block of time for each AWS Region, occurring on a random day of the week\. To see the time blocks available, see [ Adjusting the Preferred DB Cluster Maintenance Window](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_UpgradeDBInstance.Maintenance.html#AdjustingTheMaintenanceWindow.Aurora) in the *Amazon Aurora User Guide\.*   
Valid Days: Mon, Tue, Wed, Thu, Fri, Sat, Sun\.  
Constraints: Minimum 30\-minute window\.  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PubliclyAccessible`  <a name="cfn-rds-dbcluster-publiclyaccessible"></a>
A value that indicates whether the DB cluster is publicly accessible\.  
When the DB cluster is publicly accessible, its Domain Name System \(DNS\) endpoint resolves to the private IP address from within the DB cluster's virtual private cloud \(VPC\)\. It resolves to the public IP address from outside of the DB cluster's VPC\. Access to the DB cluster is ultimately controlled by the security group it uses\. That public access isn't permitted if the security group assigned to the DB cluster doesn't permit it\.  
When the DB cluster isn't publicly accessible, it is an internal DB cluster with a DNS name that resolves to a private IP address\.  
Default: The default behavior varies depending on whether `DBSubnetGroupName` is specified\.  
If `DBSubnetGroupName` isn't specified, and `PubliclyAccessible` isn't specified, the following applies:  
+ If the default VPC in the target Region doesn’t have an internet gateway attached to it, the DB cluster is private\.
+ If the default VPC in the target Region has an internet gateway attached to it, the DB cluster is public\.
If `DBSubnetGroupName` is specified, and `PubliclyAccessible` isn't specified, the following applies:  
+ If the subnets are part of a VPC that doesn’t have an internet gateway attached to it, the DB cluster is private\.
+ If the subnets are part of a VPC that has an internet gateway attached to it, the DB cluster is public\.
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplicationSourceIdentifier`  <a name="cfn-rds-dbcluster-replicationsourceidentifier"></a>
The Amazon Resource Name \(ARN\) of the source DB instance or DB cluster if this DB cluster is created as a read replica\.  
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestoreType`  <a name="cfn-rds-dbcluster-restoretype"></a>
The type of restore to be performed\. You can specify one of the following values:  
+  `full-copy` \- The new DB cluster is restored as a full copy of the source DB cluster\.
+  `copy-on-write` \- The new DB cluster is restored as a clone of the source DB cluster\.
Constraints: You can't specify `copy-on-write` if the engine version of the source DB cluster is earlier than 1\.11\.  
If you don't specify a `RestoreType` value, then the new DB cluster is restored as a full copy of the source DB cluster\.  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScalingConfiguration`  <a name="cfn-rds-dbcluster-scalingconfiguration"></a>
The `ScalingConfiguration` property type specifies the scaling configuration of an Aurora Serverless DB cluster\.  
This property is only supported for Aurora Serverless v1\. For Aurora Serverless v2, use `ServerlessV2ScalingConfiguration` property\.  
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: [ScalingConfiguration](aws-properties-rds-dbcluster-scalingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerlessV2ScalingConfiguration`  <a name="cfn-rds-dbcluster-serverlessv2scalingconfiguration"></a>
The `ServerlessV2ScalingConfiguration` property type specifies the scaling configuration of an Aurora Serverless V2 DB cluster\.   
This property is only supported for Aurora Serverless v2\. For Aurora Serverless v1, use `ScalingConfiguration` property\.  
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: [ServerlessV2ScalingConfiguration](aws-properties-rds-dbcluster-serverlessv2scalingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotIdentifier`  <a name="cfn-rds-dbcluster-snapshotidentifier"></a>
The identifier for the DB snapshot or DB cluster snapshot to restore from\.  
You can use either the name or the Amazon Resource Name \(ARN\) to specify a DB cluster snapshot\. However, you can use only the ARN to specify a DB snapshot\.  
After you restore a DB cluster with a `SnapshotIdentifier` property, you must specify the same `SnapshotIdentifier` property for any future updates to the DB cluster\. When you specify this property for an update, the DB cluster is not restored from the snapshot again, and the data in the database is not changed\. However, if you don't specify the `SnapshotIdentifier` property, an empty DB cluster is created, and the original DB cluster is deleted\. If you specify a property that is different from the previous snapshot restore property, a new DB cluster is restored from the specified `SnapshotIdentifier` property, and the original DB cluster is deleted\.  
If you specify the `SnapshotIdentifier` property to restore a DB cluster \(as opposed to specifying it for DB cluster updates\), then don't specify the following properties:  
+ `GlobalClusterIdentifier`
+ `MasterUsername`
+ `MasterUserPassword`
+ `ReplicationSourceIdentifier`
+ `RestoreType`
+ `SourceDBClusterIdentifier`
+ `SourceRegion`
+ `StorageEncrypted` \(for an encrypted snapshot\)
+ `UseLatestRestorableTime`
Constraints:  
+ Must match the identifier of an existing Snapshot\.
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceDBClusterIdentifier`  <a name="cfn-rds-dbcluster-sourcedbclusteridentifier"></a>
When restoring a DB cluster to a point in time, the identifier of the source DB cluster from which to restore\.  
Constraints:  
+ Must match the identifier of an existing DBCluster\.
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceRegion`  <a name="cfn-rds-dbcluster-sourceregion"></a>
The AWS Region which contains the source DB cluster when replicating a DB cluster\. For example, `us-east-1`\.   
Valid for: Aurora DB clusters only  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageEncrypted`  <a name="cfn-rds-dbcluster-storageencrypted"></a>
Indicates whether the DB cluster is encrypted\.  
If you specify the `KmsKeyId` property, then you must enable encryption\.  
If you specify the `SourceDBClusterIdentifier` property, don't specify this property\. The value is inherited from the source DB cluster, and if the DB cluster is encrypted, the specified `KmsKeyId` property is used\.  
If you specify the `SnapshotIdentifier` and the specified snapshot is encrypted, don't specify this property\. The value is inherited from the snapshot, and the specified `KmsKeyId` property is used\.  
If you specify the `SnapshotIdentifier` and the specified snapshot isn't encrypted, you can use this property to specify that the restored DB cluster is encrypted\. Specify the `KmsKeyId` property for the KMS key to use for encryption\. If you don't want the restored DB cluster to be encrypted, then don't set this property or set it to `false`\.  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageType`  <a name="cfn-rds-dbcluster-storagetype"></a>
Specifies the storage type to be associated with the DB cluster\.  
This setting is required to create a Multi\-AZ DB cluster\.  
Valid values: `io1`   
When specified, a value for the `Iops` parameter is required\.  
Default: `io1`   
Valid for: Multi\-AZ DB clusters only  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-rds-dbcluster-tags"></a>
An optional array of key\-value pairs to apply to this DB cluster\.  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseLatestRestorableTime`  <a name="cfn-rds-dbcluster-uselatestrestorabletime"></a>
A value that indicates whether to restore the DB cluster to the latest restorable backup time\. By default, the DB cluster is not restored to the latest restorable backup time\.   
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcSecurityGroupIds`  <a name="cfn-rds-dbcluster-vpcsecuritygroupids"></a>
A list of EC2 VPC security groups to associate with this DB cluster\.  
If you plan to update the resource, don't specify VPC security groups in a shared VPC\.  
Valid for: Aurora DB clusters and Multi\-AZ DB clusters  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rds-dbcluster-return-values"></a>

### Ref<a name="aws-resource-rds-dbcluster-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the DB cluster\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-rds-dbcluster-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-rds-dbcluster-return-values-fn--getatt-fn--getatt"></a>

`DBClusterArn`  <a name="DBClusterArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the DB cluster\.

`DBClusterResourceId`  <a name="DBClusterResourceId-fn::getatt"></a>
The AWS Region\-unique, immutable identifier for the DB cluster\. This identifier is found in AWS CloudTrail log entries whenever the KMS key for the DB cluster is accessed\.

`Endpoint`  <a name="Endpoint-fn::getatt"></a>
The connection endpoint for the primary instance of the DB cluster\.

`Endpoint.Address`  <a name="Endpoint.Address-fn::getatt"></a>
The connection endpoint for the DB cluster\. For example: `mystack-mydbcluster-123456789012.us-east-2.rds.amazonaws.com` 

`Endpoint.Port`  <a name="Endpoint.Port-fn::getatt"></a>
The port number that will accept connections on this DB cluster\. For example: `3306` 

`MasterUserSecret.SecretArn`  <a name="MasterUserSecret.SecretArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the secret\.

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
        "Description" : "Username for PostgreSQL database access",

        "Type" : "String",
        "MinLength" : "1",
        "MaxLength" : "16",
        "AllowedPattern" : "[a-zA-Z][a-zA-Z0-9]*",
        "ConstraintDescription" : "must begin with a letter and contain only alphanumeric characters."
      },
      "DBPassword" : {
        "NoEcho" : "true",
        "Description" : "Password for PostgreSQL database access",

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
    Description: Username for PostgreSQL database access
    Type: String
    MinLength: '1'
    MaxLength: '16'
    AllowedPattern: '[a-zA-Z][a-zA-Z0-9]*'
    ConstraintDescription: must begin with a letter and contain only alphanumeric characters.
  DBPassword:
    NoEcho: 'true'
    Description: Password for PostgreSQL database access
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

### Creating a Multi\-AZ DB cluster<a name="aws-resource-rds-dbcluster--examples--Creating_a_Multi-AZ_DB_cluster"></a>

The following example creates a Multi\-AZ DB cluster\. A Multi\-AZ DB cluster has a writer DB instance and two reader DB instances in three separate Availability Zones in the same AWS Region\. Multi\-AZ DB clusters provide high availability, increased capacity for read workloads, and lower write latency\. You must specify a supported DB engine and DB engine version while creating a Multi\-AZ DB cluster\. For more information, see [Multi\-AZ DB cluster deployments](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/multi-az-db-clusters-concepts.html) in the *Amazon RDS User Guide*\.

#### JSON<a name="aws-resource-rds-dbcluster--examples--Creating_a_Multi-AZ_DB_cluster--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS CloudFormation Sample Template for creating a Multi-AZ DB cluster.",
    "Parameters": {
        "DBUsername": {
            "NoEcho": "true",
            "Description": "Username for database access",
            "Type": "String",
            "MinLength": "1",
            "MaxLength": "16",
            "AllowedPattern": "[a-zA-Z][a-zA-Z0-9]*",
            "ConstraintDescription": "Must begin with a letter and contain only alphanumeric characters."
        },
        "DBPassword": {
            "NoEcho": "true",
            "Description": "Password for database access",
            "Type": "String",
            "MinLength": "8",
            "MaxLength": "41",
            "AllowedPattern": "[a-zA-Z0-9]*",
            "ConstraintDescription": "Must contain only alphanumeric characters."
        },
        "DBClusterIdentifier": {
            "Type": "String"
        },
        "Engine": {
            "Type": "String"
        },
        "EngineVersion": {
            "Type": "String"
        },
        "AllocatedStorage": {
            "Type": "Number"
        },
        "Iops": {
            "Type": "Number"
        }
    },
    "Resources": {
        "MultiAZDBCluster": {
            "Type": "AWS::RDS::DBCluster",
            "Properties": {
                "MasterUsername": {
                    "Ref": "DBUsername"
                },
                "MasterUserPassword": {
                    "Ref": "DBPassword"
                },
                "DBClusterIdentifier": {
                    "Ref": "DBClusterIdentifier"
                },
                "Engine": {
                    "Ref": "Engine"
                },
                "EngineVersion": {
                    "Ref": "EngineVersion"
                },
                "AllocatedStorage": {
                    "Ref": "AllocatedStorage"
                },
                "Iops": {
                    "Ref": "Iops"
                },
                "DBClusterInstanceClass": "db.r6gd.xlarge",
                "BackupRetentionPeriod": 1,
                "StorageType": "io1"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbcluster--examples--Creating_a_Multi-AZ_DB_cluster--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS CloudFormation Sample Template for creating a Multi-AZ DB cluster.
Parameters:
  DBUsername:
    NoEcho: 'true'
    Description: Username for database access
    Type: String
    MinLength: '1'
    MaxLength: '16'
    AllowedPattern: '[a-zA-Z][a-zA-Z0-9]*'
    ConstraintDescription: Must begin with a letter and contain only alphanumeric characters.
  DBPassword:
    NoEcho: 'true'
    Description: Password for database access
    Type: String
    MinLength: '8'
    MaxLength: '41'
    AllowedPattern: '[a-zA-Z0-9]*'
    ConstraintDescription: Must contain only alphanumeric characters.
  DBClusterIdentifier:
    Type: String
  Engine:
    Type: String
  EngineVersion:
    Type: String
  AllocatedStorage:
    Type: Number
  Iops:
    Type: Number
Resources:
  MultiAZDBCluster:
    Type: 'AWS::RDS::DBCluster'
    Properties:
      MasterUsername: !Ref DBUsername
      MasterUserPassword: !Ref DBPassword
      DBClusterIdentifier: !Ref DBClusterIdentifier
      Engine: !Ref Engine
      EngineVersion: !Ref EngineVersion
      AllocatedStorage: !Ref AllocatedStorage
      Iops: !Ref Iops
      DBClusterInstanceClass: db.r6gd.xlarge
      BackupRetentionPeriod: 1
      StorageType: io1
```

### Creating an Amazon Aurora Serverless v2 DB cluster<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_Serverless_v2_DB_cluster"></a>

The following example creates an Amazon Aurora Serverless v2 DB cluster\. Aurora Serverless v2 automates the processes of monitoring the workload and adjusting the capacity for your databases\. It adjusts the capacity in increments to provide the necessary database resources to meet an application's requirements\. For more information, see [Using Amazon Aurora Serverless v2](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless-v2.html) in the *Amazon Aurora User Guide*\.

You must provide a supported engine version when you create an Amazon Aurora Serverless v2 DB cluster\. For more information, see [ Aurora Serverless v2](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Concepts.Aurora_Fea_Regions_DB-eng.Feature.ServerlessV2.html) in the *Amazon Aurora User Guide*\.

**Note**  
This example creates an Aurora MySQL Serverless v2 DB cluster by setting `Engine` to `aurora-mysql`\.

#### JSON<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_Serverless_v2_DB_cluster--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "ServerlessV2 Cluster",
    "Parameters": {
        "MasterUsername": {
            "Type": "String"
        },
        "MasterUserPassword": {
            "Type": "String",
            "NoEcho": true
        },
        "DBClusterIdentifier": {
            "Type": "String"
        },
        "EngineVersion": {
            "Type": "String"
        },
        "MinCapacity": {
            "Type": "String"
        },
        "MaxCapacity": {
            "Type": "String"
        }
    },
    "Resources": {
        "RDSDBCluster": {
            "Type": "AWS::RDS::DBCluster",
            "Properties": {
                "Engine": "aurora-mysql",
                "DBClusterIdentifier": {
                    "Ref": "DBClusterIdentifier"
                },
                "EngineVersion": {
                    "Ref": "EngineVersion"
                },
                "MasterUsername": {
                    "Ref": "MasterUsername"
                },
                "MasterUserPassword": {
                    "Ref": "MasterUserPassword"
                },
                "ServerlessV2ScalingConfiguration": {
                    "MinCapacity": {
                        "Ref": "MinCapacity"
                    },
                    "MaxCapacity": {
                        "Ref": "MaxCapacity"
                    }
                }
            }
        },
        "RDSDBInstance": {
            "Type": "AWS::RDS::DBInstance",
            "Properties": {
                "Engine": "aurora-mysql",
                "DBInstanceClass": "db.serverless",
                "DBClusterIdentifier": {
                    "Ref": "RDSDBCluster"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_Serverless_v2_DB_cluster--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: ServerlessV2 Cluster
Parameters:
  MasterUsername:
    Type: String
  MasterUserPassword:
    Type: String
    NoEcho: true
  DBClusterIdentifier:
    Type: String
  EngineVersion:
    Type: String
  MinCapacity:
    Type: String
  MaxCapacity:
    Type: String
Resources:
  RDSDBCluster:
    Type: 'AWS::RDS::DBCluster'
    Properties:
      Engine: aurora-mysql
      DBClusterIdentifier: !Ref DBClusterIdentifier
      EngineVersion: !Ref EngineVersion
      MasterUsername: !Ref MasterUsername
      MasterUserPassword: !Ref MasterUserPassword
      ServerlessV2ScalingConfiguration:
        MinCapacity: !Ref MinCapacity
        MaxCapacity: !Ref MaxCapacity
   RDSDBInstance:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      Engine: aurora-mysql
      DBInstanceClass: db.serverless
      DBClusterIdentifier: !Ref RDSDBCluster
```

### Creating an Amazon Aurora Serverless v1 DB cluster<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_Serverless_v1_DB_cluster"></a>

The following example creates an Amazon Aurora Serverless v1 DB cluster\. An Aurora Serverless v1 DB cluster is a DB cluster that automatically starts up, shuts down, and scales up or down its compute capacity based on your application's needs\. For more information about Aurora Serverless v1 DB clusters, see [Using Amazon Aurora Serverless](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html) in the *Amazon Aurora User Guide*\.

**Note**  
This example creates an Aurora MySQL Serverless DB cluster by setting `Engine` to `aurora` and `EngineVersion` to `5.6.10a`\. To create an Aurora PostgreSQL Serverless DB cluster, set `Engine` to `aurora-postgresql` and `EngineVersion` to `10.7`\.

#### JSON<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_Serverless_v1_DB_cluster--json"></a>

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

#### YAML<a name="aws-resource-rds-dbcluster--examples--Creating_an_Amazon_Aurora_Serverless_v1_DB_cluster--yaml"></a>

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

### Create a Secrets Manager secret for a master password<a name="aws-resource-rds-dbcluster--examples--Create_a_Secrets_Manager_secret_for_a_master_password"></a>

The following example creates a AWS CloudFormation stack with the AWS::RDS::DBInstance resource with managed master user password feature\. The secret which is used to authenticate the DB instance is shown in the `Secret` stack output\. This output can be removed if showing this value to other CloudFormation stack isn't required\.

For more information about managing password with Secrets Manager, see [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-secrets-manager.html) in the *Amazon RDS User Guide* and [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-secrets-manager.html) in the *Amazon Aurora User Guide*\.

#### JSON<a name="aws-resource-rds-dbcluster--examples--Create_a_Secrets_Manager_secret_for_a_master_password--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "A sample template",
    "Resources": {
        "MyCluster": {
            "Properties": {
                "Engine": "aurora-mysql",
                "MasterUsername": "masteruser",
                "ManageMasterUserPassword": true,
                "MasterUserSecret": {
                    "KmsKeyId": {
                        "Ref": "KMSKey"
                    }
                }
            },
            "Type": "AWS::RDS::DBCluster"
        },
        "MyInstance": {
            "Properties": {
                "DBClusterIdentifier": {
                    "Ref": "MyCluster"
                },
                "DBInstanceClass": "db.t2.small",
                "Engine": "aurora-mysql",
                "PubliclyAccessible": "true"
            },
            "Type": "AWS::RDS::DBInstance"
        },
        "KMSKey": {
            "Type": "AWS::KMS::Key",
            "Properties": {
                "Description": "Manual test KMS key",
                "EnableKeyRotation": true,
                "KeyPolicy": {
                    "Version": "2012-10-17",
                    "Id": {
                        "Ref": "AWS::StackName"
                    },
                    "Statement": [
                        {
                            "Sid": "Allow administration of the key",
                            "Effect": "Allow",
                            "Principal": {
                                "AWS": {
                                    "Fn::Sub": "arn:${AWS::Partition}:iam::${AWS::AccountId}:root"
                                }
                            },
                            "Action": [
                                "kms:*"
                            ],
                            "Resource": "*"
                        }
                    ]
                }
            }
        }
    },
    "Outputs": {
        "Secret": {
            "Value": {
                "Fn::GetAtt": "MyCluster.MasterUserSecret.SecretArn"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbcluster--examples--Create_a_Secrets_Manager_secret_for_a_master_password--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: A sample template
Resources:
  MyCluster:
    Properties:
      Engine: aurora-mysql
      MasterUsername: masteruser
      ManageMasterUserPassword: true
      MasterUserSecret:
        KmsKeyId: !Ref KMSKey
    Type: "AWS::RDS::DBCluster"
  MyInstance:
    Properties:
      DBClusterIdentifier:
        Ref: MyCluster
      DBInstanceClass: db.t2.small
      Engine: aurora-mysql
      PubliclyAccessible: "true"
    Type: "AWS::RDS::DBInstance"
  KMSKey:
    Type: 'AWS::KMS::Key'
    Properties:
      Description: Manual test KMS key
      EnableKeyRotation: True
      KeyPolicy:
        Version: "2012-10-17"
        Id: !Ref "AWS::StackName"
        Statement:
          - Sid: "Allow administration of the key"
            Effect: "Allow"
            Principal:
              AWS:
                Fn::Sub: 'arn:${AWS::Partition}:iam::${AWS::AccountId}:root'
            Action:
              - "kms:*"
            Resource: "*"
Outputs:
  Secret:
    Value:
      Fn::GetAtt: MyCluster.MasterUserSecret.SecretArn
```