# AWS::RDS::DBInstance<a name="aws-resource-rds-dbinstance"></a>

The `AWS::RDS::DBInstance` resource creates an Amazon DB instance\. The new DB instance can be an RDS DB instance, or it can be a DB instance in an Aurora DB cluster\.

For more information about creating an RDS DB instance, see [Creating an Amazon RDS DB instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_CreateDBInstance.html) in the *Amazon RDS User Guide*\.

For more information about creating a DB instance in an Aurora DB cluster, see [ Creating an Amazon Aurora DB cluster](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.CreateInstance.html) in the *Amazon Aurora User Guide*\.

If you import an existing DB instance, and the template configuration doesn't match the actual configuration of the DB instance, AWS CloudFormation applies the changes in the template during the import operation\.

**Important**  
If a DB instance is deleted or replaced during an update, AWS CloudFormation deletes all automated snapshots\. However, it retains manual DB snapshots\. During an update that requires replacement, you can apply a stack policy to prevent DB instances from being replaced\. For more information, see [Prevent Updates to Stack Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/protect-stack-resources.html)\.

**Updating DB instances**

When properties labeled "*Update requires:* [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)" are updated, AWS CloudFormation first creates a replacement DB instance, then changes references from other dependent resources to point to the replacement DB instance, and finally deletes the old DB instance\.

**Important**  
We highly recommend that you take a snapshot of the database before updating the stack\. If you don't, you lose the data when AWS CloudFormation replaces your DB instance\. To preserve your data, perform the following procedure:  
Deactivate any applications that are using the DB instance so that there's no activity on the DB instance\.
Create a snapshot of the DB instance\. For more information, see [Creating a DB Snapshot](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_CreateSnapshot.html)\.
If you want to restore your instance using a DB snapshot, modify the updated template with your DB instance changes and add the `DBSnapshotIdentifier` property with the ID of the DB snapshot that you want to use\.  
After you restore a DB instance with a `DBSnapshotIdentifier` property, you must specify the same `DBSnapshotIdentifier` property for any future updates to the DB instance\. When you specify this property for an update, the DB instance is not restored from the DB snapshot again, and the data in the database is not changed\. However, if you don't specify the `DBSnapshotIdentifier` property, an empty DB instance is created, and the original DB instance is deleted\. If you specify a property that is different from the previous snapshot restore property, a new DB instance is restored from the specified `DBSnapshotIdentifier` property, and the original DB instance is deleted\.
Update the stack\.

For more information about updating other properties of this resource, see ` [ModifyDBInstance](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html)`\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.

**Deleting DB instances**

For DB instances that are part of an Aurora DB cluster, you can set a deletion policy for your DB instance to control how AWS CloudFormation handles the DB instance when the stack is deleted\. For Amazon RDS DB instances, you can choose to *retain* the DB instance, to *delete* the DB instance, or to *create a snapshot* of the DB instance\. The default AWS CloudFormation behavior depends on the `DBClusterIdentifier` property:

1. For `AWS::RDS::DBInstance` resources that don't specify the `DBClusterIdentifier` property, AWS CloudFormation saves a snapshot of the DB instance\.

1.  For `AWS::RDS::DBInstance` resources that do specify the `DBClusterIdentifier` property, AWS CloudFormation deletes the DB instance\.

 For more information, see [DeletionPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.

## Syntax<a name="aws-resource-rds-dbinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbinstance-syntax.json"></a>

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
      "[CertificateDetails](#cfn-rds-dbinstance-certificatedetails)" : CertificateDetails,
      "[CertificateRotationRestart](#cfn-rds-dbinstance-certificaterotationrestart)" : Boolean,
      "[CharacterSetName](#cfn-rds-dbinstance-charactersetname)" : String,
      "[CopyTagsToSnapshot](#cfn-rds-dbinstance-copytagstosnapshot)" : Boolean,
      "[CustomIAMInstanceProfile](#cfn-rds-dbinstance-customiaminstanceprofile)" : String,
      "[DBClusterIdentifier](#cfn-rds-dbinstance-dbclusteridentifier)" : String,
      "[DBClusterSnapshotIdentifier](#cfn-rds-dbinstance-dbclustersnapshotidentifier)" : String,
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
      "[Endpoint](#cfn-rds-dbinstance-endpoint)" : Endpoint,
      "[Engine](#cfn-rds-dbinstance-engine)" : String,
      "[EngineVersion](#cfn-rds-dbinstance-engineversion)" : String,
      "[Iops](#cfn-rds-dbinstance-iops)" : Integer,
      "[KmsKeyId](#cfn-rds-dbinstance-kmskeyid)" : String,
      "[LicenseModel](#cfn-rds-dbinstance-licensemodel)" : String,
      "[ManageMasterUserPassword](#cfn-rds-dbinstance-managemasteruserpassword)" : Boolean,
      "[MasterUsername](#cfn-rds-dbinstance-masterusername)" : String,
      "[MasterUserPassword](#cfn-rds-dbinstance-masteruserpassword)" : String,
      "[MasterUserSecret](#cfn-rds-dbinstance-masterusersecret)" : MasterUserSecret,
      "[MaxAllocatedStorage](#cfn-rds-dbinstance-maxallocatedstorage)" : Integer,
      "[MonitoringInterval](#cfn-rds-dbinstance-monitoringinterval)" : Integer,
      "[MonitoringRoleArn](#cfn-rds-dbinstance-monitoringrolearn)" : String,
      "[MultiAZ](#cfn-rds-dbinstance-multiaz)" : Boolean,
      "[NcharCharacterSetName](#cfn-rds-dbinstance-ncharcharactersetname)" : String,
      "[NetworkType](#cfn-rds-dbinstance-networktype)" : String,
      "[OptionGroupName](#cfn-rds-dbinstance-optiongroupname)" : String,
      "[PerformanceInsightsKMSKeyId](#cfn-rds-dbinstance-performanceinsightskmskeyid)" : String,
      "[PerformanceInsightsRetentionPeriod](#cfn-rds-dbinstance-performanceinsightsretentionperiod)" : Integer,
      "[Port](#cfn-rds-dbinstance-port)" : String,
      "[PreferredBackupWindow](#cfn-rds-dbinstance-preferredbackupwindow)" : String,
      "[PreferredMaintenanceWindow](#cfn-rds-dbinstance-preferredmaintenancewindow)" : String,
      "[ProcessorFeatures](#cfn-rds-dbinstance-processorfeatures)" : [ ProcessorFeature, ... ],
      "[PromotionTier](#cfn-rds-dbinstance-promotiontier)" : Integer,
      "[PubliclyAccessible](#cfn-rds-dbinstance-publiclyaccessible)" : Boolean,
      "[ReplicaMode](#cfn-rds-dbinstance-replicamode)" : String,
      "[RestoreTime](#cfn-rds-dbinstance-restoretime)" : String,
      "[SourceDBInstanceAutomatedBackupsArn](#cfn-rds-dbinstance-sourcedbinstanceautomatedbackupsarn)" : String,
      "[SourceDBInstanceIdentifier](#cfn-rds-dbinstance-sourcedbinstanceidentifier)" : String,
      "[SourceDbiResourceId](#cfn-rds-dbinstance-sourcedbiresourceid)" : String,
      "[SourceRegion](#cfn-rds-dbinstance-sourceregion)" : String,
      "[StorageEncrypted](#cfn-rds-dbinstance-storageencrypted)" : Boolean,
      "[StorageThroughput](#cfn-rds-dbinstance-storagethroughput)" : Integer,
      "[StorageType](#cfn-rds-dbinstance-storagetype)" : String,
      "[Tags](#cfn-rds-dbinstance-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Timezone](#cfn-rds-dbinstance-timezone)" : String,
      "[UseDefaultProcessorFeatures](#cfn-rds-dbinstance-usedefaultprocessorfeatures)" : Boolean,
      "[UseLatestRestorableTime](#cfn-rds-dbinstance-uselatestrestorabletime)" : Boolean,
      "[VPCSecurityGroups](#cfn-rds-dbinstance-vpcsecuritygroups)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-rds-dbinstance-syntax.yaml"></a>

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
  [CertificateDetails](#cfn-rds-dbinstance-certificatedetails): 
    CertificateDetails
  [CertificateRotationRestart](#cfn-rds-dbinstance-certificaterotationrestart): Boolean
  [CharacterSetName](#cfn-rds-dbinstance-charactersetname): String
  [CopyTagsToSnapshot](#cfn-rds-dbinstance-copytagstosnapshot): Boolean
  [CustomIAMInstanceProfile](#cfn-rds-dbinstance-customiaminstanceprofile): String
  [DBClusterIdentifier](#cfn-rds-dbinstance-dbclusteridentifier): String
  [DBClusterSnapshotIdentifier](#cfn-rds-dbinstance-dbclustersnapshotidentifier): String
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
  [Endpoint](#cfn-rds-dbinstance-endpoint): 
    Endpoint
  [Engine](#cfn-rds-dbinstance-engine): String
  [EngineVersion](#cfn-rds-dbinstance-engineversion): String
  [Iops](#cfn-rds-dbinstance-iops): Integer
  [KmsKeyId](#cfn-rds-dbinstance-kmskeyid): String
  [LicenseModel](#cfn-rds-dbinstance-licensemodel): String
  [ManageMasterUserPassword](#cfn-rds-dbinstance-managemasteruserpassword): Boolean
  [MasterUsername](#cfn-rds-dbinstance-masterusername): String
  [MasterUserPassword](#cfn-rds-dbinstance-masteruserpassword): String
  [MasterUserSecret](#cfn-rds-dbinstance-masterusersecret): 
    MasterUserSecret
  [MaxAllocatedStorage](#cfn-rds-dbinstance-maxallocatedstorage): Integer
  [MonitoringInterval](#cfn-rds-dbinstance-monitoringinterval): Integer
  [MonitoringRoleArn](#cfn-rds-dbinstance-monitoringrolearn): String
  [MultiAZ](#cfn-rds-dbinstance-multiaz): Boolean
  [NcharCharacterSetName](#cfn-rds-dbinstance-ncharcharactersetname): String
  [NetworkType](#cfn-rds-dbinstance-networktype): String
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
  [ReplicaMode](#cfn-rds-dbinstance-replicamode): String
  [RestoreTime](#cfn-rds-dbinstance-restoretime): String
  [SourceDBInstanceAutomatedBackupsArn](#cfn-rds-dbinstance-sourcedbinstanceautomatedbackupsarn): String
  [SourceDBInstanceIdentifier](#cfn-rds-dbinstance-sourcedbinstanceidentifier): String
  [SourceDbiResourceId](#cfn-rds-dbinstance-sourcedbiresourceid): String
  [SourceRegion](#cfn-rds-dbinstance-sourceregion): String
  [StorageEncrypted](#cfn-rds-dbinstance-storageencrypted): Boolean
  [StorageThroughput](#cfn-rds-dbinstance-storagethroughput): Integer
  [StorageType](#cfn-rds-dbinstance-storagetype): String
  [Tags](#cfn-rds-dbinstance-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Timezone](#cfn-rds-dbinstance-timezone): String
  [UseDefaultProcessorFeatures](#cfn-rds-dbinstance-usedefaultprocessorfeatures): Boolean
  [UseLatestRestorableTime](#cfn-rds-dbinstance-uselatestrestorabletime): Boolean
  [VPCSecurityGroups](#cfn-rds-dbinstance-vpcsecuritygroups): 
    - String
```

## Properties<a name="aws-resource-rds-dbinstance-properties"></a>

`AllocatedStorage`  <a name="cfn-rds-dbinstance-allocatedstorage"></a>
The amount of storage in gibibytes \(GiB\) to be initially allocated for the database instance\.  
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
  + Enterprise and Standard editions: Must be an integer from 20 to 16384\.
  + Web and Express editions: Must be an integer from 20 to 16384\.
+ Provisioned IOPS storage \(io1\):
  + Enterprise and Standard editions: Must be an integer from 20 to 16384\.
  + Web and Express editions: Must be an integer from 20 to 16384\.
+ Magnetic storage \(standard\):
  + Enterprise and Standard editions: Must be an integer from 20 to 1024\.
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
 **Amazon Aurora**   
Not applicable\. The associated roles are managed by the DB cluster\.  
*Required*: No  
*Type*: List of [DBInstanceRole](aws-properties-rds-dbinstance-dbinstancerole.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoMinorVersionUpgrade`  <a name="cfn-rds-dbinstance-autominorversionupgrade"></a>
A value that indicates whether minor engine upgrades are applied automatically to the DB instance during the maintenance window\. By default, minor engine upgrades are applied automatically\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`AvailabilityZone`  <a name="cfn-rds-dbinstance-availabilityzone"></a>
The Availability Zone \(AZ\) where the database will be created\. For information on AWS Regions and Availability Zones, see [Regions and Availability Zones](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html)\.  
 **Amazon Aurora**   
Each Aurora DB cluster hosts copies of its storage in three separate Availability Zones\. Specify one of these Availability Zones\. Aurora automatically chooses an appropriate Availability Zone if you don't specify one\.  
Default: A random, system\-chosen Availability Zone in the endpoint's AWS Region\.  
Example: `us-east-1d`   
Constraint: The `AvailabilityZone` parameter can't be specified if the DB instance is a Multi\-AZ deployment\. The specified Availability Zone must be in the same AWS Region as the current endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`BackupRetentionPeriod`  <a name="cfn-rds-dbinstance-backupretentionperiod"></a>
The number of days for which automated backups are retained\. Setting this parameter to a positive number enables backups\. Setting this parameter to 0 disables automated backups\.  
**Amazon Aurora**  
Not applicable\. The retention period for automated backups is managed by the DB cluster\.  
Default: 1  
Constraints:  
+ Must be a value from 0 to 35
+ Can't be set to 0 if the DB instance is a source to read replicas
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

`CertificateDetails`  <a name="cfn-rds-dbinstance-certificatedetails"></a>
The details of the DB instance's server certificate\.  
*Required*: No  
*Type*: [CertificateDetails](aws-properties-rds-dbinstance-certificatedetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CertificateRotationRestart`  <a name="cfn-rds-dbinstance-certificaterotationrestart"></a>
A value that indicates whether the DB instance is restarted when you rotate your SSL/TLS certificate\.  
By default, the DB instance is restarted when you rotate your SSL/TLS certificate\. The certificate is not updated until the DB instance is restarted\.  
Set this parameter only if you are *not* using SSL/TLS to connect to the DB instance\.
If you are using SSL/TLS to connect to the DB instance, follow the appropriate instructions for your DB engine to rotate your SSL/TLS certificate:  
+ For more information about rotating your SSL/TLS certificate for RDS DB engines, see [ Rotating Your SSL/TLS Certificate\.](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.SSL-certificate-rotation.html) in the *Amazon RDS User Guide\.* 
+ For more information about rotating your SSL/TLS certificate for Aurora DB engines, see [ Rotating Your SSL/TLS Certificate](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/UsingWithRDS.SSL-certificate-rotation.html) in the *Amazon Aurora User Guide*\.
This setting doesn't apply to RDS Custom\.  
*Required*: No  
*Type*: Boolean  
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

`CustomIAMInstanceProfile`  <a name="cfn-rds-dbinstance-customiaminstanceprofile"></a>
The instance profile associated with the underlying Amazon EC2 instance of an RDS Custom DB instance\. The instance profile must meet the following requirements:  
+ The profile must exist in your account\.
+ The profile must have an IAM role that Amazon EC2 has permissions to assume\.
+ The instance profile name and the associated IAM role name must start with the prefix `AWSRDSCustom`\.
For the list of permissions required for the IAM role, see [ Configure IAM and your VPC](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/custom-setup-orcl.html#custom-setup-orcl.iam-vpc) in the *Amazon RDS User Guide*\.  
This setting is required for RDS Custom\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBClusterIdentifier`  <a name="cfn-rds-dbinstance-dbclusteridentifier"></a>
The identifier of the DB cluster that the instance will belong to\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBClusterSnapshotIdentifier`  <a name="cfn-rds-dbinstance-dbclustersnapshotidentifier"></a>
The identifier for the RDS for MySQL Multi\-AZ DB cluster snapshot to restore from\.  
For more information on Multi\-AZ DB clusters, see [ Multi\-AZ DB cluster deployments](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/multi-az-db-clusters-concepts.html) in the *Amazon RDS User Guide*\.  
Constraints:  
+ Must match the identifier of an existing Multi\-AZ DB cluster snapshot\.
+ Can't be specified when `DBSnapshotIdentifier` is specified\.
+ Must be specified when `DBSnapshotIdentifier` isn't specified\.
+ If you are restoring from a shared manual Multi\-AZ DB cluster snapshot, the `DBClusterSnapshotIdentifier` must be the ARN of the shared snapshot\.
+ Can't be the identifier of an Aurora DB cluster snapshot\.
+ Can't be the identifier of an RDS for PostgreSQL Multi\-AZ DB cluster snapshot\.
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`DBInstanceClass`  <a name="cfn-rds-dbinstance-dbinstanceclass"></a>
The compute and memory capacity of the DB instance, for example, `db.m4.large`\. Not all DB instance classes are available in all AWS Regions, or for all database engines\.  
For the full list of DB instance classes, and availability for your engine, see [DB Instance Class](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.DBInstanceClass.html) in the *Amazon RDS User Guide\.* For more information about DB instance class pricing and AWS Region support for DB instance classes, see [Amazon RDS Pricing](http://aws.amazon.com/rds/pricing/)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`DBInstanceIdentifier`  <a name="cfn-rds-dbinstance-dbinstanceidentifier"></a>
A name for the DB instance\. If you specify a name, AWS CloudFormation converts it to lowercase\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the DB instance\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
For information about constraints that apply to DB instance identifiers, see [Naming constraints in Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Limits.html#RDS_Limits.Constraints) in the *Amazon RDS User Guide*\.  
If you specify a name, you can't perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\. 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBName`  <a name="cfn-rds-dbinstance-dbname"></a>
The meaning of this parameter differs according to the database engine you use\.  
If you specify the `[ DBSnapshotIdentifier](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsnapshotidentifier)` property, this property only applies to RDS for Oracle\.
 **Amazon Aurora**   
Not applicable\. The database name is managed by the DB cluster\.  
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
The name of the database to create when the DB instance is created\. If this parameter is not specified, the default `postgres` database is created in the DB instance\.  
Constraints:  
+ Must begin with a letter\. Subsequent characters can be letters, underscores, or digits \(0\-9\)\.
+ Must contain 1 to 63 characters\.
+ Can't be a word reserved by the specified database engine
 **Oracle**   
The Oracle System ID \(SID\) of the created DB instance\. If you specify `null`, the default value `ORCL` is used\. You can't specify the string NULL, or any other reserved word, for `DBName`\.   
Default: `ORCL`   
Constraints:  
+ Can't be longer than 8 characters
 **SQL Server**   
Not applicable\. Must be null\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBParameterGroupName`  <a name="cfn-rds-dbinstance-dbparametergroupname"></a>
The name of an existing DB parameter group or a reference to an [AWS::RDS::DBParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-dbparametergroup.html) resource created in the template\.  
To list all of the available DB parameter group names, use the following command:  
`aws rds describe-db-parameter-groups --query "DBParameterGroups[].DBParameterGroupName" --output text`  
If any of the data members of the referenced parameter group are changed during an update, the DB instance might need to be restarted, which causes some interruption\. If the parameter group contains static parameters, whether they were changed or not, an update triggers a reboot\.
If you don't specify a value for `DBParameterGroupName` property, the default DB parameter group for the specified engine and engine version is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`DBSecurityGroups`  <a name="cfn-rds-dbinstance-dbsecuritygroups"></a>
A list of the DB security groups to assign to the DB instance\. The list can include both the name of existing DB security groups or references to AWS::RDS::DBSecurityGroup resources created in the template\.  
 If you set DBSecurityGroups, you must not set VPCSecurityGroups, and vice versa\. Also, note that the DBSecurityGroups property exists only for backwards compatibility with older regions and is no longer recommended for providing security information to an RDS DB instance\. Instead, use VPCSecurityGroups\.  
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
+ `CharacterSetName`
+ `DBClusterIdentifier`
+ `DBName`
+ `DeleteAutomatedBackups`
+ `EnablePerformanceInsights`
+ `KmsKeyId`
+ `MasterUsername`
+ `MasterUserPassword`
+ `PerformanceInsightsKMSKeyId`
+ `PerformanceInsightsRetentionPeriod`
+ `PromotionTier`
+ `SourceDBInstanceIdentifier`
+ `SourceRegion`
+ `StorageEncrypted` \(for an encrypted snapshot\)
+ `Timezone`
 **Amazon Aurora**   
Not applicable\. Snapshot restore is managed by the DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`DBSubnetGroupName`  <a name="cfn-rds-dbinstance-dbsubnetgroupname"></a>
A DB subnet group to associate with the DB instance\. If you update this value, the new subnet group must be a subnet group in a new VPC\.   
If there's no DB subnet group, then the DB instance isn't a VPC DB instance\.  
For more information about using Amazon RDS in a VPC, see [Using Amazon RDS with Amazon Virtual Private Cloud \(VPC\)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.html) in the *Amazon RDS User Guide*\.   
**Amazon Aurora**  
Not applicable\. The DB subnet group is managed by the DB cluster\. If specified, the setting must match the DB cluster setting\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeleteAutomatedBackups`  <a name="cfn-rds-dbinstance-deleteautomatedbackups"></a>
A value that indicates whether to remove automated backups immediately after the DB instance is deleted\. This parameter isn't case\-sensitive\. The default is to remove automated backups immediately after the DB instance is deleted\.  
**Amazon Aurora**  
Not applicable\. When you delete a DB cluster, all automated backups for that DB cluster are deleted and can't be recovered\. Manual DB cluster snapshots of the DB cluster are not deleted\.  
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
The Active Directory directory ID to create the DB instance in\. Currently, only Microsoft SQL Server, Oracle, and PostgreSQL DB instances can be created in an Active Directory Domain\.  
For more information, see [ Kerberos Authentication](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/kerberos-authentication.html) in the *Amazon RDS User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainIAMRoleName`  <a name="cfn-rds-dbinstance-domainiamrolename"></a>
Specify the name of the IAM role to be used when making API calls to the Directory Service\.  
This setting doesn't apply to RDS Custom\.  
 **Amazon Aurora**   
Not applicable\. The domain is managed by the DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableCloudwatchLogsExports`  <a name="cfn-rds-dbinstance-enablecloudwatchlogsexports"></a>
The list of log types that need to be enabled for exporting to CloudWatch Logs\. The values in the list depend on the DB engine being used\. For more information, see [Publishing Database Logs to Amazon CloudWatch Logs ](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_LogAccess.html#USER_LogAccess.Procedural.UploadtoCloudWatch) in the *Amazon Relational Database Service User Guide*\.  
 **Amazon Aurora**   
Not applicable\. CloudWatch Logs exports are managed by the DB cluster\.   
 **MariaDB**   
Valid values: `audit`, `error`, `general`, `slowquery`   
 **Microsoft SQL Server**   
Valid values: `agent`, `error`   
 **MySQL**   
Valid values: `audit`, `error`, `general`, `slowquery`   
 **Oracle**   
Valid values: `alert`, `audit`, `listener`, `trace`   
 **PostgreSQL**   
Valid values: `postgresql`, `upgrade`   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableIAMDatabaseAuthentication`  <a name="cfn-rds-dbinstance-enableiamdatabaseauthentication"></a>
A value that indicates whether to enable mapping of AWS Identity and Access Management \(IAM\) accounts to database accounts\. By default, mapping is disabled\.  
This property is supported for RDS for MariaDB, RDS for MySQL, and RDS for PostgreSQL\. For more information, see [ IAM Database Authentication for MariaDB, MySQL, and PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.IAMDBAuth.html) in the *Amazon RDS User Guide\.*   
 **Amazon Aurora**   
Not applicable\. Mapping AWS IAM accounts to database accounts is managed by the DB cluster\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnablePerformanceInsights`  <a name="cfn-rds-dbinstance-enableperformanceinsights"></a>
A value that indicates whether to enable Performance Insights for the DB instance\. For more information, see [Using Amazon Performance Insights](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PerfInsights.html) in the *Amazon RDS User Guide*\.  
This setting doesn't apply to RDS Custom\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Endpoint`  <a name="cfn-rds-dbinstance-endpoint"></a>
Specifies the connection endpoint\.  
The endpoint might not be shown for instances whose status is `creating`\.
*Required*: No  
*Type*: [Endpoint](aws-properties-rds-dbinstance-endpoint.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engine`  <a name="cfn-rds-dbinstance-engine"></a>
The name of the database engine that you want to use for this DB instance\.  
When you are creating a DB instance, the `Engine` property is required\.
Valid Values:  
+ `aurora` \(for MySQL 5\.6\-compatible Aurora\)
+ `aurora-mysql` \(for MySQL 5\.7\-compatible Aurora\)
+ `aurora-postgresql`
+ `custom-oracle-ee`
+ `custom-oracle-ee-cdb`
+ `custom-sqlserver-ee`
+ `custom-sqlserver-se`
+ `custom-sqlserver-web`
+ `mariadb`
+ `mysql`
+ `oracle-ee`
+ `oracle-ee-cdb`
+ `oracle-se2`
+ `oracle-se2-cdb`
+ `postgres`
+ `sqlserver-ee`
+ `sqlserver-se`
+ `sqlserver-ex`
+ `sqlserver-web`
*Required*: Conditional  
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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-rds-dbinstance-iops"></a>
The number of I/O operations per second \(IOPS\) that the database provisions\. The value must be equal to or greater than 1000\.   
If you specify this property, you must follow the range of allowed ratios of your requested IOPS rate to the amount of storage that you allocate \(IOPS to allocated storage\)\. For example, you can provision an Oracle database instance with 1000 IOPS and 200 GiB of storage \(a ratio of 5:1\), or specify 2000 IOPS with 200 GiB of storage \(a ratio of 10:1\)\. For more information, see [Amazon RDS Provisioned IOPS Storage to Improve Performance](https://docs.aws.amazon.com/AmazonRDS/latest/DeveloperGuide/CHAP_Storage.html#USER_PIOPS) in the *Amazon RDS User Guide*\.  
If you specify `io1` for the `StorageType` property, then you must also specify the `Iops` property\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-rds-dbinstance-kmskeyid"></a>
The ARN of the AWS KMS key that's used to encrypt the DB instance, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the StorageEncrypted property but don't specify this property, AWS CloudFormation uses the default KMS key\. If you specify this property, you must set the StorageEncrypted property to true\.   
If you specify the `SourceDBInstanceIdentifier` property, the value is inherited from the source DB instance if the read replica is created in the same region\.  
If you create an encrypted read replica in a different AWS Region, then you must specify a KMS key for the destination AWS Region\. KMS encryption keys are specific to the region that they're created in, and you can't use encryption keys from one region in another region\.  
If you specify the `SnapshotIdentifier` property, the `StorageEncrypted` property value is inherited from the snapshot, and if the DB instance is encrypted, the specified `KmsKeyId` property is used\.  
If you specify `DBSecurityGroups`, AWS CloudFormation ignores this property\. To specify both a security group and this property, you must use a VPC security group\. For more information about Amazon RDS and VPC, see [Using Amazon RDS with Amazon VPC](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.html) in the *Amazon RDS User Guide*\.  
 **Amazon Aurora**   
Not applicable\. The KMS key identifier is managed by the DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LicenseModel`  <a name="cfn-rds-dbinstance-licensemodel"></a>
License model information for this DB instance\.  
 Valid values:  
+ Aurora MySQL \- `general-public-license`
+ Aurora PostgreSQL \- `postgresql-license`
+ MariaDB \- `general-public-license`
+ Microsoft SQL Server \- `license-included`
+ MySQL \- `general-public-license`
+ Oracle \- `bring-your-own-license` or `license-included`
+ PostgreSQL \- `postgresql-license`
If you've specified `DBSecurityGroups` and then you update the license model, AWS CloudFormation replaces the underlying DB instance\. This will incur some interruptions to database availability\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManageMasterUserPassword`  <a name="cfn-rds-dbinstance-managemasteruserpassword"></a>
A value that indicates whether to manage the master user password with AWS Secrets Manager\.  
For more information, see [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-secrets-manager.html) in the *Amazon RDS User Guide\.*   
Constraints:  
+ Can't manage the master user password with AWS Secrets Manager if `MasterUserPassword` is specified\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUsername`  <a name="cfn-rds-dbinstance-masterusername"></a>
The master user name for the DB instance\.  
If you specify the `SourceDBInstanceIdentifier` or `DBSnapshotIdentifier` property, don't specify this property\. The value is inherited from the source DB instance or snapshot\.
 **Amazon Aurora**   
Not applicable\. The name for the master user is managed by the DB cluster\.   
 **MariaDB**   
Constraints:  
+ Required for MariaDB\.
+ Must be 1 to 16 letters or numbers\.
+ Can't be a reserved word for the chosen database engine\.
 **Microsoft SQL Server**   
Constraints:  
+ Required for SQL Server\.
+ Must be 1 to 128 letters or numbers\.
+ The first character must be a letter\.
+ Can't be a reserved word for the chosen database engine\.
 **MySQL**   
Constraints:  
+ Required for MySQL\.
+ Must be 1 to 16 letters or numbers\.
+ First character must be a letter\.
+ Can't be a reserved word for the chosen database engine\.
 **Oracle**   
Constraints:  
+ Required for Oracle\.
+ Must be 1 to 30 letters or numbers\.
+ First character must be a letter\.
+ Can't be a reserved word for the chosen database engine\.
 **PostgreSQL**   
Constraints:  
+ Required for PostgreSQL\.
+ Must be 1 to 63 letters or numbers\.
+ First character must be a letter\.
+ Can't be a reserved word for the chosen database engine\.
*Required*: Conditional  
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
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUserSecret`  <a name="cfn-rds-dbinstance-masterusersecret"></a>
Contains the secret managed by RDS in AWS Secrets Manager for the master user password\.  
For more information, see [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-secrets-manager.html) in the *Amazon RDS User Guide\.*   
*Required*: No  
*Type*: [MasterUserSecret](aws-properties-rds-dbinstance-masterusersecret.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxAllocatedStorage`  <a name="cfn-rds-dbinstance-maxallocatedstorage"></a>
The upper limit in gibibytes \(GiB\) to which Amazon RDS can automatically scale the storage of the DB instance\.  
For more information about this setting, including limitations that apply to it, see [ Managing capacity automatically with Amazon RDS storage autoscaling](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PIOPS.StorageTypes.html#USER_PIOPS.Autoscaling) in the *Amazon RDS User Guide*\.  
This setting doesn't apply to RDS Custom\.  
 **Amazon Aurora**   
Not applicable\. Storage is managed by the DB cluster\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringInterval`  <a name="cfn-rds-dbinstance-monitoringinterval"></a>
The interval, in seconds, between points when Enhanced Monitoring metrics are collected for the DB instance\. To disable collection of Enhanced Monitoring metrics, specify 0\. The default is 0\.  
If `MonitoringRoleArn` is specified, then you must set `MonitoringInterval` to a value other than 0\.  
This setting doesn't apply to RDS Custom\.  
Valid Values: `0, 1, 5, 10, 15, 30, 60`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringRoleArn`  <a name="cfn-rds-dbinstance-monitoringrolearn"></a>
The ARN for the IAM role that permits RDS to send enhanced monitoring metrics to Amazon CloudWatch Logs\. For example, `arn:aws:iam:123456789012:role/emaccess`\. For information on creating a monitoring role, see [Setting Up and Enabling Enhanced Monitoring](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Monitoring.OS.html#USER_Monitoring.OS.Enabling) in the *Amazon RDS User Guide*\.  
If `MonitoringInterval` is set to a value other than 0, then you must supply a `MonitoringRoleArn` value\.  
This setting doesn't apply to RDS Custom\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiAZ`  <a name="cfn-rds-dbinstance-multiaz"></a>
Specifies whether the database instance is a Multi\-AZ DB instance deployment\. You can't set the `AvailabilityZone` parameter if the `MultiAZ` parameter is set to true\.   
For more information, see [ Multi\-AZ deployments for high availability](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html) in the *Amazon RDS User Guide*\.  
 **Amazon Aurora**   
Not applicable\. Amazon Aurora storage is replicated across all of the Availability Zones and doesn't require the `MultiAZ` option to be set\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`NcharCharacterSetName`  <a name="cfn-rds-dbinstance-ncharcharactersetname"></a>
The name of the NCHAR character set for the Oracle DB instance\.  
This parameter doesn't apply to RDS Custom\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkType`  <a name="cfn-rds-dbinstance-networktype"></a>
The network type of the DB instance\.  
Valid values:  
+  `IPV4` 
+  `DUAL` 
The network type is determined by the `DBSubnetGroup` specified for the DB instance\. A `DBSubnetGroup` can support only the IPv4 protocol or the IPv4 and IPv6 protocols \(`DUAL`\)\.  
For more information, see [ Working with a DB instance in a VPC](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.WorkingWithRDSInstanceinaVPC.html) in the *Amazon RDS User Guide\.*   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptionGroupName`  <a name="cfn-rds-dbinstance-optiongroupname"></a>
Indicates that the DB instance should be associated with the specified option group\.  
Permanent options, such as the TDE option for Oracle Advanced Security TDE, can't be removed from an option group\. Also, that option group can't be removed from a DB instance once it is associated with a DB instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerformanceInsightsKMSKeyId`  <a name="cfn-rds-dbinstance-performanceinsightskmskeyid"></a>
The AWS KMS key identifier for encryption of Performance Insights data\.  
The KMS key identifier is the key ARN, key ID, alias ARN, or alias name for the KMS key\.  
If you do not specify a value for `PerformanceInsightsKMSKeyId`, then Amazon RDS uses your default KMS key\. There is a default KMS key for your AWS account\. Your AWS account has a different default KMS key for each AWS Region\.  
For information about enabling Performance Insights, see [ EnablePerformanceInsights](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-enableperformanceinsights)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`PerformanceInsightsRetentionPeriod`  <a name="cfn-rds-dbinstance-performanceinsightsretentionperiod"></a>
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
This setting doesn't apply to RDS Custom\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-rds-dbinstance-port"></a>
The port number on which the database accepts connections\.  
 **Amazon Aurora**   
Not applicable\. The port number is managed by the DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreferredBackupWindow`  <a name="cfn-rds-dbinstance-preferredbackupwindow"></a>
 The daily time range during which automated backups are created if automated backups are enabled, using the `BackupRetentionPeriod` parameter\. For more information, see [ Backup Window](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithAutomatedBackups.html#USER_WorkingWithAutomatedBackups.BackupWindow) in the *Amazon RDS User Guide\.*   
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
This setting doesn't apply to RDS Custom\.  
 **Amazon Aurora**   
Not applicable\.  
*Required*: No  
*Type*: List of [ProcessorFeature](aws-properties-rds-dbinstance-processorfeature.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PromotionTier`  <a name="cfn-rds-dbinstance-promotiontier"></a>
A value that specifies the order in which an Aurora Replica is promoted to the primary instance after a failure of the existing primary instance\. For more information, see [ Fault Tolerance for an Aurora DB Cluster](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Managing.Backups.html#Aurora.Managing.FaultTolerance) in the *Amazon Aurora User Guide*\.  
This setting doesn't apply to RDS Custom\.  
Default: 1  
Valid Values: 0 \- 15  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PubliclyAccessible`  <a name="cfn-rds-dbinstance-publiclyaccessible"></a>
Indicates whether the DB instance is an internet\-facing instance\. If you specify true, AWS CloudFormation creates an instance with a publicly resolvable DNS name, which resolves to a public IP address\. If you specify false, AWS CloudFormation creates an internal instance with a DNS name that resolves to a private IP address\.   
The default behavior value depends on your VPC setup and the database subnet group\. For more information, see the `PubliclyAccessible` parameter in the [CreateDBInstance](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicaMode`  <a name="cfn-rds-dbinstance-replicamode"></a>
The open mode of an Oracle read replica\. For more information, see [Working with Oracle Read Replicas for Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/oracle-read-replicas.html) in the *Amazon RDS User Guide*\.  
This setting is only supported in RDS for Oracle\.  
Default: `open-read-only`  
Valid Values: `open-read-only` or `mounted`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestoreTime`  <a name="cfn-rds-dbinstance-restoretime"></a>
The date and time to restore from\.  
Valid Values: Value must be a time in Universal Coordinated Time \(UTC\) format  
Constraints:  
+ Must be before the latest restorable time for the DB instance
+ Can't be specified if the `UseLatestRestorableTime` parameter is enabled
Example: `2009-09-07T23:45:00Z`   
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SourceDBInstanceAutomatedBackupsArn`  <a name="cfn-rds-dbinstance-sourcedbinstanceautomatedbackupsarn"></a>
The Amazon Resource Name \(ARN\) of the replicated automated backups from which to restore, for example, `arn:aws:rds:useast-1:123456789012:auto-backup:ab-L2IJCEXJP7XQ7HOJ4SIEXAMPLE`\.  
This setting doesn't apply to RDS Custom\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SourceDBInstanceIdentifier`  <a name="cfn-rds-dbinstance-sourcedbinstanceidentifier"></a>
If you want to create a read replica DB instance, specify the ID of the source DB instance\. Each DB instance can have a limited number of read replicas\. For more information, see [Working with Read Replicas](https://docs.aws.amazon.com/AmazonRDS/latest/DeveloperGuide/USER_ReadRepl.html) in the *Amazon RDS User Guide*\.  
For information about constraints that apply to DB instance identifiers, see [Naming constraints in Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Limits.html#RDS_Limits.Constraints) in the *Amazon RDS User Guide*\.  
The `SourceDBInstanceIdentifier` property determines whether a DB instance is a read replica\. If you remove the `SourceDBInstanceIdentifier` property from your template and then update your stack, AWS CloudFormation promotes the Read Replica to a standalone DB instance\.  
+ If you specify a source DB instance that uses VPC security groups, we recommend that you specify the `VPCSecurityGroups` property\. If you don't specify the property, the read replica inherits the value of the `VPCSecurityGroups` property from the source DB when you create the replica\. However, if you update the stack, AWS CloudFormation reverts the replica's `VPCSecurityGroups` property to the default value because it's not defined in the stack's template\. This change might cause unexpected issues\.
+ Read replicas don't support deletion policies\. AWS CloudFormation ignores any deletion policy that's associated with a read replica\.
+ If you specify `SourceDBInstanceIdentifier`, don't specify the `DBSnapshotIdentifier` property\. You can't create a read replica from a snapshot\.
+ Don't set the `BackupRetentionPeriod`, `DBName`, `MasterUsername`, `MasterUserPassword`, and `PreferredBackupWindow` properties\. The database attributes are inherited from the source DB instance, and backups are disabled for read replicas\.
+ If the source DB instance is in a different region than the read replica, specify the source region in `SourceRegion`, and specify an ARN for a valid DB instance in `SourceDBInstanceIdentifier`\. For more information, see [ Constructing a Amazon RDS Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Tagging.html#USER_Tagging.ARN) in the *Amazon RDS User Guide*\.
+ For DB instances in Amazon Aurora clusters, don't specify this property\. Amazon RDS automatically assigns writer and reader DB instances\.
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SourceDbiResourceId`  <a name="cfn-rds-dbinstance-sourcedbiresourceid"></a>
The resource ID of the source DB instance from which to restore\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SourceRegion`  <a name="cfn-rds-dbinstance-sourceregion"></a>
The ID of the region that contains the source DB instance for the read replica\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageEncrypted`  <a name="cfn-rds-dbinstance-storageencrypted"></a>
A value that indicates whether the DB instance is encrypted\. By default, it isn't encrypted\.  
If you specify the `KmsKeyId` property, then you must enable encryption\.  
If you specify the `SourceDBInstanceIdentifier` property, don't specify this property\. The value is inherited from the source DB instance, and if the DB instance is encrypted, the specified `KmsKeyId` property is used\.  
If you specify the `SnapshotIdentifier` and the specified snapshot is encrypted, don't specify this property\. The value is inherited from the snapshot, and the specified `KmsKeyId` property is used\.  
If you specify the `SnapshotIdentifier` and the specified snapshot isn't encrypted, you can use this property to specify that the restored DB instance is encrypted\. Specify the `KmsKeyId` property for the KMS key to use for encryption\. If you don't want the restored DB instance to be encrypted, then don't set this property or set it to `false`\.  
**Amazon Aurora**  
Not applicable\. The encryption for DB instances is managed by the DB cluster\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageThroughput`  <a name="cfn-rds-dbinstance-storagethroughput"></a>
Specifies the storage throughput value for the DB instance\. This setting applies only to the `gp3` storage type\.   
This setting doesn't apply to RDS Custom or Amazon Aurora\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageType`  <a name="cfn-rds-dbinstance-storagetype"></a>
Specifies the storage type to be associated with the DB instance\.  
 Valid values: ` gp2 | gp3 | io1 | standard`   
The `standard` value is also known as magnetic\.  
 If you specify `io1` or `gp3`, you must also include a value for the `Iops` parameter\.   
 Default: `io1` if the `Iops` parameter is specified, otherwise `gp2`   
For more information, see [Amazon RDS DB Instance Storage](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Storage.html) in the *Amazon RDS User Guide*\.  
 **Amazon Aurora**   
Not applicable\. Aurora data is stored in the cluster volume, which is a single, virtual volume that uses solid state drives \(SSDs\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Tags`  <a name="cfn-rds-dbinstance-tags"></a>
An optional array of key\-value pairs to apply to this DB instance\.  
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
This setting doesn't apply to RDS Custom\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseLatestRestorableTime`  <a name="cfn-rds-dbinstance-uselatestrestorabletime"></a>
A value that indicates whether the DB instance is restored from the latest backup time\. By default, the DB instance isn't restored from the latest backup time\.  
Constraints: Can't be specified if the `RestoreTime` parameter is provided\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`VPCSecurityGroups`  <a name="cfn-rds-dbinstance-vpcsecuritygroups"></a>
A list of the VPC security group IDs to assign to the DB instance\. The list can include both the physical IDs of existing VPC security groups and references to [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resources created in the template\.  
If you plan to update the resource, don't specify VPC security groups in a shared VPC\.  
 If you set `VPCSecurityGroups`, you must not set [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsecuritygroups](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsecuritygroups), and vice versa\.  
You can migrate a DB instance in your stack from an RDS DB security group to a VPC security group, but keep the following in mind:  
+ You can't revert to using an RDS security group after you establish a VPC security group membership\.
+ When you migrate your DB instance to VPC security groups, if your stack update rolls back because the DB instance update fails or because an update fails in another AWS CloudFormation resource, the rollback fails because it can't revert to an RDS security group\.
+ To use the properties that are available when you use a VPC security group, you must recreate the DB instance\. If you don't, AWS CloudFormation submits only the property values that are listed in the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsecuritygroups](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html#cfn-rds-dbinstance-dbsecuritygroups) property\.
To avoid this situation, migrate your DB instance to using VPC security groups only when that is the only change in your stack template\.   
 **Amazon Aurora**   
Not applicable\. The associated list of EC2 VPC security groups is managed by the DB cluster\. If specified, the setting must match the DB cluster setting\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rds-dbinstance-return-values"></a>

### Ref<a name="aws-resource-rds-dbinstance-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the DB instance name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-rds-dbinstance-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-rds-dbinstance-return-values-fn--getatt-fn--getatt"></a>

`CertificateDetails.CAIdentifier`  <a name="CertificateDetails.CAIdentifier-fn::getatt"></a>
The CA identifier of the CA certificate used for the DB instance's server certificate\.

`CertificateDetails.ValidTill`  <a name="CertificateDetails.ValidTill-fn::getatt"></a>
The expiration date of the DB instance’s server certificate\.

`DBInstanceArn`  <a name="DBInstanceArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the DB instance\.

`DbiResourceId`  <a name="DbiResourceId-fn::getatt"></a>
The AWS Region\-unique, immutable identifier for the DB instance\. This identifier is found in AWS CloudTrail log entries whenever the AWS KMS key for the DB instance is accessed\.

`DBSystemId`  <a name="DBSystemId-fn::getatt"></a>
The Oracle system ID \(Oracle SID\) for a container database \(CDB\)\. The Oracle SID is also the name of the CDB\.  
This setting is valid for RDS Custom only\.

`Endpoint.Address`  <a name="Endpoint.Address-fn::getatt"></a>
The connection endpoint for the database\. For example: `mystack-mydb-1apw1j4phylrk.cg034hpkmmjt.us-east-2.rds.amazonaws.com`  
For Aurora Serverless DB clusters, the connection endpoint only applies to the DB cluster\.

`Endpoint.HostedZoneId`  <a name="Endpoint.HostedZoneId-fn::getatt"></a>
The ID that Amazon Route 53 assigns when you create a hosted zone\.

`Endpoint.Port`  <a name="Endpoint.Port-fn::getatt"></a>
The port number on which the database accepts connections\. For example: `3306` 

`MasterUserSecret.SecretArn`  <a name="MasterUserSecret.SecretArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the secret\.

## Examples<a name="aws-resource-rds-dbinstance--examples"></a>

### Creating a DB instance with Enhanced Monitoring enabled<a name="aws-resource-rds-dbinstance--examples--Creating_a_DB_instance_with_Enhanced_Monitoring_enabled"></a>

The following example creates an Amazon RDS MySQL DB instance with Enhanced Monitoring enabled\. The IAM role for Enhanced Monitoring specified in `MonitoringRoleArn` must exist before you run this example\. For more information, see [ Enhanced Monitoring](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Monitoring.OS.html) in the *Amazon RDS User Guide*\.

#### JSON<a name="aws-resource-rds-dbinstance--examples--Creating_a_DB_instance_with_Enhanced_Monitoring_enabled--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS CloudFormation Sample Template for creating an Amazon RDS DB instance: Sample template showing how to create a DB instance with Enhanced Monitoring enabled. **WARNING** This template creates an RDS DB instance. You will be billed for the AWS resources used if you create a stack from this template.",
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
            "MinValue": "20",
            "MaxValue": "65536",
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
                "MonitoringInterval": 60,
                "MonitoringRoleArn": "arn:aws:iam::1233456789012:role/rds-monitoring-role"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbinstance--examples--Creating_a_DB_instance_with_Enhanced_Monitoring_enabled--yaml"></a>

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
    MinValue: '20'
    MaxValue: '65536'
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
      EngineVersion: "8.0.16"
      MasterUsername: !Ref DBUsername
      MasterUserPassword: !Ref DBPassword
      MonitoringInterval: 60
      MonitoringRoleArn: 'arn:aws:iam::123456789012:role/rds-monitoring-role'
```

### Creating a cross\-region encrypted read replica<a name="aws-resource-rds-dbinstance--examples--Creating_a_cross-region_encrypted_read_replica"></a>

The following example creates an encrypted read replica from a cross\-region source DB instance\. 

#### JSON<a name="aws-resource-rds-dbinstance--examples--Creating_a_cross-region_encrypted_read_replica--json"></a>

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

#### YAML<a name="aws-resource-rds-dbinstance--examples--Creating_a_cross-region_encrypted_read_replica--yaml"></a>

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

### Creating an Amazon RDS Custom DB instance<a name="aws-resource-rds-dbinstance--examples--Creating_an_Amazon_RDS_Custom_DB_instance"></a>

This example creates an Amazon RDS Custom DB instance\. Amazon RDS Custom allows you as a database administrator to access and customize your database environment and operating system\. With this access, you can configure settings, install patches, and enable native features to meet the dependent application's requirements\. With RDS Custom, you can run your database workload using the AWS Management Console or AWS CLI\. For more information, see [Working with Amazon RDS Custom](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-custom.html) in the *Amazon RDS User Guide*\.

#### JSON<a name="aws-resource-rds-dbinstance--examples--Creating_an_Amazon_RDS_Custom_DB_instance--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "AllocatedStorage": {
            "Type": "String"
        },
        "CustomIAMInstanceProfile": {
            "Type": "String"
        },
        "DBInstanceIdentifier": {
            "Type": "String"
        },
        "DBInstanceClass": {
            "Type": "String"
        },
        "DBName": {
            "Type": "String"
        },
        "DBSubnetGroupName": {
            "Type": "String"
        },
        "Engine": {
            "Type": "String"
        },
        "EngineVersion": {
            "Type": "String"
        },
        "KMSKeyId": {
            "Type": "String"
        },
        "LicenseModel": {
            "Type": "String"
        },
        "MasterUsername": {
            "Type": "String"
        },
        "MasterUserPassword": {
            "Type": "String",
            "NoEcho": true
        }
    },
    "Resources": {
        "RDSDBInstance": {
            "Properties": {
                "AllocatedStorage": {
                    "Ref": "AllocatedStorage"
                },
                "AutoMinorVersionUpgrade": false,
                "CustomIAMInstanceProfile": {
                    "Ref": "CustomIAMInstanceProfile"
                },
                "DBInstanceClass": {
                    "Ref": "DBInstanceClass"
                },
                "DBSubnetGroupName": {
                    "Ref": "DBSubnetGroupName"
                },
                "Engine": {
                    "Ref": "Engine"
                },
                "EngineVersion": {
                    "Ref": "EngineVersion"
                },
                "LicenseModel": {
                    "Ref": "LicenseModel"
                },
                "KmsKeyId": {
                    "Ref": "KMSKeyId"
                },
                "MasterUsername": {
                    "Ref": "MasterUsername"
                },
                "MasterUserPassword": {
                    "Ref": "MasterUserPassword"
                }
            },
            "Type": "AWS::RDS::DBInstance"
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbinstance--examples--Creating_an_Amazon_RDS_Custom_DB_instance--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  AllocatedStorage:
    Type: String
  CustomIAMInstanceProfile:
    Type: String
  DBInstanceIdentifier:
    Type: String
  DBInstanceClass:
    Type: String
  DBName:
    Type: String
  DBSubnetGroupName:
    Type: String
  Engine:
    Type: String
  EngineVersion:
    Type: String
  KMSKeyId:
    Type: String
  LicenseModel:
    Type: String
  MasterUsername:
    Type: String
  MasterUserPassword:
    Type: String
    NoEcho: true
Resources:
  RDSDBInstance:
    Properties:
      AllocatedStorage: !Ref AllocatedStorage
      AutoMinorVersionUpgrade: false
      CustomIAMInstanceProfile: !Ref CustomIAMInstanceProfile
      DBInstanceClass: !Ref DBInstanceClass
      DBSubnetGroupName: !Ref DBSubnetGroupName
      Engine: !Ref Engine
      EngineVersion: !Ref EngineVersion
      LicenseModel: !Ref LicenseModel
      KmsKeyId: !Ref KMSKeyId
      MasterUsername: !Ref MasterUsername
      MasterUserPassword: !Ref MasterUserPassword
    Type: 'AWS::RDS::DBInstance'
```

### Create a Secrets Manager secret for a master password<a name="aws-resource-rds-dbinstance--examples--Create_a_Secrets_Manager_secret_for_a_master_password"></a>

The following example creates a AWS CloudFormation stack with the AWS::RDS::DBInstance resource with managed master user password feature\. The secret which is used to authenticate the DB instance is shown in the `Secret` stack output\. This output can be removed if showing this value to other CloudFormation stack isn't required\.

For more information about managing password with Secrets Manager, see [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-secrets-manager.html) in the *Amazon RDS User Guide* and [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-secrets-manager.html) in the *Amazon Aurora User Guide*\.

#### JSON<a name="aws-resource-rds-dbinstance--examples--Create_a_Secrets_Manager_secret_for_a_master_password--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "A sample template",
    "Resources": {
        "MyInstance": {
            "Properties": {
                "MasterUsername": "masteruser",
                "DBInstanceClass": "db.t3.micro",
                "Engine": "mysql",
                "AllocatedStorage": 5,
                "AutoMinorVersionUpgrade": false,
                "ManageMasterUserPassword": true,
                "MasterUserSecret": {
                    "KmsKeyId": {
                        "Ref": "KMSKey"
                    }
                }
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
                "Fn::GetAtt": "MyInstance.MasterUserSecret.SecretArn"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbinstance--examples--Create_a_Secrets_Manager_secret_for_a_master_password--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: A sample template
Resources:
  MyInstance:
    Properties:
      MasterUsername: "masteruser"
      DBInstanceClass: "db.t3.micro"
      Engine: "mysql"
      AllocatedStorage: 5
      AutoMinorVersionUpgrade: false
      ManageMasterUserPassword: true
      MasterUserSecret:
        KmsKeyId: !Ref KMSKey
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
      Fn::GetAtt: MyInstance.MasterUserSecret.SecretArn
```