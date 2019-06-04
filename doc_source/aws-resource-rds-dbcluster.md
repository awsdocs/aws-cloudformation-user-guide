# AWS::RDS::DBCluster<a name="aws-resource-rds-dbcluster"></a>

The `AWS::RDS::DBCluster` resource creates an Amazon Aurora DB cluster\. For more information, see [Managing an Amazon Aurora DB Cluster](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_Aurora.html) in the *Amazon Aurora User Guide*\.

**Note**  
You can only create this resource in regions where Amazon Aurora is supported\.

The default `DeletionPolicy` for `AWS::RDS::DBCluster` resources is `Snapshot`\. For more information about how AWS CloudFormation deletes resources, see [ DeletionPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.

## Syntax<a name="aws-resource-rds-dbcluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbcluster-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBCluster",
  "Properties" : {
      "[AvailabilityZones](#cfn-rds-dbcluster-availabilityzones)" : [ String, ... ],
      "[BacktrackWindow](#cfn-rds-dbcluster-backtrackwindow)" : Long,
      "[BackupRetentionPeriod](#cfn-rds-dbcluster-backuprententionperiod)" : Integer,
      "[DBClusterIdentifier](#cfn-rds-dbcluster-dbclusteridentifier)" : String,
      "[DBClusterParameterGroupName](#cfn-rds-dbcluster-dbclusterparametergroupname)" : String,
      "[DBSubnetGroupName](#cfn-rds-dbcluster-dbsubnetgroupname)" : String,
      "[DatabaseName](#cfn-rds-dbcluster-databasename)" : String,
      "[DeletionProtection](#cfn-rds-dbcluster-deletionprotection)" : Boolean,
      "[EnableCloudwatchLogsExports](#cfn-rds-dbcluster-enablecloudwatchlogsexports)" : [ String, ... ],
      "[EnableIAMDatabaseAuthentication](#cfn-rds-dbcluster-enableiamdatabaseauthentication)" : Boolean,
      "[Engine](#cfn-rds-dbcluster-engine)" : String,
      "[EngineMode](#cfn-rds-dbcluster-enginemode)" : String,
      "[EngineVersion](#cfn-rds-dbcluster-engineversion)" : String,
      "[KmsKeyId](#cfn-rds-dbcluster-kmskeyid)" : String,
      "[MasterUserPassword](#cfn-rds-dbcluster-masteruserpassword)" : String,
      "[MasterUsername](#cfn-rds-dbcluster-masterusername)" : String,
      "[Port](#cfn-rds-dbcluster-port)" : Integer,
      "[PreferredBackupWindow](#cfn-rds-dbcluster-preferredbackupwindow)" : String,
      "[PreferredMaintenanceWindow](#cfn-rds-dbcluster-preferredmaintenancewindow)" : String,
      "[ReplicationSourceIdentifier](#cfn-rds-dbcluster-replicationsourceidentifier)" : String,
      "[ScalingConfiguration](#cfn-rds-dbcluster-scalingconfiguration)" : [ScalingConfiguration](aws-properties-rds-dbcluster-scalingconfiguration.md),
      "[SnapshotIdentifier](#cfn-rds-dbcluster-snapshotidentifier)" : String,
      "[SourceRegion](#cfn-rds-dbcluster-sourceregion)" : String,
      "[StorageEncrypted](#cfn-rds-dbcluster-storageencrypted)" : Boolean,
      "[Tags](#cfn-rds-dbcluster-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcSecurityGroupIds](#cfn-rds-dbcluster-vpcsecuritygroupids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-rds-dbcluster-syntax.yaml"></a>

```
Type: AWS::RDS::DBCluster
Properties: 
  [AvailabilityZones](#cfn-rds-dbcluster-availabilityzones): 
    - String
  [BacktrackWindow](#cfn-rds-dbcluster-backtrackwindow): Long
  [BackupRetentionPeriod](#cfn-rds-dbcluster-backuprententionperiod): Integer
  [DBClusterIdentifier](#cfn-rds-dbcluster-dbclusteridentifier): String
  [DBClusterParameterGroupName](#cfn-rds-dbcluster-dbclusterparametergroupname): String
  [DBSubnetGroupName](#cfn-rds-dbcluster-dbsubnetgroupname): String
  [DatabaseName](#cfn-rds-dbcluster-databasename): String
  [DeletionProtection](#cfn-rds-dbcluster-deletionprotection): Boolean
  [EnableCloudwatchLogsExports](#cfn-rds-dbcluster-enablecloudwatchlogsexports): 
    - String
  [EnableIAMDatabaseAuthentication](#cfn-rds-dbcluster-enableiamdatabaseauthentication): Boolean
  [Engine](#cfn-rds-dbcluster-engine): String
  [EngineMode](#cfn-rds-dbcluster-enginemode): String
  [EngineVersion](#cfn-rds-dbcluster-engineversion): String
  [KmsKeyId](#cfn-rds-dbcluster-kmskeyid): String
  [MasterUserPassword](#cfn-rds-dbcluster-masteruserpassword): String
  [MasterUsername](#cfn-rds-dbcluster-masterusername): String
  [Port](#cfn-rds-dbcluster-port): Integer
  [PreferredBackupWindow](#cfn-rds-dbcluster-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-rds-dbcluster-preferredmaintenancewindow): String
  [ReplicationSourceIdentifier](#cfn-rds-dbcluster-replicationsourceidentifier): String
  [ScalingConfiguration](#cfn-rds-dbcluster-scalingconfiguration): 
    [ScalingConfiguration](aws-properties-rds-dbcluster-scalingconfiguration.md)
  [SnapshotIdentifier](#cfn-rds-dbcluster-snapshotidentifier): String
  [SourceRegion](#cfn-rds-dbcluster-sourceregion): String
  [StorageEncrypted](#cfn-rds-dbcluster-storageencrypted): Boolean
  [Tags](#cfn-rds-dbcluster-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcSecurityGroupIds](#cfn-rds-dbcluster-vpcsecuritygroupids): 
    - String
```

## Properties<a name="aws-resource-rds-dbcluster-properties"></a>

`AvailabilityZones`  <a name="cfn-rds-dbcluster-availabilityzones"></a>
A list of Availability Zones \(AZs\) where instances in the DB cluster can be created\. For information on AWS Regions and Availability Zones, see [Choosing the Regions and Availability Zones](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Concepts.RegionsAndAvailabilityZones.html) in the *Amazon Aurora User Guide*\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BacktrackWindow`  <a name="cfn-rds-dbcluster-backtrackwindow"></a>
The target backtrack window, in seconds\. To disable backtracking, set this value to 0\.   
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
 If this argument is omitted, `default.aurora5.6` is used\. If `default.aurora5.6` is used, specifying `aurora-mysql` or `aurora-postgresql` for the `Engine` property might result in an error\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBSubnetGroupName`  <a name="cfn-rds-dbcluster-dbsubnetgroupname"></a>
A DB subnet group that you want to associate with this DB cluster\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatabaseName`  <a name="cfn-rds-dbcluster-databasename"></a>
The name of your database\. If you don't provide a name, then Amazon RDS won't create a database in this DB cluster\. For naming constraints, see [Naming Constraints](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Limits.html#RDS_Limits.Constraints) in the *Amazon RDS User Guide*\.   
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
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableIAMDatabaseAuthentication`  <a name="cfn-rds-dbcluster-enableiamdatabaseauthentication"></a>
A value that indicates whether to enable mapping of AWS Identity and Access Management \(IAM\) accounts to database accounts\. By default, mapping is disabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engine`  <a name="cfn-rds-dbcluster-engine"></a>
The name of the database engine to be used for this DB cluster\.  
Valid Values: `aurora` \(for MySQL 5\.6\-compatible Aurora\), `aurora-mysql` \(for MySQL 5\.7\-compatible Aurora\), and `aurora-postgresql`   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineMode`  <a name="cfn-rds-dbcluster-enginemode"></a>
The DB engine mode of the DB cluster, either `provisioned`, `serverless`, `parallelquery`, or `global`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineVersion`  <a name="cfn-rds-dbcluster-engineversion"></a>
The version number of the database engine to use\.  
To prevent automatic upgrades, be sure to specify the full version number \(for example, 5\.6\.13\)\. If the default version for the database engine changes and you specify only the major version \(for example, 5\.6\), your DB instance will be upgraded to use the new default version\. Note that the default version is not necessarily the latest supported version\. 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-rds-dbcluster-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of the AWS Key Management Service master key that is used to encrypt the database instances in the DB cluster, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the `StorageEncrypted` property but don't specify this property, the default master key is used\. If you specify this property, you must set the `StorageEncrypted` property to `true`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUserPassword`  <a name="cfn-rds-dbcluster-masteruserpassword"></a>
The master password for the DB instance\.  
If you specify the `SourceDBInstanceIdentifier` or `DBSnapshotIdentifier` property, don't specify this property\. The value is inherited from the source DB instance or snapshot\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUsername`  <a name="cfn-rds-dbcluster-masterusername"></a>
The name of the master user for the DB cluster\.  
You must specify `MasterUsername`, unless you specify `SnapshotIdentifier`\. In that case, don't specify `MasterUsername`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-rds-dbcluster-port"></a>
The port number on which the instances in the DB cluster accept connections\.  
 Default: `3306` if engine is set as aurora or `5432` if set to aurora\-postgresql\.   
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
The Amazon Resource Name \(ARN\) of the source DB instance or DB cluster if this DB cluster is created as a Read Replica\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScalingConfiguration`  <a name="cfn-rds-dbcluster-scalingconfiguration"></a>
The `ScalingConfiguration` property type specifies the scaling configuration of an Aurora Serverless DB cluster\.  
*Required*: No  
*Type*: [ScalingConfiguration](aws-properties-rds-dbcluster-scalingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotIdentifier`  <a name="cfn-rds-dbcluster-snapshotidentifier"></a>
The identifier for the DB snapshot or DB cluster snapshot to restore from\.  
You can use either the name or the Amazon Resource Name \(ARN\) to specify a DB cluster snapshot\. However, you can use only the ARN to specify a DB snapshot\.  
Constraints:  
+ Must match the identifier of an existing Snapshot\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceRegion`  <a name="cfn-rds-dbcluster-sourceregion"></a>
The AWS Region which contains the source DB cluster when replicating a DB cluster\. For example, `us-east-1`\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageEncrypted`  <a name="cfn-rds-dbcluster-storageencrypted"></a>
Indicates whether the DB instance is encrypted\.  
If you specify the `DBClusterIdentifier`, `DBSnapshotIdentifier`, or `SourceDBInstanceIdentifier` property, don't specify this property\. The value is inherited from the cluster, snapshot, or source DB instance\.   
If you specify the `KmsKeyId` property, then you must enable encryption\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-rds-dbcluster-tags"></a>
Tags to assign to the DB cluster\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-rds-dbcluster-vpcsecuritygroupids"></a>
A list of EC2 VPC security groups to associate with this DB cluster\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-rds-dbcluster-return-values"></a>

### Ref<a name="aws-resource-rds-dbcluster-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the DB cluster\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-rds-dbcluster-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-rds-dbcluster-return-values-fn--getatt-fn--getatt"></a>

`Endpoint.Address`  <a name="Endpoint.Address-fn::getatt"></a>
The connection endpoint for the DB cluster\. For example: `mystack-mydbcluster-1apw1j4phylrk.cg034hpkmmjt.us-east-2.rds.amazonaws.com` 

`Endpoint.Port`  <a name="Endpoint.Port-fn::getatt"></a>
The port number that will accept connections on this DB cluster\. For example: `3306` 

`ReadEndpoint.Address`  <a name="ReadEndpoint.Address-fn::getatt"></a>
The reader endpoint for the DB cluster\. For example: `mystack-mydbcluster-ro-1apw1j4phylrk.cg034hpkmmjt.us-east-2.rds.amazonaws.com` 

## Examples<a name="aws-resource-rds-dbcluster--examples"></a>

### <a name="aws-resource-rds-dbcluster--examples--"></a>

The following example creates an Amazon Aurora DB cluster and adds two DB instances to it\. Because Amazon RDS automatically assigns a writer and reader DB instances in the cluster, use the cluster endpoint to read and write data, not the individual DB instance endpoints\. 

#### JSON<a name="aws-resource-rds-dbcluster--examples----json"></a>

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
                "sql_mode": "IGNORE_SPACE"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbcluster--examples----yaml"></a>

```
--- 
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
      ? "Fn::GetAtt"
      : 
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
      ? "Fn::GetAtt"
      : 
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
  Properties: 
    Description: "CloudFormation Sample Aurora Parameter Group"
    Family: aurora5.6
    Parameters: 
      sql_mode: IGNORE_SPACE
  Type: "AWS::RDS::DBParameterGroup"
```