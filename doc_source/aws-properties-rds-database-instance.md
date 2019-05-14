# AWS::RDS::DBInstance<a name="aws-properties-rds-database-instance"></a>

The `AWS::RDS::DBInstance` resource creates an Amazon RDS DB instance\.

**Important**  
If a DB instance is deleted or replaced during an update, AWS CloudFormation deletes all automated snapshots\. However, it retains manual DB snapshots\. During an update that requires replacement, you can apply a stack policy to prevent DB instances from being replaced\. For more information, see [Prevent Updates to Stack Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/protect-stack-resources.html)\.

**Updating DB Instances**

When properties labeled "*Update requires:* [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)" are updated, AWS CloudFormation first creates a replacement DB instance, then changes references from other dependent resources to point to the replacement DB instance, and finally deletes the old DB instance\.

**Important**  
We highly recommend that you take a snapshot of the database before updating the stack\. If you don't, you lose the data when AWS CloudFormation replaces your DB instance\. To preserve your data, perform the following procedure:  
Deactivate any applications that are using the DB instance so that there's no activity on the DB instance\.
Create a snapshot of the DB instance\. For more information about creating DB snapshots, see [Creating a DB snapshot](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_CreateSnapshot.html)\.
If you want to restore your instance using a DB snapshot, modify the updated template with your DB instance changes and add the `DBSnapshotIdentifier` property with the ID of the DB snapshot that you want to use\.
Update the stack\.

For more information about updating other properties of this resource, see ` [ModifyDBInstance](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html)`\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.

**Deleting DB Instances**

You can set a deletion policy for your DB instance to control how AWS CloudFormation handles the instance when the stack is deleted\. For Amazon RDS DB instances, you can choose to *retain* the instance, to *delete* the instance, or to *create a snapshot* of the instance\. The default AWS CloudFormation behavior depends on the `DBClusterIdentifier` property:

1. For `AWS::RDS::DBInstance` resources that don't specify the `DBClusterIdentifier` property, AWS CloudFormation saves a snapshot of the DB instance\.

1.  For `AWS::RDS::DBInstance` resources that do specify the `DBClusterIdentifier` property, AWS CloudFormation deletes the DB instance\.

 For more information, see [DeletionPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.

## Syntax<a name="aws-properties-rds-database-instance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-database-instance-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBInstance",
  "Properties" : {
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
      "[DeleteAutomatedBackups](#cfn-rds-dbinstance-deleteautomatedbackups)" : Boolean,
      "[DeletionProtection](#cfn-rds-dbinstance-deletionprotection)" : Boolean,
      "[Domain](#cfn-rds-dbinstance-domain)" : String,
      "[DomainIAMRoleName](#cfn-rds-dbinstance-domainiamrolename)" : String,
      "[EnableCloudwatchLogsExports](#cfn-rds-dbinstance-enablecloudwatchlogsexports)" : [ String, ... ],
      "[EnableIAMDatabaseAuthentication](#cfn-rds-dbinstance-enableiamdatabaseauthentication)" : Boolean,
      "[EnablePerformanceInsights](#cfn-rds-dbinstance-enableperformanceinsights)" : Boolean,
      "[Engine](#cfn-rds-dbinstance-engine)" : String,
      "[EngineVersion](#cfn-rds-dbinstance-engineversion)" : String,
      "[Iops](#cfn-rds-dbinstance-iops)" : Integer,
      "[KmsKeyId](#cfn-rds-dbinstance-kmskeyid)" : String,
      "[LicenseModel](#cfn-rds-dbinstance-licensemodel)" : String,
      "[MasterUserPassword](#cfn-rds-dbinstance-masteruserpassword)" : String,
      "[MasterUsername](#cfn-rds-dbinstance-masterusername)" : String,
      "[MonitoringInterval](#cfn-rds-dbinstance-monitoringinterval)" : Integer,
      "[MonitoringRoleArn](#cfn-rds-dbinstance-monitoringrolearn)" : String,
      "[MultiAZ](#cfn-rds-dbinstance-multiaz)" : Boolean,
      "[OptionGroupName](#cfn-rds-dbinstance-optiongroupname)" : String,
      "[PerformanceInsightsKMSKeyId](#cfn-rds-dbinstance-performanceinsightskmskeyid)" : String,
      "[PerformanceInsightsRetentionPeriod](#cfn-rds-dbinstance-performanceinsightsretentionperiod)" : Integer,
      "[Port](#cfn-rds-dbinstance-port)" : String,
      "[PreferredBackupWindow](#cfn-rds-dbinstance-preferredbackupwindow)" : String,
      "[PreferredMaintenanceWindow](#cfn-rds-dbinstance-preferredmaintenancewindow)" : String,
      "[ProcessorFeatures](#cfn-rds-dbinstance-processorfeatures)" : [ [ProcessorFeature](aws-properties-rds-dbinstance-processorfeature.md), ... ],
      "[PromotionTier](#cfn-rds-dbinstance-promotiontier)" : Integer,
      "[PubliclyAccessible](#cfn-rds-dbinstance-publiclyaccessible)" : Boolean,
      "[SourceDBInstanceIdentifier](#cfn-rds-dbinstance-sourcedbinstanceidentifier)" : String,
      "[SourceRegion](#cfn-rds-dbinstance-sourceregion)" : String,
      "[StorageEncrypted](#cfn-rds-dbinstance-storageencrypted)" : Boolean,
      "[StorageType](#cfn-rds-dbinstance-storagetype)" : String,
      "[Tags](#cfn-rds-dbinstance-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Timezone](#cfn-rds-dbinstance-timezone)" : String,
      "[UseDefaultProcessorFeatures](#cfn-rds-dbinstance-usedefaultprocessorfeatures)" : Boolean,
      "[VPCSecurityGroups](#cfn-rds-dbinstance-vpcsecuritygroups)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-properties-rds-database-instance-syntax.yaml"></a>

```
Type: AWS::RDS::DBInstance
Properties : 
﻿  [AllocatedStorage](#cfn-rds-dbinstance-allocatedstorage) : String
﻿  [AllowMajorVersionUpgrade](#cfn-rds-dbinstance-allowmajorversionupgrade) : Boolean
﻿  [AutoMinorVersionUpgrade](#cfn-rds-dbinstance-autominorversionupgrade) : Boolean
﻿  [AvailabilityZone](#cfn-rds-dbinstance-availabilityzone) : String
﻿  [BackupRetentionPeriod](#cfn-rds-dbinstance-backupretentionperiod) : String
﻿  [CharacterSetName](#cfn-rds-dbinstance-charactersetname) : String
﻿  [CopyTagsToSnapshot](#cfn-rds-dbinstance-copytagstosnapshot) : Boolean
﻿  [DBClusterIdentifier](#cfn-rds-dbinstance-dbclusteridentifier) : String
﻿  [DBInstanceClass](#cfn-rds-dbinstance-dbinstanceclass) : String
﻿  [DBInstanceIdentifier](#cfn-rds-dbinstance-dbinstanceidentifier) : String
﻿  [DBName](#cfn-rds-dbinstance-dbname) : String
﻿  [DBParameterGroupName](#cfn-rds-dbinstance-dbparametergroupname) : String
﻿  [DBSecurityGroups](#cfn-rds-dbinstance-dbsecuritygroups) : 
    - String
﻿  [DBSnapshotIdentifier](#cfn-rds-dbinstance-dbsnapshotidentifier) : String
﻿  [DBSubnetGroupName](#cfn-rds-dbinstance-dbsubnetgroupname) : String
﻿  [DeleteAutomatedBackups](#cfn-rds-dbinstance-deleteautomatedbackups) : Boolean
﻿  [DeletionProtection](#cfn-rds-dbinstance-deletionprotection) : Boolean
﻿  [Domain](#cfn-rds-dbinstance-domain) : String
﻿  [DomainIAMRoleName](#cfn-rds-dbinstance-domainiamrolename) : String
﻿  [EnableCloudwatchLogsExports](#cfn-rds-dbinstance-enablecloudwatchlogsexports) : 
    - String
﻿  [EnableIAMDatabaseAuthentication](#cfn-rds-dbinstance-enableiamdatabaseauthentication) : Boolean
﻿  [EnablePerformanceInsights](#cfn-rds-dbinstance-enableperformanceinsights) : Boolean
﻿  [Engine](#cfn-rds-dbinstance-engine) : String
﻿  [EngineVersion](#cfn-rds-dbinstance-engineversion) : String
﻿  [Iops](#cfn-rds-dbinstance-iops) : Integer
﻿  [KmsKeyId](#cfn-rds-dbinstance-kmskeyid) : String
﻿  [LicenseModel](#cfn-rds-dbinstance-licensemodel) : String
﻿  [MasterUserPassword](#cfn-rds-dbinstance-masteruserpassword) : String
﻿  [MasterUsername](#cfn-rds-dbinstance-masterusername) : String
﻿  [MonitoringInterval](#cfn-rds-dbinstance-monitoringinterval) : Integer
﻿  [MonitoringRoleArn](#cfn-rds-dbinstance-monitoringrolearn) : String
﻿  [MultiAZ](#cfn-rds-dbinstance-multiaz) : Boolean
﻿  [OptionGroupName](#cfn-rds-dbinstance-optiongroupname) : String
﻿  [PerformanceInsightsKMSKeyId](#cfn-rds-dbinstance-performanceinsightskmskeyid) : String
﻿  [PerformanceInsightsRetentionPeriod](#cfn-rds-dbinstance-performanceinsightsretentionperiod) : Integer
﻿  [Port](#cfn-rds-dbinstance-port) : String
﻿  [PreferredBackupWindow](#cfn-rds-dbinstance-preferredbackupwindow) : String
﻿  [PreferredMaintenanceWindow](#cfn-rds-dbinstance-preferredmaintenancewindow) : String
﻿  [ProcessorFeatures](#cfn-rds-dbinstance-processorfeatures) : 
    - [ProcessorFeature](aws-properties-rds-dbinstance-processorfeature.md)
﻿  [PromotionTier](#cfn-rds-dbinstance-promotiontier) : Integer
﻿  [PubliclyAccessible](#cfn-rds-dbinstance-publiclyaccessible) : Boolean
﻿  [SourceDBInstanceIdentifier](#cfn-rds-dbinstance-sourcedbinstanceidentifier) : String
﻿  [SourceRegion](#cfn-rds-dbinstance-sourceregion) : String
﻿  [StorageEncrypted](#cfn-rds-dbinstance-storageencrypted) : Boolean
﻿  [StorageType](#cfn-rds-dbinstance-storagetype) : String
﻿  [Tags](#cfn-rds-dbinstance-tags) : 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
﻿  [Timezone](#cfn-rds-dbinstance-timezone) : String
﻿  [UseDefaultProcessorFeatures](#cfn-rds-dbinstance-usedefaultprocessorfeatures) : Boolean
﻿  [VPCSecurityGroups](#cfn-rds-dbinstance-vpcsecuritygroups) : 
    - String
```

## Properties<a name="aws-properties-rds-database-instance-properties"></a>

`AllocatedStorage`  <a name="cfn-rds-dbinstance-allocatedstorage"></a>
The amount of storage \(in gigabytes\) to be initially allocated for the database instance\.  
If any value is set in the `Iops` parameter, `AllocatedStorage` must be at least 100 GB, which corresponds to the minimum Iops value of 1,000\. If you increase the `Iops` value \(in 1,000 IOPS increments\), then you must also increase the `AllocatedStorage` value \(in 100\-GB increments\)\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowMajorVersionUpgrade`  <a name="cfn-rds-dbinstance-allowmajorversionupgrade"></a>
Indicates that major version upgrades are allowed\. Changing this parameter does not result in an outage and the change is asynchronously applied as soon as possible\.  
Constraints: This parameter must be set to true when specifying a value for the EngineVersion parameter that is a different major version than the DB Instance's current version\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoMinorVersionUpgrade`  <a name="cfn-rds-dbinstance-autominorversionupgrade"></a>
Indicates that minor engine upgrades will be applied automatically to the DB Instance during the maintenance window\.  
Default: `true`   
*Required*: No  
*Type*: Boolean

`AvailabilityZone`  <a name="cfn-rds-dbinstance-availabilityzone"></a>
The Availability Zone that the database instance will be created in\.  
Default: A random, system\-chosen Availability Zone in the endpoint's region\.  
 Example: `us-east-1d`   
 Constraint: The AvailabilityZone parameter cannot be specified if the MultiAZ parameter is set to `true`\. The specified Availability Zone must be in the same region as the current endpoint\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BackupRetentionPeriod`  <a name="cfn-rds-dbinstance-backupretentionperiod"></a>
The number of days for which automated backups are retained\. Setting this parameter to a positive number enables backups\. Setting this parameter to 0 disables automated backups\.  
Default: 1  
Constraints:  
+ Must be a value from 0 to 8
+ Cannot be set to 0 if the DB Instance is a master instance with read replicas
*Required*: No  
*Type*: String

`CharacterSetName`  <a name="cfn-rds-dbinstance-charactersetname"></a>
For supported engines, indicates that the DB Instance should be associated with the specified CharacterSet\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CopyTagsToSnapshot`  <a name="cfn-rds-dbinstance-copytagstosnapshot"></a>
A value that indicates whether to copy tags from the DB instance to snapshots of the DB instance\. By default, tags are not copied\.  
 **Amazon Aurora**   
Not applicable\. Copying tags to snapshots is managed by the DB cluster\. Setting this value for an Aurora DB instance has no effect on the DB cluster setting\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBClusterIdentifier`  <a name="cfn-rds-dbinstance-dbclusteridentifier"></a>
The identifier of the DB cluster that the instance will belong to\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBInstanceClass`  <a name="cfn-rds-dbinstance-dbinstanceclass"></a>
The compute and memory capacity of the DB Instance\.  
 Valid Values: `db.t1.micro | db.m1.small | db.m1.medium | db.m1.large | db.m1.xlarge | db.m2.xlarge |db.m2.2xlarge | db.m2.4xlarge`   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBInstanceIdentifier`  <a name="cfn-rds-dbinstance-dbinstanceidentifier"></a>
A name for the DB instance\. If you specify a name, AWS CloudFormation converts it to lowercase\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the DB instance\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\. 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBName`  <a name="cfn-rds-dbinstance-dbname"></a>
The name of the DB instance that was provided at the time of creation, if one was specified\. This same name is returned for the life of the DB instance\.  
 If you specify the ` [DBSnapshotIdentifier](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsnapshotidentifier)` property, AWS CloudFormation ignores this property\.  
If you restore DB instances from snapshots, this property doesn't apply to the MySQL, PostgreSQL, or MariaDB engines\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBParameterGroupName`  <a name="cfn-rds-dbinstance-dbparametergroupname"></a>
The name of an existing DB parameter group or a reference to an [AWS::RDS::DBParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-dbparametergroup.html) resource created in the template\.  
If any of the data members of the referenced parameter group are changed during an update, the DB instance might need to be restarted, which causes some interruption\. If the parameter group contains static parameters, whether they were changed or not, an update triggers a reboot\.
*Required*: No  
*Type*: String

`DBSecurityGroups`  <a name="cfn-rds-dbinstance-dbsecuritygroups"></a>
A list of the DB security groups to assign to the DB instance\. The list can include both the name of existing DB security groups or references to AWS::RDS::DBSecurityGroup resources created in the template\.  
 If you set DBSecurityGroups, you must not set VPCSecurityGroups, and vice versa\. Also, note that the EC2VpcId property exists only for backwards compatibility with older regions and is no longer recommended for providing security information to an RDS DB instance\. Instead, use VPCSecurityGroups\.  
If you specify this property, AWS CloudFormation sends only the following properties \(if specified\) to Amazon RDS during create operations:  
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
If you specify this property, AWS CloudFormation sends only the following properties \(if specified\) to Amazon RDS during updates:  
+ `AllocatedStorage`
+ `AutoMinorVersionUpgrade`
+ `AllowMajorVersionUpgrade`
+ ` BackupRetentionPeriod`
+ ` DBInstanceClass`
+ ` DBParameterGroupName`
+ ` DBSecurityGroups`
+ `DBInstanceIdentifier`
+ `EngineVersion`
+ `Iops`
+ `MasterUserPassword`
+ `MultiAZ`
+ `OptionGroupName`
+ `PreferredBackupWindow`
+ `PreferredMaintenanceWindow`
All other properties are ignored\. Specify a virtual private cloud \(VPC\) security group if you want to submit other properties, such as `StorageType`, `StorageEncrypted`, or `KmsKeyId`\. If you're already using the `DBSecurityGroups` property, you can't use these other properties by updating your DB instance to use a VPC security group\. You must recreate the DB instance\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBSnapshotIdentifier`  <a name="cfn-rds-dbinstance-dbsnapshotidentifier"></a>
The name or Amazon Resource Name \(ARN\) of the DB snapshot that's used to restore the DB instance\. If you're restoring from a shared manual DB snapshot, you must specify the ARN of the snapshot\.  
By specifying this property, you can create a DB instance from the specified DB snapshot\. If the `DBSnapshotIdentifier` property is an empty string or the `AWS::RDS::DBInstance` declaration has no `DBSnapshotIdentifier` property, AWS CloudFormation creates a new database\. If the property contains a value \(other than an empty string\), AWS CloudFormation creates a database from the specified snapshot\. If a snapshot with the specified name doesn't exist, AWS CloudFormation can't create the database and it rolls back the stack\.  
Some DB instance properties aren't valid when you restore from a snapshot, such as the `MasterUsername` and `MasterUserPassword` properties\. For information about the properties that you can specify, see the `RestoreDBInstanceFromDBSnapshot` action in the *Amazon RDS API Reference*\.  
 If you specify this property, AWS CloudFormation ignores the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbname](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbname) property\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBSubnetGroupName`  <a name="cfn-rds-dbinstance-dbsubnetgroupname"></a>
A DB subnet group to associate with the DB instance\. If you update this value, the new subnet group must be a subnet group in a new VPC\.   
If there's no DB subnet group, then the instance isn't a VPC DB instance\.  
For more information about using Amazon RDS in a VPC, see [Using Amazon RDS with Amazon Virtual Private Cloud \(VPC\)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.html) in the *Amazon Relational Database Service Developer Guide*\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeleteAutomatedBackups`  <a name="cfn-rds-dbinstance-deleteautomatedbackups"></a>
A value that indicates whether to remove automated backups immediately after the DB instance is deleted\. This parameter isn't case\-sensitive\. The default is to remove automated backups immediately after the DB instance is deleted\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeletionProtection`  <a name="cfn-rds-dbinstance-deletionprotection"></a>
A value that indicates whether the DB instance has deletion protection enabled\. The database can't be deleted when deletion protection is enabled\. By default, deletion protection is disabled\. For more information, see [ Deleting a DB Instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_DeleteInstance.html)\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Domain`  <a name="cfn-rds-dbinstance-domain"></a>
For an Amazon RDS DB instance that's running Microsoft SQL Server, this parameter specifies the Active Directory directory ID to create the instance in\. Amazon RDS uses Windows Authentication to authenticate users that connect to the DB instance\. For more information, see [Using Windows Authentication with an Amazon RDS DB Instance Running Microsoft SQL Server](https://docs.aws.amazon.com/AmazonRDS/latest/DeveloperGuide/USER_SQLServerWinAuth.html) in the *Amazon RDS User Guide*\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainIAMRoleName`  <a name="cfn-rds-dbinstance-domainiamrolename"></a>
Specify the name of the IAM role to be used when making API calls to the Directory Service\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableCloudwatchLogsExports`  <a name="cfn-rds-dbinstance-enablecloudwatchlogsexports"></a>
The list of log types that need to be enabled for exporting to CloudWatch Logs\. The values in the list depend on the DB engine being used\. For more information, see [Publishing Database Logs to Amazon CloudWatch Logs ](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_LogAccess.html#USER_LogAccess.Procedural.UploadtoCloudWatch) in the *Amazon Relational Database Service User Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableIAMDatabaseAuthentication`  <a name="cfn-rds-dbinstance-enableiamdatabaseauthentication"></a>
A value that indicates whether to enable mapping of AWS Identity and Access Management \(IAM\) accounts to database accounts\. By default, mapping is disabled\.  
You can enable IAM database authentication for the following database engines:  
 **Amazon Aurora**   
Not applicable\. Mapping AWS IAM accounts to database accounts is managed by the DB cluster\.  
 **MySQL**   
+ For MySQL 5\.6, minor version 5\.6\.34 or higher
+ For MySQL 5\.7, minor version 5\.7\.16 or higher
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnablePerformanceInsights`  <a name="cfn-rds-dbinstance-enableperformanceinsights"></a>
A value that indicates whether to enable Performance Insights for the DB instance\.   
For more information, see [Using Amazon Performance Insights](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PerfInsights.html) in the *Amazon Relational Database Service User Guide*\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engine`  <a name="cfn-rds-dbinstance-engine"></a>
The name of the database engine that you want to use for this DB cluster\. For valid values, see the `Engine` parameter of the [CreateDBCluster](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBCluster.html) action in the *Amazon RDS API Reference*\.  
If you don't specify a value for the `DBClusterParameterGroupName` property and `default.aurora5.6` is used, specifying `aurora.mysql` or `aurora-postgresql` for this property might result in an error\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineVersion`  <a name="cfn-rds-dbinstance-engineversion"></a>
The version number of the database engine to use\.  
 **MySQL**   
Example: `5.1.42`   
Type: String  
 **Oracle**   
Example: `11.2.0.2.v2`   
Type: String  
 **SQL Server**   
Example: `10.50.2789.0.v1`   
*Required*: No  
*Type*: String

`Iops`  <a name="cfn-rds-dbinstance-iops"></a>
The number of I/O operations per second \(IOPS\) that the database provisions\. The value must be equal to or greater than 1000\.   
If you specify this property, you must follow the range of allowed ratios of your requested IOPS rate to the amount of storage that you allocate \(IOPS to allocated storage\)\. For example, you can provision an Oracle database instance with 1000 IOPS and 200 GB of storage \(a ratio of 5:1\), or specify 2000 IOPS with 200 GB of storage \(a ratio of 10:1\)\. For more information, see [Amazon RDS Provisioned IOPS Storage to Improve Performance](https://docs.aws.amazon.com/AmazonRDS/latest/DeveloperGuide/CHAP_Storage.html#USER_PIOPS) in the *Amazon RDS User Guide*\.  
If you specify `io1` for the `StorageType` property, then you must also specify the `Iops` property\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-rds-dbinstance-kmskeyid"></a>
The ARN of the AWS Key Management Service \(AWS KMS\) master key that's used to encrypt the DB instance, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the StorageEncrypted property but don't specify this property, AWS CloudFormation uses the default master key\. If you specify this property, you must set the StorageEncrypted property to true\.   
If you specify the `SourceDBInstanceIdentifier` property, the value is inherited from the source DB instance if the read replica is created in the same region\. If you specify this property when you create a read replica from an unencrypted DB instance, the read replica is encrypted\.  
If you create an encrypted read replica in a different AWS Region, then you must specify a KMS key for the destination AWS Region\. KMS encryption keys are specific to the region that they're created in, and you can't use encryption keys from one region in another region\.  
If you specify `DBSecurityGroups`, AWS CloudFormation ignores this property\. To specify both a security group and this property, you must use a VPC security group\. For more information about Amazon RDS and VPC, see [Using Amazon RDS with Amazon VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) in the *Amazon RDS User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LicenseModel`  <a name="cfn-rds-dbinstance-licensemodel"></a>
License model information for this DB instance\.  
If you've specified `DBSecurityGroups` and then you update the license model, AWS CloudFormation replaces the underlying DB instance\. This will incur some interruptions to database availability\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUserPassword`  <a name="cfn-rds-dbinstance-masteruserpassword"></a>
The password for the master database user\. Can be any printable ASCII character except "/", "\\", or "@"\.  
Type: String  
 **MySQL**   
Constraints: Must contain from 8 to 41 alphanumeric characters\.  
 **Oracle**   
Constraints: Must contain from 8 to 30 alphanumeric characters\.  
 **SQL Server**   
Constraints: Must contain from 8 to 128 alphanumeric characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUsername`  <a name="cfn-rds-dbinstance-masterusername"></a>
The master user name for the DB instance\.  
If you specify the `SourceDBInstanceIdentifier` or `DBSnapshotIdentifier` property, don't specify this property\. The value is inherited from the source DB instance or snapshot\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MonitoringInterval`  <a name="cfn-rds-dbinstance-monitoringinterval"></a>
The interval, in seconds, between points when Enhanced Monitoring metrics are collected for the DB instance\. To disable collecting Enhanced Monitoring metrics, specify 0\. The default is 0\.  
If `MonitoringRoleArn` is specified, then you must also set `MonitoringInterval` to a value other than 0\.  
Valid Values: `0, 1, 5, 10, 15, 30, 60`   
*Required*: No  
*Type*: Integer

`MonitoringRoleArn`  <a name="cfn-rds-dbinstance-monitoringrolearn"></a>
The ARN for the IAM role that permits RDS to send enhanced monitoring metrics to Amazon CloudWatch Logs\. For example, `arn:aws:iam:123456789012:role/emaccess`\. For information on creating a monitoring role, go to [Setting Up and Enabling Enhanced Monitoring](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Monitoring.OS.html#USER_Monitoring.OS.Enabling) in the *Amazon RDS User Guide*\.  
If `MonitoringInterval` is set to a value other than 0, then you must supply a `MonitoringRoleArn` value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiAZ`  <a name="cfn-rds-dbinstance-multiaz"></a>
Specifies whether the database instance is a multiple Availability Zone deployment\. You can't set the `AvailabilityZone` parameter if the `MultiAZ` parameter is set to true\. Amazon Aurora storage is replicated across all the Availability Zones and doesn't require the `MultiAZ` option to be set\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptionGroupName`  <a name="cfn-rds-dbinstance-optiongroupname"></a>
Indicates that the DB Instance should be associated with the specified option group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerformanceInsightsKMSKeyId`  <a name="cfn-rds-dbinstance-performanceinsightskmskeyid"></a>
The AWS KMS key identifier for encryption of Performance Insights data\. The KMS key ID is the Amazon Resource Name \(ARN\), KMS key identifier, or the KMS key alias for the KMS encryption key\.  
If you do not specify a value for `PerformanceInsightsKMSKeyId`, then Amazon RDS uses your default encryption key\. AWS KMS creates the default encryption key for your AWS account\. Your AWS account has a different default encryption key for each AWS Region\.  
*Required*: No  
*Type*: String

`PerformanceInsightsRetentionPeriod`  <a name="cfn-rds-dbinstance-performanceinsightsretentionperiod"></a>
The amount of time, in days, to retain Performance Insights data\. Valid values are 7 or 731 \(2 years\)\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-rds-dbinstance-port"></a>
The port number on which the database accepts connections\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreferredBackupWindow`  <a name="cfn-rds-dbinstance-preferredbackupwindow"></a>
 The daily time range during which automated backups are created if automated backups are enabled, using the `BackupRetentionPeriod` parameter\.   
Default: A 30\-minute window selected at random from an 8\-hour block of time per region\. The following list shows the time blocks for each region from which the default backup windows are assigned\.  
+  **US\-East \(Northern Virginia\) Region:** 03:00\-11:00 UTC
+  **US\-West \(Northern California\) Region:** 06:00\-14:00 UTC
+  **EU \(Ireland\) Region:** 22:00\-06:00 UTC
+  **Asia Pacific \(Singapore\) Region:** 14:00\-22:00 UTC
+  **Asia Pacific \(Tokyo\) Region: ** 17:00\-03:00 UTC
 Constraints: Must be in the format `hh24:mi-hh24:mi`\. Times should be Universal Time Coordinated \(UTC\)\. Must not conflict with the preferred maintenance window\. Must be at least 30 minutes\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-rds-dbinstance-preferredmaintenancewindow"></a>
The weekly time range \(in UTC\) during which system maintenance can occur\.  
This property applies when AWS CloudFormation initially creates the DB instance\. If you use AWS CloudFormation to update the DB instance, those updates are applied immediately\.
*Required*: No  
*Type*: String

`ProcessorFeatures`  <a name="cfn-rds-dbinstance-processorfeatures"></a>
The number of CPU cores and the number of threads per core for the DB instance class of the DB instance\.  
*Required*: No  
*Type*: List of [ProcessorFeature](aws-properties-rds-dbinstance-processorfeature.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PromotionTier`  <a name="cfn-rds-dbinstance-promotiontier"></a>
A value that specifies the order in which an Aurora Replica is promoted to the primary instance after a failure of the existing primary instance\. For more information, see [ Fault Tolerance for an Aurora DB Cluster](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Managing.Backups.html#Aurora.Managing.FaultTolerance) in the *Amazon Aurora User Guide*\.   
Default: 1  
Valid Values: 0 \- 15  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PubliclyAccessible`  <a name="cfn-rds-dbinstance-publiclyaccessible"></a>
 Indicates whether the DB instance is an internet\-facing instance\. If you specify `true`, AWS CloudFormation creates an instance with a publicly resolvable DNS name, which resolves to a public IP address\. If you specify false, AWS CloudFormation creates an internal instance with a DNS name that resolves to a private IP address\.   
 The default behavior value depends on your VPC setup and the database subnet group\. For more information, see the `PubliclyAccessible` parameter in [https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) in the *Amazon RDS API Reference*\.   
 If this resource has a public IP address and is also in a VPC that is defined in the same template, you must use the *DependsOn* attribute to declare a dependency on the VPC\-gateway attachment\. For more information, see [DependsOn Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html)\.   
If you specify DBSecurityGroups, AWS CloudFormation ignores this property\. To specify a security group and this property, you must use a VPC security group\. For more information about Amazon RDS and VPC, see [Using Amazon RDS with Amazon VPC](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.html) in the *Amazon RDS User Guide*\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceDBInstanceIdentifier`  <a name="cfn-rds-dbinstance-sourcedbinstanceidentifier"></a>
If you want to create a read replica DB instance, specify the ID of the source DB instance\. Each DB instance can have a limited number of read replicas\. For more information, see [Working with Read Replicas](https://docs.aws.amazon.com/AmazonRDS/latest/DeveloperGuide/USER_ReadRepl.html) in the *Amazon Relational Database Service Developer Guide*\.   
 The `SourceDBInstanceIdentifier` property determines whether a DB instance is a read replica\. If you remove the `SourceDBInstanceIdentifier` property from your template and then update your stack, AWS CloudFormation deletes the read replica and creates a new DB instance \(not a read replica\)\.   
+ If you specify a source DB instance that uses VPC security groups, we recommend that you specify the `VPCSecurityGroups` property\. If you don't specify the property, the read replica inherits the value of the `VPCSecurityGroups` property from the source DB when you create the replica\. However, if you update the stack, AWS CloudFormation reverts the replica's `VPCSecurityGroups` property to the default value because it's not defined in the stack's template\. This change might cause unexpected issues\.
+ Read replicas don't support deletion policies\. AWS CloudFormation ignores any deletion policy that's associated with a read replica\.
+ If you specify `SourceDBInstanceIdentifier`, don't set the `MultiAZ` property to `true`, and don't specify the `DBSnapshotIdentifier` property\. You can't deploy read replicas in multiple Availability Zones, and you can't create a read replica from a snapshot\.
+  Don't set the `BackupRetentionPeriod`, `DBName`, `MasterUsername`, `MasterUserPassword`, and `PreferredBackupWindow` properties\. The database attributes are inherited from the source DB instance, and backups are disabled for read replicas\.
+ If the source DB instance is in a different region than the read replica, specify an ARN for a valid DB instance\. For more information, see [Constructing a Amazon RDS Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Tagging.html#USER_Tagging.ARN) in the *Amazon RDS User Guide*\.
+ For DB instances in Amazon Aurora clusters, don't specify this property\. Amazon RDS automatically assigns writer and reader DB instances\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceRegion`  <a name="cfn-rds-dbinstance-sourceregion"></a>
The ID of the region that contains the source DB instance for the read replica\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageEncrypted`  <a name="cfn-rds-dbinstance-storageencrypted"></a>
A value that indicates whether the DB instance is encrypted\. By default, it is not encrypted\.  
 **Amazon Aurora**   
Not applicable\. The encryption for DB instances is managed by the DB cluster\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageType`  <a name="cfn-rds-dbinstance-storagetype"></a>
Specifies storage type to be associated with the DB Instance\.  
*Required*: No  
*Type*: String

`Tags`  <a name="cfn-rds-dbinstance-tags"></a>
Tags to assign to the DB instance\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timezone`  <a name="cfn-rds-dbinstance-timezone"></a>
The time zone of the DB instance\. The time zone parameter is currently supported only by [Microsoft SQL Server](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_SQLServer.html#SQLServer.Concepts.General.TimeZone)\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UseDefaultProcessorFeatures`  <a name="cfn-rds-dbinstance-usedefaultprocessorfeatures"></a>
A value that indicates whether the DB instance class of the DB instance uses its default processor features\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCSecurityGroups`  <a name="cfn-rds-dbinstance-vpcsecuritygroups"></a>
A list of the VPC security group IDs to assign to the DB instance\. The list can include both the physical IDs of existing VPC security groups and references to [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resources created in the template\.  
 If you set `VPCSecurityGroups`, you must not set [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsecuritygroups](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsecuritygroups), and vice versa\.  
You can migrate a DB instance in your stack from an RDS DB security group to a VPC security group, but keep the following in mind:  
+ You can't revert to using an RDS security group after you establish a VPC security group membership\.
+ When you migrate your DB instance to VPC security groups, if your stack update rolls back because the DB instance update fails or because an update fails in another AWS CloudFormation resource, the rollback fails because it can't revert to an RDS security group\.
+ To use the properties that are available when you use a VPC security group, you must recreate the DB instance\. If you don't, AWS CloudFormation submits only the property values that are listed in the [ `DBSecurityGroups`](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsecuritygroups) property\.
To avoid this situation, migrate your DB instance to using VPC security groups only when that is the only change in your stack template\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-properties-rds-database-instance-return-values"></a>

### Ref<a name="aws-properties-rds-database-instance-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the DB instance name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-rds-database-instance-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-rds-database-instance-return-values-fn--getatt-fn--getatt"></a>

`Endpoint.Address`  <a name="Endpoint.Address-fn::getatt"></a>
The connection endpoint for the database\. For example: `mystack-mydb-1apw1j4phylrk.cg034hpkmmjt.us-east-2.rds.amazonaws.com` 

`Endpoint.Port`  <a name="Endpoint.Port-fn::getatt"></a>
The port number on which the database accepts connections\. For example: `3306` 

## Examples<a name="aws-properties-rds-database-instance--examples"></a>

### DBInstance with a set MySQL version<a name="aws-properties-rds-database-instance--examples--DBInstance_with_a_set_MySQL_version"></a>

This example shows how to set the MySQL version\. Note the usage of the [DeletionPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html): When this attribute is set to `Snapshot`, AWS CloudFormation takes a snapshot of this DB instance before deleting it during stack deletion\.

This example also sets a tag, to specify a friendly name for the database\.

#### JSON<a name="aws-properties-rds-database-instance--examples--DBInstance_with_a_set_MySQL_version--json"></a>

```
{
    "MyDB": {
        "Type": "AWS::RDS::DBInstance",
        "Properties": {
            "DBName": {
                "Ref": "DBName"
            },
            "AllocatedStorage": {
                "Ref": "DBAllocatedStorage"
            },
            "DBInstanceClass": {
                "Ref": "DBInstanceClass"
            },
            "Engine": "MySQL",
            "EngineVersion": "5.6.13",
            "MasterUsername": {
                "Ref": "DBUser"
            },
            "MasterUserPassword": {
                "Ref": "DBPassword"
            },
            "Tags": [
                {
                    "Key": "Name",
                    "Value": "My SQL Database"
                }
            ]
        },
        "DeletionPolicy": "Snapshot"
    }
}
```

#### YAML<a name="aws-properties-rds-database-instance--examples--DBInstance_with_a_set_MySQL_version--yaml"></a>

```
--- 
MyDB: 
  DeletionPolicy: Snapshot
  Properties: 
    AllocatedStorage: 
      Ref: DBAllocatedStorage
    DBInstanceClass: 
      Ref: DBInstanceClass
    DBName: 
      Ref: DBName
    Engine: MySQL
    EngineVersion: "5.6.13"
    MasterUserPassword: 
      Ref: DBPassword
    MasterUsername: 
      Ref: DBUser
    Tags: 
      - 
        Key: Name
        Value: "My SQL Database"
  Type: "AWS::RDS::DBInstance"
```

### DBInstance with Provisioned IOPS<a name="aws-properties-rds-database-instance--examples--DBInstance_with_Provisioned_IOPS"></a>

This example sets a provisioned IOPS value in the [Iops](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-iops) property\. Note that the [AllocatedStorage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-allocatedstorage) property is set according to the 10:1 ratio between IOPS and GiBs of storage\.

#### JSON<a name="aws-properties-rds-database-instance--examples--DBInstance_with_Provisioned_IOPS--json"></a>

```
{
    "MyDB": {
        "Type": "AWS::RDS::DBInstance",
        "Properties": {
            "AllocatedStorage": "100",
            "DBInstanceClass": "db.m1.small",
            "Engine": "MySQL",
            "EngineVersion": "5.6.13",
            "Iops": "1000",
            "MasterUsername": {
                "Ref": "DBUser"
            },
            "MasterUserPassword": {
                "Ref": "DBPassword"
            }
        }
    }
}
```

#### YAML<a name="aws-properties-rds-database-instance--examples--DBInstance_with_Provisioned_IOPS--yaml"></a>

```
--- 
MyDB: 
  Properties: 
    AllocatedStorage: "100"
    DBInstanceClass: db.m1.small
    Engine: MySQL
    EngineVersion: "5.6.13"
    Iops: "1000"
    MasterUserPassword: 
      Ref: DBPassword
    MasterUsername: 
      Ref: DBUser
  Type: "AWS::RDS::DBInstance"
```

### Cross\-Region Encrypted Read Replica<a name="aws-properties-rds-database-instance--examples--Cross-Region_Encrypted_Read_Replica"></a>

The following example creates an encrypted read replica from a cross\-region source DB instance\. 

#### JSON<a name="aws-properties-rds-database-instance--examples--Cross-Region_Encrypted_Read_Replica--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "RDS Storage Encrypted",
    "Parameters": {
        "SourceDBInstanceIdentifier": {
            "Type": "String"
        },
        "DBInstanceType": {
            "Type": "String"
        },
        "SourceRegion": {
            "Type": "String"
        }
    },
    "Resources": {
        "MyKey": {
            "Type": "AWS::KMS::Key",
            "Properties": {
                "KeyPolicy": {
                    "Version": "2012-10-17",
                    "Id": "key-default-1",
                    "Statement": [
                        {
                            "Sid": "Enable IAM User Permissions",
                            "Effect": "Allow",
                            "Principal": {
                                "AWS": {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "arn:aws:iam::",
                                            {
                                                "Ref": "AWS::AccountId"
                                            },
                                            ":root"
                                        ]
                                    ]
                                }
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
                "DBInstanceClass": {
                    "Ref": "DBInstanceType"
                },
                "SourceDBInstanceIdentifier": {
                    "Ref": "SourceDBInstanceIdentifier"
                },
                "SourceRegion": {
                    "Ref": "SourceRegion"
                },
                "KmsKeyId": {
                    "Ref": "MyKey"
                }
            }
        }
    },
    "Outputs": {
        "InstanceId": {
            "Description": "InstanceId of the newly created RDS Instance",
            "Value": {
                "Ref": "MyDBSmall"
            }
        }
    }
}
```

#### YAML<a name="aws-properties-rds-database-instance--examples--Cross-Region_Encrypted_Read_Replica--yaml"></a>

```
--- 
AWSTemplateFormatVersion: 2010-09-09
Description: "RDS Storage Encrypted"
Outputs: 
  InstanceId: 
    Description: "InstanceId of the newly created RDS Instance"
    Value: MyDBSmall
Parameters: 
  DBInstanceType: 
    Type: String
  SourceDBInstanceIdentifier: 
    Type: String
  SourceRegion: 
    Type: String
Resources: 
  MyDBSmall: 
    Properties: 
      DBInstanceClass: DBInstanceType
      KmsKeyId: MyKey
      SourceDBInstanceIdentifier: SourceDBInstanceIdentifier
      SourceRegion: SourceRegion
    Type: "AWS::RDS::DBInstance"
  MyKey: 
    Properties: 
      KeyPolicy: 
        Id: key-default-1
        Statement: 
          - 
            Action: "kms:*"
            Effect: Allow
            Principal: 
              AWS: 
                - ""
                - 
                  - "arn:aws:iam::"
                  - "AWS::AccountId"
                  - ":root"
            Resource: "*"
            Sid: "Enable IAM User Permissions"
        Version: 2012-10-17
    Type: "AWS::KMS::Key"
```