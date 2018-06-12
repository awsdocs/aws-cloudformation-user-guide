# AWS::RDS::DBInstance<a name="aws-properties-rds-database-instance"></a>

The `AWS::RDS::DBInstance` type creates an Amazon Relational Database Service \(Amazon RDS\) DB instance\. For detailed information about configuring RDS DB instances, see [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html)\.

**Important**  
If a DB instance is deleted or replaced during an update, AWS CloudFormation deletes all automated snapshots\. However, it retains manual DB snapshots\. During an update that requires replacement, you can apply a stack policy to prevent DB instances from being replaced\. For more information, see [Prevent Updates to Stack Resources](protect-stack-resources.md)\.

**Topics**
+ [Syntax](#aws-resource-rds-dbinstance-syntax)
+ [Properties](#aws-properties-rds-database-instance-prop)
+ [Updating and Deleting AWS::RDS::DBInstance Resources](#updating-and-deleting-dbinstance-resources)
+ [Return Values](#aws-properties-rds-database-instance-returnvalues)
+ [Examples](#aws-properties-rds-database-instance-examples)

## Syntax<a name="aws-resource-rds-dbinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbinstance-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBInstance",
  "Properties" :
  {
    "[AllocatedStorage](#cfn-rds-dbinstance-allocatedstorage)" : String,
    "[AllowMajorVersionUpgrade](#cfn-rds-dbinstance-allowmajorversionupgrade)" : Boolean,
    "[AutoMinorVersionUpgrade](#cfn-rds-dbinstance-autominorversionupgrade)" : Boolean,
    "[AvailabilityZone](#cfn-rds-dbinstance-availabilityzone)" : String,
    "[BackupRetentionPeriod](#cfn-rds-dbinstance-backupretentionperiod)" : String,
    "[CharacterSetName](#cfn-rds-dbinstance-charactersetname)" : String,
    "[CopyTagsToSnapshot](#cfn-rds-dbinstance-copytagstosnapshot)" : Boolean,
    "[DBClusterIdentifier](#cfn-rds-dbinstance-dbclusteridentifier)" : String,
    "[DBInstanceClass](#cfn-rds-dbinstance-dbinstanceclass)" : String,
    "[DBInstanceIdentifier](#cfn-rds-dbinstance-dbinstanceidentifier)" : String,
    "[DBName](#cfn-rds-dbinstance-dbname)" : String,
    "[DBParameterGroupName](#cfn-rds-dbinstance-dbparametergroupname)" : String,
    "[DBSecurityGroups](#cfn-rds-dbinstance-dbsecuritygroups)" : [ String, ... ],
    "[DBSnapshotIdentifier](#cfn-rds-dbinstance-dbsnapshotidentifier)" : String,
    "[DBSubnetGroupName](#cfn-rds-dbinstance-dbsubnetgroupname)" : String,
    "[Domain](#cfn-rds-dbinstance-domain)" : String,
    "[DomainIAMRoleName](#cfn-rds-dbinstance-domainIAMRoleName)" : String,
    "[Engine](#cfn-rds-dbinstance-engine)" : String,
    "[EngineVersion](#cfn-rds-dbinstance-engineversion)" : String,
    "[Iops](#cfn-rds-dbinstance-iops)" : Number,
    "[KmsKeyId](#cfn-rds-dbinstance-kmskeyid)" : String,
    "[LicenseModel](#cfn-rds-dbinstance-licensemodel)" : String,
    "[MasterUsername](#cfn-rds-dbinstance-masterusername)" : String,
    "[MasterUserPassword](#cfn-rds-dbinstance-masteruserpassword)" : String,
    "[MonitoringInterval](#cfn-rds-dbinstance-monitoringinterval)" : Integer,
    "[MonitoringRoleArn](#cfn-rds-dbinstance-monitoringrolearn)" : String,
    "[MultiAZ](#cfn-rds-dbinstance-multiaz)" : Boolean,
    "[OptionGroupName](#cfn-rds-dbinstance-optiongroupname)" : String,
    "[Port](#cfn-rds-dbinstance-port)" : String,
    "[PreferredBackupWindow](#cfn-rds-dbinstance-preferredbackupwindow)" : String,
    "[PreferredMaintenanceWindow](#cfn-rds-dbinstance-preferredmaintenancewindow)" : String,
    "[PubliclyAccessible](#cfn-rds-dbinstance-publiclyaccessible)" : Boolean,
    "[SourceDBInstanceIdentifier](#cfn-rds-dbinstance-sourcedbinstanceidentifier)" : String,
    "[SourceRegion](#cfn-rds-dbinstance-sourceregion)" : String,
    "[StorageEncrypted](#cfn-rds-dbinstance-storageencrypted)" : Boolean,
    "[StorageType](#cfn-rds-dbinstance-storagetype)" : String,
    "[Tags](#cfn-rds-dbinstance-tags)" : [ Resource Tag, ... ],
    "[Timezone](#cfn-rds-dbinstance-timezone)" : String,
    "[VPCSecurityGroups](#cfn-rds-dbinstance-vpcsecuritygroups)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-rds-dbinstance-syntax.yaml"></a>

```
Type: "AWS::RDS::DBInstance"
Properties:
  [AllocatedStorage](#cfn-rds-dbinstance-allocatedstorage): String
  [AllowMajorVersionUpgrade](#cfn-rds-dbinstance-allowmajorversionupgrade): Boolean
  [AutoMinorVersionUpgrade](#cfn-rds-dbinstance-autominorversionupgrade): Boolean
  [AvailabilityZone](#cfn-rds-dbinstance-availabilityzone): String
  [BackupRetentionPeriod](#cfn-rds-dbinstance-backupretentionperiod): String
  [CharacterSetName](#cfn-rds-dbinstance-charactersetname): String
  [CopyTagsToSnapshot](#cfn-rds-dbinstance-copytagstosnapshot): Boolean
  [DBClusterIdentifier](#cfn-rds-dbinstance-dbclusteridentifier): String
  [DBInstanceClass](#cfn-rds-dbinstance-dbinstanceclass): String
  [DBInstanceIdentifier](#cfn-rds-dbinstance-dbinstanceidentifier): String
  [DBName](#cfn-rds-dbinstance-dbname): String
  [DBParameterGroupName](#cfn-rds-dbinstance-dbparametergroupname): String
  [DBSecurityGroups](#cfn-rds-dbinstance-dbsecuritygroups):
    - String
  [DBSnapshotIdentifier](#cfn-rds-dbinstance-dbsnapshotidentifier): String
  [DBSubnetGroupName](#cfn-rds-dbinstance-dbsubnetgroupname): String
  [Domain](#cfn-rds-dbinstance-domain): String
  [DomainIAMRoleName](#cfn-rds-dbinstance-domainIAMRoleName): String
  [Engine](#cfn-rds-dbinstance-engine): String
  [EngineVersion](#cfn-rds-dbinstance-engineversion): String
  [Iops](#cfn-rds-dbinstance-iops): Number
  [KmsKeyId](#cfn-rds-dbinstance-kmskeyid): String
  [LicenseModel](#cfn-rds-dbinstance-licensemodel): String
  [MasterUsername](#cfn-rds-dbinstance-masterusername): String
  [MasterUserPassword](#cfn-rds-dbinstance-masteruserpassword): String
  [MonitoringInterval](#cfn-rds-dbinstance-monitoringinterval): Integer
  [MonitoringRoleArn](#cfn-rds-dbinstance-monitoringrolearn): String
  [MultiAZ](#cfn-rds-dbinstance-multiaz): Boolean
  [OptionGroupName](#cfn-rds-dbinstance-optiongroupname): String
  [Port](#cfn-rds-dbinstance-port): String
  [PreferredBackupWindow](#cfn-rds-dbinstance-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-rds-dbinstance-preferredmaintenancewindow): String
  [PubliclyAccessible](#cfn-rds-dbinstance-publiclyaccessible): Boolean
  [SourceDBInstanceIdentifier](#cfn-rds-dbinstance-sourcedbinstanceidentifier): String
  [SourceRegion](#cfn-rds-dbinstance-sourceregion): String
  [StorageEncrypted](#cfn-rds-dbinstance-storageencrypted): Boolean
  [StorageType](#cfn-rds-dbinstance-storagetype): String
  [Tags](#cfn-rds-dbinstance-tags):
    Resource Tag
  [Timezone](#cfn-rds-dbinstance-timezone): String
  [VPCSecurityGroups](#cfn-rds-dbinstance-vpcsecuritygroups):
    - String
```

## Properties<a name="aws-properties-rds-database-instance-prop"></a>

`AllocatedStorage`  <a name="cfn-rds-dbinstance-allocatedstorage"></a>
The allocated storage size, specified in gigabytes \(GB\)\.  
If any value is set in the `Iops` parameter, `AllocatedStorage` must be at least 100 GB, which corresponds to the minimum `Iops` value of 1,000\. If you increase the `Iops` value \(in 1,000 IOPS increments\), then you must also increase the `AllocatedStorage` value \(in 100\-GB increments\)\.  
*Required*: Conditional\. This property is required except when you specify the `DBClusterIdentifier` property or when you create a read replica from AWS CloudFormation by using the `AWS::RDS::DBInstance` resource\. In these cases, don't specify this property\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AllowMajorVersionUpgrade`  <a name="cfn-rds-dbinstance-allowmajorversionupgrade"></a>
If you update the `EngineVersion` property to a version that's different from the DB instance's current major version, set this property to `true`\. For more information, see [ModifyDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html) in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AutoMinorVersionUpgrade`  <a name="cfn-rds-dbinstance-autominorversionupgrade"></a>
Indicates that minor engine upgrades are applied automatically to the DB instance during the maintenance window\. The default value is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. For more information, see [ModifyDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html) in the *Amazon RDS API Reference*\.

`AvailabilityZone`  <a name="cfn-rds-dbinstance-availabilityzone"></a>
The name of the Availability Zone where the DB instance is located\. You can't set the `AvailabilityZone` parameter if the `MultiAZ` parameter is set to `true`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`BackupRetentionPeriod`  <a name="cfn-rds-dbinstance-backupretentionperiod"></a>
The number of days during which automatic DB snapshots are retained\.   
If this DB instance is deleted or replaced during an update, AWS CloudFormation deletes all automated snapshots\. However, it retains manual DB snapshots\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. For more information, see [ModifyDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html) in the *Amazon RDS API Reference*\.

`CharacterSetName`  <a name="cfn-rds-dbinstance-charactersetname"></a>
For supported engines, specifies the character set to associate with the DB instance\. For more information, see [Appendix: Oracle Character Sets Supported in Amazon RDS](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Appendix.OracleCharacterSets.html) in the *Amazon RDS User Guide*\.  
If you specify the `DBSnapshotIdentifier` or `SourceDBInstanceIdentifier` property, don't specify this property\. The value is inherited from the snapshot or source DB instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`CopyTagsToSnapshot`  <a name="cfn-rds-dbinstance-copytagstosnapshot"></a>
Indicates whether to copy all of the user\-defined tags from the DB instance to snapshots of the DB instance\. By default, Amazon RDS doesn't copy tags to snapshots\. Amazon RDS doesn't copy tags with the `aws::` prefix unless it's the DB instance's final snapshot \(the snapshot when you delete the DB instance\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DBClusterIdentifier`  <a name="cfn-rds-dbinstance-dbclusteridentifier"></a>
The name of an existing DB cluster that this instance is associated with\. If you specify this property, specify `aurora` for the `Engine` property and don't specify any of the following properties: `AllocatedStorage`, `BackupRetentionPeriod`, `CharacterSetName`, `DBName`,  `DBSecurityGroups`, `MasterUsername`, `MasterUserPassword`, `OptionGroupName`, `PreferredBackupWindow`, `PreferredMaintenanceWindow`, `Port`, `SourceDBInstanceIdentifier`, `StorageType`, or `VPCSecurityGroups`\.  
Amazon RDS assigns the first DB instance in the cluster as the primary, and additional DB instances as replicas\.  
If you specify this property, the default deletion policy is `Delete`\. Otherwise, the default deletion policy is `Snapshot`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBInstanceClass`  <a name="cfn-rds-dbinstance-dbinstanceclass"></a>
The name of the compute and memory capacity classes of the DB instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`DBInstanceIdentifier`  <a name="cfn-rds-dbinstance-dbinstanceidentifier"></a>
A name for the DB instance\. If you specify a name, AWS CloudFormation converts it to lowercase\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the DB instance\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBName`  <a name="cfn-rds-dbinstance-dbname"></a>
The name of the DB instance that was provided at the time of creation, if one was specified\. This same name is returned for the life of the DB instance\.  
If you specify the `[DBSnapshotIdentifier](#cfn-rds-dbinstance-dbsnapshotidentifier)` property, AWS CloudFormation ignores this property\.  
If you restore DB instances from snapshots, this property doesn't apply to the MySQL, PostgreSQL, or MariaDB engines\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBParameterGroupName`  <a name="cfn-rds-dbinstance-dbparametergroupname"></a>
The name of an existing DB parameter group or a reference to an [AWS::RDS::DBParameterGroup](aws-properties-rds-dbparametergroup.md) resource created in the template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. If any of the data members of the referenced parameter group are changed during an update, the DB instance might need to be restarted, which causes some interruption\. If the parameter group contains static parameters, whether they were changed or not, an update triggers a reboot\.

`DBSecurityGroups`  <a name="cfn-rds-dbinstance-dbsecuritygroups"></a>
A list of the DB security groups to assign to the DB instance\. The list can include both the name of existing DB security groups or references to [AWS::RDS::DBSecurityGroup](aws-properties-rds-security-group.md) resources created in the template\.  
If you set `DBSecurityGroups`, you must not set [VPCSecurityGroups](#cfn-rds-dbinstance-vpcsecuritygroups), and vice versa\. Also, note that the `EC2VpcId` property exists only for backwards compatibility with older regions and is no longer recommended for providing security information to an RDS DB instance\. Instead, use `VPCSecurityGroups`\.  
If you specify this property, AWS CloudFormation sends only the following properties \(if specified\) to Amazon RDS:   
+ `AllocatedStorage`
+ `AutoMinorVersionUpgrade`
+ `AvailabilityZone`
+ `BackupRetentionPeriod`
+ `CharacterSetName`
+ `DBInstanceClass`
+ `DBName`
+ `DBParameterGroupName`
+ `DBSecurityGroups`
+ `DBSubnetGroupName`
+ `Engine`
+ `EngineVersion`
+ `Iops`
+ `LicenseModel`
+ `MasterUsername`
+ `MasterUserPassword`
+ `MultiAZ`
+ `OptionGroupName`
+ `PreferredBackupWindow`
+ `PreferredMaintenanceWindow`
All other properties are ignored\. Specify a virtual private cloud \(VPC\) security group if you want to submit other properties, such as `StorageType`, `StorageEncrypted`, or `KmsKeyId`\. If you're already using the `DBSecurityGroups` property, you can't use these other properties by updating your DB instance to use a VPC security group\. You must recreate the DB instance\.
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DBSnapshotIdentifier`  <a name="cfn-rds-dbinstance-dbsnapshotidentifier"></a>
The name or Amazon Resource Name \(ARN\) of the DB snapshot that's used to restore the DB instance\. If you're restoring from a shared manual DB snapshot, you must specify the ARN of the snapshot\.  
By specifying this property, you can create a DB instance from the specified DB snapshot\. If the `DBSnapshotIdentifier` property is an empty string or the `AWS::RDS::DBInstance` declaration has no `DBSnapshotIdentifier` property, AWS CloudFormation creates a new database\. If the property contains a value \(other than an empty string\), AWS CloudFormation creates a database from the specified snapshot\. If a snapshot with the specified name doesn't exist, AWS CloudFormation can't create the database and it rolls back the stack\.  
Some DB instance properties aren't valid when you restore from a snapshot, such as the `MasterUsername` and `MasterUserPassword` properties\. For information about the properties that you can specify, see the [RestoreDBInstanceFromDBSnapshot](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_RestoreDBInstanceFromDBSnapshot.html) action in the *Amazon RDS API Reference*\.  
If you specify this property, AWS CloudFormation ignores the `[DBName](#cfn-rds-dbinstance-dbname)` property\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBSubnetGroupName`  <a name="cfn-rds-dbinstance-dbsubnetgroupname"></a>
A DB subnet group to associate with the DB instance\. If you update this value, the new subnet group must be a subnet group in a new VPC\.  
If there's no DB subnet group, then the instance isn't a VPC DB instance\.  
For more information about using Amazon RDS in a VPC, see [Using Amazon RDS with Amazon Virtual Private Cloud \(VPC\)](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.html) in the *Amazon Relational Database Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Domain`  <a name="cfn-rds-dbinstance-domain"></a>
For an Amazon RDS DB instance that's running Microsoft SQL Server, the Active Directory directory ID to create the instance in\. Amazon RDS uses Windows Authentication to authenticate users that connect to the DB instance\. For more information, see [Using Windows Authentication with an Amazon RDS DB Instance Running Microsoft SQL Server](http://docs.aws.amazon.com/AmazonRDS/latest/DeveloperGuide/USER_SQLServerWinAuth.html) in the *Amazon RDS User Guide*\.  
If you specify this property, you must specify a SQL Server engine for the `Engine` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DomainIAMRoleName`  <a name="cfn-rds-dbinstance-domainIAMRoleName"></a>
The name of an IAM role that Amazon RDS uses when calling the AWS Directory Service APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Engine`  <a name="cfn-rds-dbinstance-engine"></a>
The database engine that the DB instance uses\. This property is optional when you specify the `DBSnapshotIdentifier` property to create DB instances\.  
For valid values, see the `Engine` parameter of the [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) action in the *Amazon RDS API Reference*\.  
If you specify `aurora` as the database engine, you must also specify the `DBClusterIdentifier` property\.  
If you've specified `oracle-se` or `oracle-se1` as the database engine, you can update the database engine to `oracle-se2` without the database instance being replaced\. For information on the deprecation of support for Oracle version 12\.1\.0\.1, see [Deprecation of Oracle 12\.1\.0\.1](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Oracle.html#Oracle.Concepts.Deprecate.12101) in the *Amazon Relational Database Service User Guide*\.
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EngineVersion`  <a name="cfn-rds-dbinstance-engineversion"></a>
The version number of the database engine that the DB instance uses\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`Iops`  <a name="cfn-rds-dbinstance-iops"></a>
The number of I/O operations per second \(IOPS\) that the database provisions\. The value must be equal to or greater than `1000`\.  
If you specify this property, you must follow the range of allowed ratios of your requested IOPS rate to the amount of storage that you allocate \(IOPS to allocated storage\)\. For example, you can provision an Oracle database instance with `1000` IOPS and `200` GB of storage \(a ratio of 5:1\), or specify 2000 IOPS with 200 GB of storage \(a ratio of 10:1\)\. For more information, see [Amazon RDS Provisioned IOPS Storage to Improve Performance](http://docs.aws.amazon.com/AmazonRDS/latest/DeveloperGuide/CHAP_Storage.html#USER_PIOPS) in the *Amazon RDS User Guide*\.  
*Required*: Conditional\. If you specify `io1` for the `StorageType` property, you must specify this property\.  
*Type*: Number  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KmsKeyId`  <a name="cfn-rds-dbinstance-kmskeyid"></a>
The ARN of the AWS Key Management Service \(AWS KMS\) master key that's used to encrypt the DB instance, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the `StorageEncrypted` property but don't specify this property, AWS CloudFormation uses the default master key\. If you specify this property, you must set the `StorageEncrypted` property to `true`\.  
If you specify the `SourceDBInstanceIdentifier` property, the value is inherited from the source DB instance if the read replica is created in the same region\. If you specify this property when you create a read replica from an unencrypted DB instance, the read replica is encrypted\.  
If you create an encrypted read replica in a different AWS Region, then you must specify a KMS key for the destination AWS Region\. KMS encryption keys are specific to the region that they're created in, and you can't use encryption keys from one region in another region\.  
If you specify `DBSecurityGroups`, AWS CloudFormation ignores this property\. To specify both a security group and this property, you must use a VPC security group\. For more information about Amazon RDS and VPC, see [Using Amazon RDS with Amazon VPC](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.html) in the *Amazon RDS User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LicenseModel`  <a name="cfn-rds-dbinstance-licensemodel"></a>
The license model of the DB instance\.  
If `DBSecurityGroups` is specified, updating the license model requires its replacement\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MasterUsername`  <a name="cfn-rds-dbinstance-masterusername"></a>
The master user name for the DB instance\.  
If you specify the `SourceDBInstanceIdentifier` or `DBSnapshotIdentifier` property, don't specify this property\. The value is inherited from the source DB instance or snapshot\.
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`MasterUserPassword`  <a name="cfn-rds-dbinstance-masteruserpassword"></a>
The master password for the DB instance\.  
If you specify the `SourceDBInstanceIdentifier` or `DBSnapshotIdentifier` property, don't specify this property\. The value is inherited from the source DB instance or snapshot\.
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MonitoringInterval`  <a name="cfn-rds-dbinstance-monitoringinterval"></a>
The interval, in seconds, between points when Amazon RDS collects enhanced monitoring metrics for the DB instance\. To disable metrics collection, specify `0`\.  
For default and valid values, see the `MonitoringInterval` parameter for the [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) action in the *Amazon RDS API Reference*\.  
*Required*: Conditional\. If you specify the `MonitoringRoleArn` property, specify a value other than `0` for `MonitoringInterval`\.  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. For more information, see [ModifyDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html) in the *Amazon RDS API Reference*\.

`MonitoringRoleArn`  <a name="cfn-rds-dbinstance-monitoringrolearn"></a>
The ARN of the AWS Identity and Access Management \(IAM\) role that permits Amazon RDS to send enhanced monitoring metrics to Amazon CloudWatch, for example, `arn:aws:iam::123456789012:role/emaccess`\. For information on creating a monitoring role, see [To create an IAM role for Amazon RDS Enhanced Monitoring](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Monitoring.html#USER_Monitoring.OS.IAMRole) in the *Amazon RDS User Guide*\.  
*Required*: Conditional\. If you specify a value other than `0` for the `MonitoringInterval` property, specify a value for `MonitoringRoleArn`\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MultiAZ`  <a name="cfn-rds-dbinstance-multiaz"></a>
Specifies if the database instance is a multiple Availability Zone deployment\. You can't set the `AvailabilityZone` parameter if the `MultiAZ` parameter is set to true\. Amazon Aurora storage is replicated across all the Availability Zones and doesn't require the `MultiAZ` option to be set\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`OptionGroupName`  <a name="cfn-rds-dbinstance-optiongroupname"></a>
The option group that this DB instance is associated with\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Port`  <a name="cfn-rds-dbinstance-port"></a>
The port for the instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PreferredBackupWindow`  <a name="cfn-rds-dbinstance-preferredbackupwindow"></a>
The daily time range during which automated backups are performed if automated backups are enabled, as determined by the `BackupRetentionPeriod` property\. For valid values, see the `PreferredBackupWindow` parameter for the [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) action in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-rds-dbinstance-preferredmaintenancewindow"></a>
The weekly time range \(in UTC\) during which system maintenance can occur\. For valid values, see the `PreferredMaintenanceWindow` parameter for the [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) action in the *Amazon RDS API Reference*\.  
This property applies when AWS CloudFormation initially creates the DB instance\. If you use AWS CloudFormation to update the DB instance, those updates are applied immediately\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. For more information, see [ModifyDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html) in the *Amazon RDS API Reference*\.

`PubliclyAccessible`  <a name="cfn-rds-dbinstance-publiclyaccessible"></a>
Indicates whether the DB instance is an internet\-facing instance\. If you specify `true`, AWS CloudFormation creates an instance with a publicly resolvable DNS name, which resolves to a public IP address\. If you specify `false`, AWS CloudFormation creates an internal instance with a DNS name that resolves to a private IP address\.   
The default behavior value depends on your VPC setup and the database subnet group\. For more information, see the `PubliclyAccessible` parameter in [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) in the *Amazon RDS API Reference*\.  
If this resource has a public IP address and is also in a VPC that is defined in the same template, you must use the `DependsOn` attribute to declare a dependency on the VPC\-gateway attachment\. For more information, see [DependsOn Attribute](aws-attribute-dependson.md)\.  
If you specify `DBSecurityGroups`, AWS CloudFormation ignores this property\. To specify a security group and this property, you must use a VPC security group\. For more information about Amazon RDS and VPC, see [Using Amazon RDS with Amazon VPC](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.html) in the *Amazon RDS User Guide*\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SourceDBInstanceIdentifier`  <a name="cfn-rds-dbinstance-sourcedbinstanceidentifier"></a>
If you want to create a read replica DB instance, specify the ID of the source DB instance\. Each DB instance can have a limited number of read replicas\. For more information, see [Working with Read Replicas](http://docs.aws.amazon.com/AmazonRDS/latest/DeveloperGuide/USER_ReadRepl.html) in the *Amazon Relational Database Service Developer Guide*\.  
The `SourceDBInstanceIdentifier` property determines whether a DB instance is a read replica\. If you remove the `SourceDBInstanceIdentifier` property from your template and then update your stack, AWS CloudFormation deletes the read replica and creates a new DB instance \(not a read replica\)\.  
+ If you specify a source DB instance that uses VPC security groups, we recommend that you specify the `VPCSecurityGroups` property\. If you don't specify the property, the read replica inherits the value of the `VPCSecurityGroups` property from the source DB when you create the replica\. However, if you update the stack, AWS CloudFormation reverts the replica's `VPCSecurityGroups` property to the default value because it's not defined in the stack's template\. This change might cause unexpected issues\.
+ Read replicas don't support deletion policies\. AWS CloudFormation ignores any deletion policy that's associated with a read replica\.
+ If you specify `SourceDBInstanceIdentifier`, don't set the `MultiAZ` property to `true`, and don't specify the `DBSnapshotIdentifier` property\. You can't deploy read replicas in multiple Availability Zones, and you can't create a read replica from a snapshot\.
+ Don't set the `BackupRetentionPeriod`, `DBName`, `MasterUsername`, `MasterUserPassword`, and `PreferredBackupWindow` properties\. The database attributes are inherited from the source DB instance, and backups are disabled for read replicas\.
+ If the source DB instance is in a different region than the read replica, specify an ARN for a valid DB instance\. For more information, see [Constructing a Amazon RDS Amazon Resource Name \(ARN\)](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Tagging.html#USER_Tagging.ARN) in the *Amazon RDS User Guide*\.
+ For DB instances in Amazon Aurora clusters, don't specify this property\. Amazon RDS automatically assigns writer and reader DB instances\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SourceRegion`  <a name="cfn-rds-dbinstance-sourceregion"></a>
The ID of the region that contains the source DB instance for the read replica\.  
*Required: *No  
*Type: *String  
*Update requires: * [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`StorageEncrypted`  <a name="cfn-rds-dbinstance-storageencrypted"></a>
Indicates whether the DB instance is encrypted\.  
If you specify the `DBClusterIdentifier`, `DBSnapshotIdentifier`, or `SourceDBInstanceIdentifier` property, don't specify this property\. The value is inherited from the cluster, snapshot, or source DB instance\.  
*Required*: Conditional\. If you specify the `KmsKeyId` property, you must enable encryption\.  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`StorageType`  <a name="cfn-rds-dbinstance-storagetype"></a>
The storage type associated with this DB instance\.  
For the default and valid values, see the `StorageType` parameter of the [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) action in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`Tags`  <a name="cfn-rds-dbinstance-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this DB instance\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Timezone`  <a name="cfn-rds-dbinstance-timezone"></a>
The time zone of the DB instance, which you can specify to match the time zone of your applications\. To see which engines support time zones, see the `Timezone` parameter for the [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) action in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`VPCSecurityGroups`  <a name="cfn-rds-dbinstance-vpcsecuritygroups"></a>
A list of the VPC security group IDs to assign to the DB instance\. The list can include both the physical IDs of existing VPC security groups and references to [AWS::EC2::SecurityGroup](aws-properties-ec2-security-group.md) resources created in the template\.  
If you set `VPCSecurityGroups`, you must not set [DBSecurityGroups](#cfn-rds-dbinstance-dbsecuritygroups), and vice versa\.  
You can migrate a DB instance in your stack from an RDS DB security group to a VPC security group, but keep the following in mind:  
+ You can't revert to using an RDS security group after you establish a VPC security group membership\.
+ When you migrate your DB instance to VPC security groups, if your stack update rolls back because the DB instance update fails or because an update fails in another AWS CloudFormation resource, the rollback fails because it can't revert to an RDS security group\.
+ To use the properties that are available when you use a VPC security group, you must recreate the DB instance\. If you don't, AWS CloudFormation submits only the property values that are listed in the [DBSecurityGroups](#cfn-rds-dbinstance-dbsecuritygroups) property\.
 To avoid this situation, migrate your DB instance to using VPC security groups only when that is the only change in your stack template\.
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Updating and Deleting AWS::RDS::DBInstance Resources<a name="updating-and-deleting-dbinstance-resources"></a>

### Updating DB Instances<a name="w3ab2c21c10d956c13b2"></a>

When properties labeled "*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)" are updated, AWS CloudFormation first creates a replacement DB instance, then changes references from other dependent resources to point to the replacement DB instance, and finally deletes the old DB instance\.

**Important**  
We highly recommend that you take a snapshot of the database before updating the stack\. If you don't, you lose the data when AWS CloudFormation replaces your DB instance\. To preserve your data, perform the following procedure:  
Deactivate any applications that are using the DB instance so that there's no activity on the DB instance\.
Create a snapshot of the DB instance\. For more information about creating DB snapshots, see [Creating a DB snapshot](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_CreateSnapshot.html)\.
If you want to restore your instance using a DB snapshot, modify the updated template with your DB instance changes and add the `DBSnapshotIdentifier` property with the ID of the DB snapshot that you want to use\.
Update the stack\.

For more information about updating other properties of this resource, see [ModifyDBInstance](http://docs.aws.amazon.com//AmazonRDS/latest/APIReference/API_ModifyDBInstance.html)\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.

### Deleting DB Instances<a name="w3ab2c21c10d956c13b4"></a>

You can set a deletion policy for your DB instance to control how AWS CloudFormation handles the instance when the stack is deleted\. For Amazon RDS DB instances, you can choose to *retain* the instance, to *delete* the instance, or to *create a snapshot* of the instance\. The default AWS CloudFormation behavior depends on the `DBClusterIdentifier` property:
+ For `AWS::RDS::DBInstance` resources that don't specify the `DBClusterIdentifier` property, AWS CloudFormation saves a snapshot of the DB instance\.
+ For `AWS::RDS::DBInstance` resources that do specify the `DBClusterIdentifier` property, AWS CloudFormation deletes the DB instance\.

For more information, see [DeletionPolicy Attribute](aws-attribute-deletionpolicy.md)\.

## Return Values<a name="aws-properties-rds-database-instance-returnvalues"></a>

### Ref<a name="aws-properties-rds-database-instance-ref"></a>

When you provide the RDS DB instance's logical name to the `Ref` intrinsic function, `Ref` returns the `DBInstanceIdentifier`\. For example: `mystack-mydb-ea5ugmfvuaxg`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-properties-rds-database-instance-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.
+ **Endpoint\.Address**

  The connection endpoint for the database\. For example: `mystack-mydb-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`\.
+ **Endpoint\.Port**

  The port number on which the database accepts connections\. For example: `3306`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-properties-rds-database-instance-examples"></a>

### DBInstance with a set MySQL version, Tags and DeletionPolicy<a name="aws-properties-rds-database-instance-example1"></a>

This example shows how to set the MySQL version that has a `[DeletionPolicy Attribute](aws-attribute-deletionpolicy.md)` set\. With the `DeletionPolicy` set to `Snapshot`, AWS CloudFormation takes a snapshot of this DB instance before deleting it during stack deletion\. A tag that contains a friendly name for the database is also set\.

#### JSON<a name="aws-resource-rds-dbinstance-example.json"></a>

```
"MyDB" : {
   "Type" : "AWS::RDS::DBInstance",
   "Properties" : {
      "DBName" : { "Ref" : "DBName" },
      "AllocatedStorage" : { "Ref" : "DBAllocatedStorage" },
      "DBInstanceClass" : { "Ref" : "DBInstanceClass" },
      "Engine" : "MySQL",
      "EngineVersion" : "5.5",
      "MasterUsername" : { "Ref" : "DBUser" },
      "MasterUserPassword" : { "Ref" : "DBPassword" },
      "Tags" : [ { "Key" : "Name", "Value" : "My SQL Database" } ]
   },
   "DeletionPolicy" : "Snapshot"
}
```

#### YAML<a name="aws-resource-rds-dbinstance-example.yaml"></a>

```
MyDB: 
  Type: "AWS::RDS::DBInstance"
  Properties: 
    DBName: 
      Ref: "DBName"
    AllocatedStorage: 
      Ref: "DBAllocatedStorage"
    DBInstanceClass: 
      Ref: "DBInstanceClass"
    Engine: "MySQL"
    EngineVersion: "5.5"
    MasterUsername: 
      Ref: "DBUser"
    MasterUserPassword: 
      Ref: "DBPassword"
    Tags: 
      - 
        Key: "Name"
        Value: "My SQL Database"
  DeletionPolicy: "Snapshot"
```

### DBInstance with Provisioned IOPS<a name="aws-properties-rds-database-instance-example2"></a>

This example sets a provisioned IOPS value in the [Iops](#cfn-rds-dbinstance-iops) property\. Note that the [AllocatedStorage](#cfn-rds-dbinstance-allocatedstorage) property is set according to the 10:1 ratio between IOPS and GiBs of storage\.

#### JSON<a name="aws-resource-rds-dbinstance-example2.json"></a>

```
"MyDB" : {
   "Type" : "AWS::RDS::DBInstance",
   "Properties" : {
      "AllocatedStorage" : "100",
      "DBInstanceClass" : "db.m1.small",
      "Engine" : "MySQL",
      "EngineVersion" : "5.5",
      "Iops" : "1000",
      "MasterUsername" : { "Ref" : "DBUser" },
      "MasterUserPassword" : { "Ref" : "DBPassword" }
   }
}
```

#### YAML<a name="aws-resource-rds-dbinstance-example2.yaml"></a>

```
MyDB: 
  Type: "AWS::RDS::DBInstance"
  Properties: 
    AllocatedStorage: "100"
    DBInstanceClass: "db.m1.small"
    Engine: "MySQL"
    EngineVersion: "5.5"
    Iops: "1000"
    MasterUsername: 
      Ref: "DBUser"
    MasterUserPassword: 
      Ref: "DBPassword"
```

### Cross\-Region Encrypted Read Replica<a name="aws-properties-rds-database-instance-example3"></a>

The following example creates an encrypted read replica from a cross\-region source DB instance\.

#### JSON<a name="aws-resource-rds-dbinstance-example3.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "RDS Storage Encrypted",
 
  "Parameters": {
    "SourceDBInstanceIdentifier": {
      "Type": "String"
    },
    "DBInstanceType" : {
      "Type" : "String"
    },
    "SourceRegion": {
      "Type": "String"
    }
  },
  "Resources": {
    "MyKey" : {
      "Type" : "AWS::KMS::Key",
      "Properties" : {
        "KeyPolicy" : {
          "Version": "2012-10-17",
          "Id": "key-default-1",
          "Statement": [
            {
              "Sid": "Enable IAM User Permissions",
              "Effect": "Allow",
              "Principal": {
                "AWS": { "Fn::Join" : ["" , ["arn:aws:iam::", {"Ref" : "AWS::AccountId"} ,":root" ]] }
              },
              "Action": "kms:*",
              "Resource": "*"
            }
          ]
        }
      }
    },
    "MyDBSmall": {
      "Type": "AWS::RDS::DBInstance",
      "Properties": {
        "DBInstanceClass": { "Ref" : "DBInstanceType" },
        "SourceDBInstanceIdentifier": { "Ref" : "SourceDBInstanceIdentifier" },
        "SourceRegion": { "Ref" : "SourceRegion" },
        "KmsKeyId" :  { "Ref" : "MyKey" }
      }
    }
  },
  "Outputs" : {
    "InstanceId" : {
      "Description" : "InstanceId of the newly created RDS Instance",
      "Value" : { "Ref" : "MyDBSmall" }
    }
  }
}
```

#### YAML<a name="aws-resource-rds-dbinstance-example3.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: RDS Storage Encrypted
Parameters:
  SourceDBInstanceIdentifier:
    Type: String
  DBInstanceType:
    Type: String
  SourceRegion:
    Type: String
Resources:
  MyKey:
    Type: 'AWS::KMS::Key'
    Properties:
      KeyPolicy:
        Version: 2012-10-17
        Id: key-default-1
        Statement:
          - Sid: Enable IAM User Permissions
            Effect: Allow
            Principal:
              AWS: !Join 
                - ''
                - - 'arn:aws:iam::'
                  - !Ref 'AWS::AccountId'
                  - ':root'
            Action: 'kms:*'
            Resource: '*'
  MyDBSmall:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      DBInstanceClass: !Ref DBInstanceType
      SourceDBInstanceIdentifier: !Ref SourceDBInstanceIdentifier
      SourceRegion: !Ref SourceRegion
      KmsKeyId: !Ref MyKey
Outputs:
  InstanceId:
    Description: InstanceId of the newly created RDS Instance
    Value: !Ref MyDBSmall
```