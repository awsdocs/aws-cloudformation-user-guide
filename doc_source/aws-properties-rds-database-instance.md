# AWS::RDS::DBInstance<a name="aws-properties-rds-database-instance"></a>

The `AWS::RDS::DBInstance` resource creates an Amazon RDS DB instance\.

**Important**  
If a DB instance is deleted or replaced during an update, AWS CloudFormation deletes all automated snapshots\. However, it retains manual DB snapshots\. During an update that requires replacement, you can apply a stack policy to prevent DB instances from being replaced\. For more information, see [Prevent Updates to Stack Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/protect-stack-resources.html)\.

**Updating DB instances**

When properties labeled "*Update requires:* [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)" are updated, AWS CloudFormation first creates a replacement DB instance, then changes references from other dependent resources to point to the replacement DB instance, and finally deletes the old DB instance\.

**Important**  
We highly recommend that you take a snapshot of the database before updating the stack\. If you don't, you lose the data when AWS CloudFormation replaces your DB instance\. To preserve your data, perform the following procedure:  
Deactivate any applications that are using the DB instance so that there's no activity on the DB instance\.
Create a snapshot of the DB instance\. For more information about creating DB snapshots, see [Creating a DB Snapshot](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_CreateSnapshot.html)\.
If you want to restore your instance using a DB snapshot, modify the updated template with your DB instance changes and add the `DBSnapshotIdentifier` property with the ID of the DB snapshot that you want to use\.  
After you restore a DB instance with a `DBSnapshotIdentifier` property, you must specify the same `DBSnapshotIdentifier` property for any future updates to the DB instance\. When you specify this property for an update, the DB instance is not restored from the DB snapshot again, and the data in the database is not changed\. However, if you don't specify the `DBSnapshotIdentifier` property, an empty DB instance is created, and the original DB instance is deleted\. If you specify a property that is different from the previous snapshot restore property, a new DB instance is restored from the specified `DBSnapshotIdentifier` property, and the original DB instance is deleted\.
Update the stack\.

For more information about updating other properties of this resource, see ` [ModifyDBInstance](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html)`\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.

**Deleting DB instances**

For DB instances that are part of an Aurora DB cluster, you can set a deletion policy for your DB instance to control how AWS CloudFormation handles the DB instance when the stack is deleted\. For Amazon RDS DB instances, you can choose to *retain* the DB instance, to *delete* the DB instance, or to *create a snapshot* of the DB instance\. The default AWS CloudFormation behavior depends on the `DBClusterIdentifier` property:

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
      "[AssociatedRoles](#cfn-rds-dbinstance-associatedroles)" : [ DBInstanceRole, ... ],
      "[AutoMinorVersionUpgrade](#cfn-rds-dbinstance-autominorversionupgrade)" : Boolean,
      "[AvailabilityZone](#cfn-rds-dbinstance-availabilityzone)" : String,
      "[BackupRetentionPeriod](#cfn-rds-dbinstance-backupretentionperiod)" : Integer,
      "[CACertificateIdentifier](#cfn-rds-dbinstance-cacertificateidentifier)" : String,
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
      "[MasterUsername](#cfn-rds-dbinstance-masterusername)" : String,
      "[MasterUserPassword](#cfn-rds-dbinstance-masteruserpassword)" : String,
      "[MaxAllocatedStorage](#cfn-rds-dbinstance-maxallocatedstorage)" : Integer,
      "[MonitoringInterval](#cfn-rds-dbinstance-monitoringinterval)" : Integer,
      "[MonitoringRoleArn](#cfn-rds-dbinstance-monitoringrolearn)" : String,
      "[MultiAZ](#cfn-rds-dbinstance-multiaz)" : Boolean,
      "[OptionGroupName](#cfn-rds-dbinstance-optiongroupname)" : String,
      "[PerformanceInsightsKMSKeyId](#cfn-rds-dbinstance-performanceinsightskmskeyid)" : String,
      "[PerformanceInsightsRetentionPeriod](#cfn-rds-dbinstance-performanceinsightsretentionperiod)" : Integer,
      "[Port](#cfn-rds-dbinstance-port)" : String,
      "[PreferredBackupWindow](#cfn-rds-dbinstance-preferredbackupwindow)" : String,
      "[PreferredMaintenanceWindow](#cfn-rds-dbinstance-preferredmaintenancewindow)" : String,
      "[ProcessorFeatures](#cfn-rds-dbinstance-processorfeatures)" : [ ProcessorFeature, ... ],
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
Properties: 
  [AllocatedStorage](#cfn-rds-dbinstance-allocatedstorage): String
  [AllowMajorVersionUpgrade](#cfn-rds-dbinstance-allowmajorversionupgrade): Boolean
  [AssociatedRoles](#cfn-rds-dbinstance-associatedroles): 
    - DBInstanceRole
  [AutoMinorVersionUpgrade](#cfn-rds-dbinstance-autominorversionupgrade): Boolean
  [AvailabilityZone](#cfn-rds-dbinstance-availabilityzone): String
  [BackupRetentionPeriod](#cfn-rds-dbinstance-backupretentionperiod): Integer
  [CACertificateIdentifier](#cfn-rds-dbinstance-cacertificateidentifier): String
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
  [DeleteAutomatedBackups](#cfn-rds-dbinstance-deleteautomatedbackups): Boolean
  [DeletionProtection](#cfn-rds-dbinstance-deletionprotection): Boolean
  [Domain](#cfn-rds-dbinstance-domain): String
  [DomainIAMRoleName](#cfn-rds-dbinstance-domainiamrolename): String
  [EnableCloudwatchLogsExports](#cfn-rds-dbinstance-enablecloudwatchlogsexports): 
    - String
  [EnableIAMDatabaseAuthentication](#cfn-rds-dbinstance-enableiamdatabaseauthentication): Boolean
  [EnablePerformanceInsights](#cfn-rds-dbinstance-enableperformanceinsights): Boolean
  [Engine](#cfn-rds-dbinstance-engine): String
  [EngineVersion](#cfn-rds-dbinstance-engineversion): String
  [Iops](#cfn-rds-dbinstance-iops): Integer
  [KmsKeyId](#cfn-rds-dbinstance-kmskeyid): String
  [LicenseModel](#cfn-rds-dbinstance-licensemodel): String
  [MasterUsername](#cfn-rds-dbinstance-masterusername): String
  [MasterUserPassword](#cfn-rds-dbinstance-masteruserpassword): String
  [MaxAllocatedStorage](#cfn-rds-dbinstance-maxallocatedstorage): Integer
  [MonitoringInterval](#cfn-rds-dbinstance-monitoringinterval): Integer
  [MonitoringRoleArn](#cfn-rds-dbinstance-monitoringrolearn): String
  [MultiAZ](#cfn-rds-dbinstance-multiaz): Boolean
  [OptionGroupName](#cfn-rds-dbinstance-optiongroupname): String
  [PerformanceInsightsKMSKeyId](#cfn-rds-dbinstance-performanceinsightskmskeyid): String
  [PerformanceInsightsRetentionPeriod](#cfn-rds-dbinstance-performanceinsightsretentionperiod): Integer
  [Port](#cfn-rds-dbinstance-port): String
  [PreferredBackupWindow](#cfn-rds-dbinstance-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-rds-dbinstance-preferredmaintenancewindow): String
  [ProcessorFeatures](#cfn-rds-dbinstance-processorfeatures): 
    - ProcessorFeature
  [PromotionTier](#cfn-rds-dbinstance-promotiontier): Integer
  [PubliclyAccessible](#cfn-rds-dbinstance-publiclyaccessible): Boolean
  [SourceDBInstanceIdentifier](#cfn-rds-dbinstance-sourcedbinstanceidentifier): String
  [SourceRegion](#cfn-rds-dbinstance-sourceregion): String
  [StorageEncrypted](#cfn-rds-dbinstance-storageencrypted): Boolean
  [StorageType](#cfn-rds-dbinstance-storagetype): String
  [Tags](#cfn-rds-dbinstance-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Timezone](#cfn-rds-dbinstance-timezone): String
  [UseDefaultProcessorFeatures](#cfn-rds-dbinstance-usedefaultprocessorfeatures): Boolean
  [VPCSecurityGroups](#cfn-rds-dbinstance-vpcsecuritygroups): 
    - String
```

## Properties<a name="aws-properties-rds-database-instance-properties"></a>

`AllocatedStorage`  <a name="cfn-rds-dbinstance-allocatedstorage"></a>
The amount of storage \(in gigabytes\) to be initially allocated for the database instance\.  
If any value is set in the `Iops` parameter, `AllocatedStorage` must be at least 100 GiB, which corresponds to the minimum Iops value of 1,000\. If you increase the `Iops` value \(in 1,000 IOPS increments\), then you must also increase the `AllocatedStorage` value \(in 100\-GiB increments\)\. 
 **Amazon Aurora**   
Not applicable\. Aurora cluster volumes automatically grow as the amount of data in your database increases, though you are only charged for the space that you use in an Aurora cluster volume\.  
 **MySQL**   
Constraints to the amount of storage for each storage type are the following:   
+ General Purpose \(SSD\) storage \(gp2\): Must be an integer from 20 to 65536\.
+ Provisioned IOPS storage \(io1\): Must be an integer from 100 to 65536\.
+ Magnetic storage \(standard\): Must be an integer from 5 to 3072\.
 **MariaDB**   
Constraints to the amount of storage for each storage type are the following:   
+ General Purpose \(SSD\) storage \(gp2\): Must be an integer from 20 to 65536\.
+ Provisioned IOPS storage \(io1\): Must be an integer from 100 to 65536\.
+ Magnetic storage \(standard\): Must be an integer from 5 to 3072\.
 **PostgreSQL**   
Constraints to the amount of storage for each storage type are the following:   
+ General Purpose \(SSD\) storage \(gp2\): Must be an integer from 20 to 65536\.
+ Provisioned IOPS storage \(io1\): Must be an integer from 100 to 65536\.
+ Magnetic storage \(standard\): Must be an integer from 5 to 3072\.
 **Oracle**   
Constraints to the amount of storage for each storage type are the following:   
+ General Purpose \(SSD\) storage \(gp2\): Must be an integer from 20 to 65536\.
+ Provisioned IOPS storage \(io1\): Must be an integer from 100 to 65536\.
+ Magnetic storage \(standard\): Must be an integer from 10 to 3072\.
 **SQL Server**   
Constraints to the amount of storage for each storage type are the following:   
+ General Purpose \(SSD\) storage \(gp2\):
  + Enterprise and Standard editions: Must be an integer from 200 to 16384\.
  + Web and Express editions: Must be an integer from 20 to 16384\.
+ Provisioned IOPS storage \(io1\):
  + Enterprise and Standard editions: Must be an integer from 200 to 16384\.
  + Web and Express editions: Must be an integer from 100 to 16384\.
+ Magnetic storage \(standard\):
  + Enterprise and Standard editions: Must be an integer from 200 to 1024\.
  + Web and Express editions: Must be an integer from 20 to 1024\.
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowMajorVersionUpgrade`  <a name="cfn-rds-dbinstance-allowmajorversionupgrade"></a>
A value that indicates whether major version upgrades are allowed\. Changing this parameter doesn't result in an outage and the change is asynchronously applied as soon as possible\.  
Constraints: Major version upgrades must be allowed when specifying a value for the `EngineVersion` parameter that is a different major version than the DB instance's current version\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssociatedRoles`  <a name="cfn-rds-dbinstance-associatedroles"></a>
 The AWS Identity and Access Management \(IAM\) roles associated with the DB instance\.   
*Required*: No  
*Type*: List of [DBInstanceRole](aws-properties-rds-dbinstance-dbinstancerole.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoMinorVersionUpgrade`  <a name="cfn-rds-dbinstance-autominorversionupgrade"></a>
A value that indicates whether minor engine upgrades are applied automatically to the DB instance during the maintenance window\. By default, minor engine upgrades are applied automatically\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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
**Amazon Aurora**  
Not applicable\. The retention period for automated backups is managed by the DB cluster\.  
Default: 1  
Constraints:  
+ Must be a value from 0 to 35
+ Can't be set to 0 if the DB instance is a source to Read Replicas
*Required*: No  
*Type*: Integer  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`CACertificateIdentifier`  <a name="cfn-rds-dbinstance-cacertificateidentifier"></a>
The identifier of the CA certificate for this DB instance\.  
Specifying or updating this property triggers a reboot\.
For more information about CA certificate identifiers for RDS DB engines, see [ Rotating Your SSL/TLS Certificate](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.SSL-certificate-rotation.html) in the *Amazon RDS User Guide*\.  
For more information about CA certificate identifiers for Aurora DB engines, see [ Rotating Your SSL/TLS Certificate](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/UsingWithRDS.SSL-certificate-rotation.html) in the *Amazon Aurora User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CharacterSetName`  <a name="cfn-rds-dbinstance-charactersetname"></a>
For supported engines, indicates that the DB instance should be associated with the specified character set\.  
 **Amazon Aurora**   
Not applicable\. The character set is managed by the DB cluster\. For more information, see [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)\.  
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
The compute and memory capacity of the DB instance, for example, `db.m4.large`\. Not all DB instance classes are available in all AWS Regions, or for all database engines\.  
For the full list of DB instance classes, and availability for your engine, see [DB Instance Class](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.DBInstanceClass.html) in the *Amazon RDS User Guide\.* For more information about DB instance class pricing and AWS Region support for DB instance classes, see [Amazon RDS Pricing](http://aws.amazon.com/rds/pricing/)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`DBInstanceIdentifier`  <a name="cfn-rds-dbinstance-dbinstanceidentifier"></a>
A name for the DB instance\. If you specify a name, AWS CloudFormation converts it to lowercase\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the DB instance\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\. 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBName`  <a name="cfn-rds-dbinstance-dbname"></a>
The meaning of this parameter differs according to the database engine you use\.  
 If you specify the ` [DBSnapshotIdentifier](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsnapshotidentifier)` property, AWS CloudFormation ignores this property\.  
If you restore DB instances from snapshots, this property doesn't apply to the MySQL, PostgreSQL, or MariaDB engines\.
 **MySQL**   
The name of the database to create when the DB instance is created\. If this parameter is not specified, no database is created in the DB instance\.  
Constraints:  
+ Must contain 1 to 64 letters or numbers\.
+ Can't be a word reserved by the specified database engine
 **MariaDB**   
The name of the database to create when the DB instance is created\. If this parameter is not specified, no database is created in the DB instance\.  
Constraints:  
+ Must contain 1 to 64 letters or numbers\.
+ Can't be a word reserved by the specified database engine
 **PostgreSQL**   
The name of the database to create when the DB instance is created\. If this parameter is not specified, the default "postgres" database is created in the DB instance\.  
Constraints:  
+ Must contain 1 to 63 letters, numbers, or underscores\.
+ Must begin with a letter or an underscore\. Subsequent characters can be letters, underscores, or digits \(0\-9\)\.
+ Can't be a word reserved by the specified database engine
 **Oracle**   
The Oracle System ID \(SID\) of the created DB instance\. If you specify `null`, the default value `ORCL` is used\. You can't specify the string NULL, or any other reserved word, for `DBName`\.   
Default: `ORCL`   
Constraints:  
+ Can't be longer than 8 characters
 **SQL Server**   
Not applicable\. Must be null\.  
 **Amazon Aurora**   
The name of the database to create when the primary instance of the DB cluster is created\. If this parameter is not specified, no database is created in the DB instance\.  
Constraints:  
+ Must contain 1 to 64 letters or numbers\.
+ Can't be a word reserved by the specified database engine
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBParameterGroupName`  <a name="cfn-rds-dbinstance-dbparametergroupname"></a>
The name of an existing DB parameter group or a reference to an [AWS::RDS::DBParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-dbparametergroup.html) resource created in the template\.  
To list all of the available DB parameter group names, use the following command:  
`aws rds describe-db-parameter-groups --query "DBParameterGroups[].DBParameterGroupName" --output text`  
If any of the data members of the referenced parameter group are changed during an update, the DB instance might need to be restarted, which causes some interruption\. If the parameter group contains static parameters, whether they were changed or not, an update triggers a reboot\.
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

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
All other properties are ignored\. Specify a virtual private cloud \(VPC\) security group if you want to submit other properties, such as `StorageType`, `StorageEncrypted`, or `KmsKeyId`\. If you're already using the `DBSecurityGroups` property, you can't use these other properties by updating your DB instance to use a VPC security group\. You must recreate the DB instance\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBSnapshotIdentifier`  <a name="cfn-rds-dbinstance-dbsnapshotidentifier"></a>
The name or Amazon Resource Name \(ARN\) of the DB snapshot that's used to restore the DB instance\. If you're restoring from a shared manual DB snapshot, you must specify the ARN of the snapshot\.  
By specifying this property, you can create a DB instance from the specified DB snapshot\. If the `DBSnapshotIdentifier` property is an empty string or the `AWS::RDS::DBInstance` declaration has no `DBSnapshotIdentifier` property, AWS CloudFormation creates a new database\. If the property contains a value \(other than an empty string\), AWS CloudFormation creates a database from the specified snapshot\. If a snapshot with the specified name doesn't exist, AWS CloudFormation can't create the database and it rolls back the stack\.  
Some DB instance properties aren't valid when you restore from a snapshot, such as the `MasterUsername` and `MasterUserPassword` properties\. For information about the properties that you can specify, see the `RestoreDBInstanceFromDBSnapshot` action in the *Amazon RDS API Reference*\.  
After you restore a DB instance with a `DBSnapshotIdentifier` property, you must specify the same `DBSnapshotIdentifier` property for any future updates to the DB instance\. When you specify this property for an update, the DB instance is not restored from the DB snapshot again, and the data in the database is not changed\. However, if you don't specify the `DBSnapshotIdentifier` property, an empty DB instance is created, and the original DB instance is deleted\. If you specify a property that is different from the previous snapshot restore property, a new DB instance is restored from the specified `DBSnapshotIdentifier` property, and the original DB instance is deleted\.  
If you specify the `DBSnapshotIdentifier` property to restore a DB instance \(as opposed to specifying it for DB instance updates\), then don't specify the following properties:  
+ `AllocatedStorage`
+ `BackupRetentionPeriod`
+ `CharacterSetName`
+ `DBClusterIdentifier`
+ `DBName`
+ `DBSecurityGroups`
+ `DeleteAutomatedBackups`
+ `EnablePerformanceInsights`
+ `EngineVersion`
+ `KmsKeyId`
+ `MasterUsername`
+ `MasterUserPassword`
+ `MaxAllocatedStorage`
+ `MonitoringInterval`
+ `MonitoringRoleArn`
+ `PerformanceInsightsKMSKeyId`
+ `PerformanceInsightsRetentionPeriod`
+ `PreferredBackupWindow`
+ `PreferredMaintenanceWindow`
+ `PromotionTier`
+ `SourceDBInstanceIdentifier`
+ `SourceRegion`
+ `StorageEncrypted`
+ `Timezone`
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBSubnetGroupName`  <a name="cfn-rds-dbinstance-dbsubnetgroupname"></a>
A DB subnet group to associate with the DB instance\. If you update this value, the new subnet group must be a subnet group in a new VPC\.   
If there's no DB subnet group, then the DB instance isn't a VPC DB instance\.  
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
 **Amazon Aurora**   
Not applicable\. You can enable or disable deletion protection for the DB cluster\. For more information, see `CreateDBCluster`\. DB instances in a DB cluster can be deleted even when deletion protection is enabled for the DB cluster\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Domain`  <a name="cfn-rds-dbinstance-domain"></a>
The Active Directory directory ID to create the DB instance in\. Currently, only MySQL, Microsoft SQL Server, Oracle, and PostgreSQL DB instances can be created in an Active Directory Domain\.  
For more information, see [ Kerberos Authentication](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/kerberos-authentication.html) in the *Amazon RDS User Guide*\.  
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
 **Amazon Aurora**   
Not applicable\. CloudWatch Logs exports are managed by the DB cluster\.   
 **MariaDB**   
Possible values are `audit`, `error`, `general`, and `slowquery`\.   
 **Microsoft SQL Server**   
Possible values are `agent` and `error`\.   
 **MySQL**   
Possible values are `audit`, `error`, `general`, and `slowquery`\.   
 **Oracle**   
Possible values are `alert`, `audit`, `listener`, and `trace`\.   
 **PostgreSQL**   
Possible values are `postgresql` and `upgrade`\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableIAMDatabaseAuthentication`  <a name="cfn-rds-dbinstance-enableiamdatabaseauthentication"></a>
A value that indicates whether to enable mapping of AWS Identity and Access Management \(IAM\) accounts to database accounts\. By default, mapping is disabled\.  
This setting doesn't apply to Amazon Aurora\. Mapping AWS IAM accounts to database accounts is managed by the DB cluster\.  
For more information, see [ IAM Database Authentication for MySQL and PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.IAMDBAuth.html) in the *Amazon RDS User Guide\.*   
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
The name of the database engine that you want to use for this DB instance\.  
If you don't specify a value for the `DBParameterGroupName` property, the default DBParameterGroup for the specified engine is used\.
Valid Values:  
+ `aurora` \(for MySQL 5\.6\-compatible Aurora\)
+ `aurora-mysql` \(for MySQL 5\.7\-compatible Aurora\)
+ `aurora-postgresql`
+ `mariadb`
+ `mysql`
+ `oracle-ee`
+ `oracle-se2`
+ `oracle-se1`
+ `oracle-se`
+ `postgres`
+ `sqlserver-ee`
+ `sqlserver-se`
+ `sqlserver-ex`
+ `sqlserver-web`
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`EngineVersion`  <a name="cfn-rds-dbinstance-engineversion"></a>
The version number of the database engine to use\.  
For a list of valid engine versions, use the `DescribeDBEngineVersions` action\.  
The following are the database engines and links to information about the major and minor versions that are available with Amazon RDS\. Not every database engine is available for every AWS Region\.  
 **Amazon Aurora**   
Not applicable\. The version number of the database engine to be used by the DB instance is managed by the DB cluster\.  
**MariaDB**  
See [MariaDB on Amazon RDS Versions](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_MariaDB.html#MariaDB.Concepts.VersionMgmt) in the *Amazon RDS User Guide\.*  
**Microsoft SQL Server**  
See [Microsoft SQL Server Versions on Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_SQLServer.html#SQLServer.Concepts.General.VersionSupport) in the *Amazon RDS User Guide\.*  
**MySQL**  
See [MySQL on Amazon RDS Versions](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_MySQL.html#MySQL.Concepts.VersionMgmt) in the *Amazon RDS User Guide\.*  
**Oracle**  
See [Oracle Database Engine Release Notes](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Appendix.Oracle.PatchComposition.html) in the *Amazon RDS User Guide\.*  
**PostgreSQL**  
See [Supported PostgreSQL Database Versions](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html#PostgreSQL.Concepts.General.DBVersions) in the *Amazon RDS User Guide\.*  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Iops`  <a name="cfn-rds-dbinstance-iops"></a>
The number of I/O operations per second \(IOPS\) that the database provisions\. The value must be equal to or greater than 1000\.   
If you specify this property, you must follow the range of allowed ratios of your requested IOPS rate to the amount of storage that you allocate \(IOPS to allocated storage\)\. For example, you can provision an Oracle database instance with 1000 IOPS and 200 GiB of storage \(a ratio of 5:1\), or specify 2000 IOPS with 200 GiB of storage \(a ratio of 10:1\)\. For more information, see [Amazon RDS Provisioned IOPS Storage to Improve Performance](https://docs.aws.amazon.com/AmazonRDS/latest/DeveloperGuide/CHAP_Storage.html#USER_PIOPS) in the *Amazon RDS User Guide*\.  
If you specify `io1` for the `StorageType` property, then you must also specify the `Iops` property\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-rds-dbinstance-kmskeyid"></a>
The ARN of the AWS Key Management Service \(AWS KMS\) master key that's used to encrypt the DB instance, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the StorageEncrypted property but don't specify this property, AWS CloudFormation uses the default master key\. If you specify this property, you must set the StorageEncrypted property to true\.   
If you specify the `SourceDBInstanceIdentifier` property, the value is inherited from the source DB instance if the Read Replica is created in the same region\.  
If you create an encrypted Read Replica in a different AWS Region, then you must specify a KMS key for the destination AWS Region\. KMS encryption keys are specific to the region that they're created in, and you can't use encryption keys from one region in another region\.  
If you specify `DBSecurityGroups`, AWS CloudFormation ignores this property\. To specify both a security group and this property, you must use a VPC security group\. For more information about Amazon RDS and VPC, see [Using Amazon RDS with Amazon VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) in the *Amazon RDS User Guide*\.  
 **Amazon Aurora**   
Not applicable\. The KMS key identifier is managed by the DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LicenseModel`  <a name="cfn-rds-dbinstance-licensemodel"></a>
License model information for this DB instance\.  
 Valid values: `license-included` \| `bring-your-own-license` \| `general-public-license`   
If you've specified `DBSecurityGroups` and then you update the license model, AWS CloudFormation replaces the underlying DB instance\. This will incur some interruptions to database availability\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUsername`  <a name="cfn-rds-dbinstance-masterusername"></a>
The master user name for the DB instance\.  
If you specify the `SourceDBInstanceIdentifier` or `DBSnapshotIdentifier` property, don't specify this property\. The value is inherited from the source DB instance or snapshot\.
 **Amazon Aurora**   
Not applicable\. The name for the master user is managed by the DB cluster\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUserPassword`  <a name="cfn-rds-dbinstance-masteruserpassword"></a>
The password for the master user\. The password can include any printable ASCII character except "/", """, or "@"\.  
 **Amazon Aurora**   
Not applicable\. The password for the master user is managed by the DB cluster\.  
 **MariaDB**   
Constraints: Must contain from 8 to 41 characters\.  
 **Microsoft SQL Server**   
Constraints: Must contain from 8 to 128 characters\.  
 **MySQL**   
Constraints: Must contain from 8 to 41 characters\.  
 **Oracle**   
Constraints: Must contain from 8 to 30 characters\.  
 **PostgreSQL**   
Constraints: Must contain from 8 to 128 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxAllocatedStorage`  <a name="cfn-rds-dbinstance-maxallocatedstorage"></a>
The upper limit to which Amazon RDS can automatically scale the storage of the DB instance\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringInterval`  <a name="cfn-rds-dbinstance-monitoringinterval"></a>
The interval, in seconds, between points when Enhanced Monitoring metrics are collected for the DB instance\. To disable collecting Enhanced Monitoring metrics, specify 0\. The default is 0\.  
If `MonitoringRoleArn` is specified, then you must also set `MonitoringInterval` to a value other than 0\.  
Valid Values: `0, 1, 5, 10, 15, 30, 60`   
*Required*: No  
*Type*: Integer  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

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
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`OptionGroupName`  <a name="cfn-rds-dbinstance-optiongroupname"></a>
Indicates that the DB instance should be associated with the specified option group\.  
Permanent options, such as the TDE option for Oracle Advanced Security TDE, can't be removed from an option group\. Also, that option group can't be removed from a DB instance once it is associated with a DB instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerformanceInsightsKMSKeyId`  <a name="cfn-rds-dbinstance-performanceinsightskmskeyid"></a>
The AWS KMS key identifier for encryption of Performance Insights data\.  
The AWS KMS key identifier is the key ARN, key ID, alias ARN, or alias name for the AWS KMS customer master key \(CMK\)\.  
If you do not specify a value for `PerformanceInsightsKMSKeyId`, then Amazon RDS uses your default CMK\. There is a default CMK for your AWS account\. Your AWS account has a different default CMK for each AWS Region\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

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
 The daily time range during which automated backups are created if automated backups are enabled, using the `BackupRetentionPeriod` parameter\. For more information, see [The Backup Window](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithAutomatedBackups.html#USER_WorkingWithAutomatedBackups.BackupWindow) in the *Amazon RDS User Guide*\.   
 The default is a 30\-minute window selected at random from an 8\-hour block of time for each AWS Region\. To see the time blocks available, see [ Adjusting the Preferred DB Instance Maintenance Window](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_UpgradeDBInstance.Maintenance.html#AdjustingTheMaintenanceWindow) in the *Amazon RDS User Guide*\.   
Constraints:  
+ Must be in the format `hh24:mi-hh24:mi`\.
+ Must be in Universal Coordinated Time \(UTC\)\.
+ Must not conflict with the preferred maintenance window\.
+ Must be at least 30 minutes\.
 **Amazon Aurora**   
Not applicable\. The daily time range for creating automated backups is managed by the DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-rds-dbinstance-preferredmaintenancewindow"></a>
The weekly time range during which system maintenance can occur, in Universal Coordinated Time \(UTC\)\.  
Format: `ddd:hh24:mi-ddd:hh24:mi`   
The default is a 30\-minute window selected at random from an 8\-hour block of time for each AWS Region, occurring on a random day of the week\. To see the time blocks available, see [ Adjusting the Preferred DB Instance Maintenance Window](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_UpgradeDBInstance.Maintenance.html#AdjustingTheMaintenanceWindow) in the *Amazon RDS User Guide\.*   
This property applies when AWS CloudFormation initially creates the DB instance\. If you use AWS CloudFormation to update the DB instance, those updates are applied immediately\.
Constraints: Minimum 30\-minute window\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

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
If you want to create a Read Replica DB instance, specify the ID of the source DB instance\. Each DB instance can have a limited number of Read Replicas\. For more information, see [Working with Read Replicas](https://docs.aws.amazon.com/AmazonRDS/latest/DeveloperGuide/USER_ReadRepl.html) in the *Amazon Relational Database Service Developer Guide*\.   
 The `SourceDBInstanceIdentifier` property determines whether a DB instance is a Read Replica\. If you remove the `SourceDBInstanceIdentifier` property from your template and then update your stack, AWS CloudFormation deletes the Read Replica and creates a new DB instance \(not a Read Replica\)\.   
+ If you specify a source DB instance that uses VPC security groups, we recommend that you specify the `VPCSecurityGroups` property\. If you don't specify the property, the Read Replica inherits the value of the `VPCSecurityGroups` property from the source DB when you create the replica\. However, if you update the stack, AWS CloudFormation reverts the replica's `VPCSecurityGroups` property to the default value because it's not defined in the stack's template\. This change might cause unexpected issues\.
+ Read Replicas don't support deletion policies\. AWS CloudFormation ignores any deletion policy that's associated with a Read Replica\.
+ If you specify `SourceDBInstanceIdentifier`, don't specify the `DBSnapshotIdentifier` property\. You can't create a Read Replica from a snapshot\.
+  Don't set the `BackupRetentionPeriod`, `DBName`, `MasterUsername`, `MasterUserPassword`, and `PreferredBackupWindow` properties\. The database attributes are inherited from the source DB instance, and backups are disabled for Read Replicas\.
+ If the source DB instance is in a different region than the Read Replica, specify the source region in `SourceRegion`, and specify an ARN for a valid DB instance in `SourceDBInstanceIdentifier`\. For more information, see [Constructing a Amazon RDS Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Tagging.html#USER_Tagging.ARN) in the *Amazon RDS User Guide*\.
+ For DB instances in Amazon Aurora clusters, don't specify this property\. Amazon RDS automatically assigns writer and reader DB instances\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceRegion`  <a name="cfn-rds-dbinstance-sourceregion"></a>
The ID of the region that contains the source DB instance for the Read Replica\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageEncrypted`  <a name="cfn-rds-dbinstance-storageencrypted"></a>
A value that indicates whether the DB instance is encrypted\. By default, it isn't encrypted\.  
 **Amazon Aurora**   
Not applicable\. The encryption for DB instances is managed by the DB cluster\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageType`  <a name="cfn-rds-dbinstance-storagetype"></a>
Specifies the storage type to be associated with the DB instance\.  
 Valid values: `standard | gp2 | io1`   
The `standard` value is also known as magnetic\.  
 If you specify `io1`, you must also include a value for the `Iops` parameter\.   
 Default: `io1` if the `Iops` parameter is specified, otherwise `standard`   
For more information, see [Amazon RDS DB Instance Storage](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Storage.html) in the *Amazon RDS User Guide*\.  
This setting doesn't apply to Amazon Aurora\.
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

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
If you plan to update the resource, don't specify VPC security groups in a shared VPC\.  
 If you set `VPCSecurityGroups`, you must not set [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsecuritygroups](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsecuritygroups), and vice versa\.  
You can migrate a DB instance in your stack from an RDS DB security group to a VPC security group, but keep the following in mind:  
+ You can't revert to using an RDS security group after you establish a VPC security group membership\.
+ When you migrate your DB instance to VPC security groups, if your stack update rolls back because the DB instance update fails or because an update fails in another AWS CloudFormation resource, the rollback fails because it can't revert to an RDS security group\.
+ To use the properties that are available when you use a VPC security group, you must recreate the DB instance\. If you don't, AWS CloudFormation submits only the property values that are listed in the [ `DBSecurityGroups`](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsecuritygroups) property\.
To avoid this situation, migrate your DB instance to using VPC security groups only when that is the only change in your stack template\.   
 **Amazon Aurora**   
Not applicable\. The associated list of EC2 VPC security groups is managed by the DB cluster\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-rds-database-instance-return-values"></a>

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

### Creating a DB instance with Enhanced Monitoring enabled<a name="aws-properties-rds-database-instance--examples--Creating_a_DB_instance_with_Enhanced_Monitoring_enabled"></a>

The following example creates an Amazon RDS MySQL DB instance with Enhanced Monitoring enabled\. The IAM role for Enhanced Monitoring specified in `MonitoringRoleArn` must exist before you run this example\. For more information about Enhanced Monitoring, see [ Enhanced Monitoring](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Monitoring.OS.html) in the *Amazon RDS User Guide*\.

#### JSON<a name="aws-properties-rds-database-instance--examples--Creating_a_DB_instance_with_Enhanced_Monitoring_enabled--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS CloudFormation Sample Template for creating an Amazon RDS DB instance: Sample template showing 
how to create a DB instance with Enhanced Monitoring enabled. **WARNING** This template creates an RDS DB instance. You will 
be billed for the AWS resources used if you create a stack from this template.",
    "Parameters": {
        "DBInstanceID": {
            "Default": "mydbinstance",
            "Description": "My database instance",
            "Type": "String",
            "MinLength": "1",
            "MaxLength": "63",
            "AllowedPattern": "[a-zA-Z][a-zA-Z0-9]*",
            "ConstraintDescription": "Must begin with a letter and must not end with a hyphen or contain two consecutive hyphens."
        },
        "DBName": {
            "Default": "mydb",
            "Description": "My database",
            "Type": "String",
            "MinLength": "1",
            "MaxLength": "64",
            "AllowedPattern": "[a-zA-Z][a-zA-Z0-9]*",
            "ConstraintDescription": "Must begin with a letter and contain only alphanumeric characters."
        },
        "DBInstanceClass": {
            "Default": "db.m5.large",
            "Description": "DB instance class",
            "Type": "String",
            "ConstraintDescription": "Must select a valid DB instance type."
        },
        "DBAllocatedStorage": {
            "Default": "50",
            "Description": "The size of the database (GiB)",
            "Type": "Number",
            "MinValue": "5",
            "MaxValue": "1024",
            "ConstraintDescription": "must be between 20 and 65536 GiB."
        },
        "DBUsername": {
            "NoEcho": "true",
            "Description": "Username for MySQL database access",
            "Type": "String",
            "MinLength": "1",
            "MaxLength": "16",
            "AllowedPattern": "[a-zA-Z][a-zA-Z0-9]*",
            "ConstraintDescription": "must begin with a letter and contain only alphanumeric characters."
        },
        "DBPassword": {
            "NoEcho": "true",
            "Description": "Password MySQL database access",
            "Type": "String",
            "MinLength": "8",
            "MaxLength": "41",
            "AllowedPattern": "[a-zA-Z0-9]*",
            "ConstraintDescription": "must contain only alphanumeric characters."
        }
    },
    "Resources": {
        "MyDB": {
            "Type": "AWS::RDS::DBInstance",
            "Properties": {
                "DBInstanceIdentifier": {
                    "Ref": "DBInstanceID"
                },
                "DBName": {
                    "Ref": "DBName"
                },
                "DBInstanceClass": {
                    "Ref": "DBInstanceClass"
                },
                "AllocatedStorage": {
                    "Ref": "DBAllocatedStorage"
                },
                "Engine": "MySQL",
                "EngineVersion": "8.0.16",
                "MasterUsername": {
                    "Ref": "DBUsername"
                },
                "MasterUserPassword": {
                    "Ref": "DBPassword"
                },
                "MonitoringInterval": "60",
                "MonitoringRoleArn": "arn:aws:iam::1233456789012:role/rds-monitoring-role"
            }
        }
    }
}
```

#### YAML<a name="aws-properties-rds-database-instance--examples--Creating_a_DB_instance_with_Enhanced_Monitoring_enabled--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: >-
  Description": "AWS CloudFormation Sample Template for creating an Amazon RDS DB instance: 
  Sample template showing how to create a DB instance with Enhanced Monitoring enabled. 
  **WARNING** This template creates an RDS DB instance. You will be billed for the AWS 
  resources used if you create a stack from this template.
Parameters:
  DBInstanceID:
    Default: mydbinstance
    Description: My database instance
    Type: String
    MinLength: '1'
    MaxLength: '63'
    AllowedPattern: '[a-zA-Z][a-zA-Z0-9]*'
    ConstraintDescription: >-
      Must begin with a letter and must not end with a hyphen or contain two
      consecutive hyphens.
  DBName:
    Default: mydb
    Description: My database
    Type: String
    MinLength: '1'
    MaxLength: '64'
    AllowedPattern: '[a-zA-Z][a-zA-Z0-9]*'
    ConstraintDescription: Must begin with a letter and contain only alphanumeric characters.
  DBInstanceClass:
    Default: db.m5.large
    Description: DB instance class
    Type: String
    ConstraintDescription: Must select a valid DB instance type.
  DBAllocatedStorage:
    Default: '50'
    Description: The size of the database (GiB)
    Type: Number
    MinValue: '5'
    MaxValue: '1024'
    ConstraintDescription: must be between 20 and 65536 GiB.
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
  MyDB:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      DBInstanceIdentifier: !Ref DBInstanceID
      DBName: !Ref DBName
      DBInstanceClass: !Ref DBInstanceClass
      AllocatedStorage: !Ref DBAllocatedStorage
      Engine: MySQL
      EngineVersion: 8.0.16
      MasterUsername: !Ref DBUsername
      MasterUserPassword: !Ref DBPassword
      MonitoringInterval: '60'
      MonitoringRoleArn: 'arn:aws:iam::123456789012:role/rds-monitoring-role'
```

### Creating a cross\-region encrypted read replica<a name="aws-properties-rds-database-instance--examples--Creating_a_cross-region_encrypted_read_replica"></a>

The following example creates an encrypted Read Replica from a cross\-region source DB instance\. 

#### JSON<a name="aws-properties-rds-database-instance--examples--Creating_a_cross-region_encrypted_read_replica--json"></a>

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

#### YAML<a name="aws-properties-rds-database-instance--examples--Creating_a_cross-region_encrypted_read_replica--yaml"></a>

```
--- 
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
    Type: "AWS::KMS::Key"
    Properties:
      KeyPolicy:
        Version: 2012-10-17
        Id: key-default-1
        Statement:
          - Sid: Enable IAM User Permissions
            Effect: Allow
            Principal:
              AWS: !Join
                - ""
                - - "arn:aws:iam::"
                  - !Ref "AWS::AccountId"
                  - ":root"
            Action: "kms:*"
            Resource: "*"
  MyDBSmall:
    Type: "AWS::RDS::DBInstance"
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