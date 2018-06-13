# AWS::RDS::DBCluster<a name="aws-resource-rds-dbcluster"></a>

The `AWS::RDS::DBCluster` resource creates a cluster, such as an Aurora for Amazon RDS \(Amazon Aurora\) DB cluster\. Amazon Aurora is a fully managed, MySQL\-compatible, relational database engine\. For more information, see [Aurora on Amazon RDS](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Aurora.html) in the *Amazon RDS User Guide*\.

**Note**  
Currently, you can create this resource only in regions in which Amazon Aurora is supported\.

The default DeletionPolicy for `AWS::RDS::DBCluster` resources is `Snapshot`\. For more information about how AWS CloudFormation deletes resources, see [DeletionPolicy Attribute](aws-attribute-deletionpolicy.md)\.

**Topics**
+ [Syntax](#aws-resource-rds-dbcluster-syntax)
+ [Properties](#w3ab2c21c10d947c15)
+ [Return Values](#aws-resource-rds-dbcluster-ref)
+ [Example](#w3ab2c21c10d947c19)

## Syntax<a name="aws-resource-rds-dbcluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbcluster-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBCluster",
  "Properties" :
  {
    "[AvailabilityZones](#cfn-rds-dbcluster-availabilityzones)" : [ String, ... ],
    "[BackupRetentionPeriod](#cfn-rds-dbcluster-backuprententionperiod)" : Integer,
    "[DatabaseName](#cfn-rds-dbcluster-databasename)" : String,   
    "[DBClusterIdentifier](#cfn-rds-dbcluster-dbclusteridentifier)" : String,
    "[DBClusterParameterGroupName](#cfn-rds-dbcluster-dbclusterparametergroupname)" : String,
    "[DBSubnetGroupName](#cfn-rds-dbcluster-dbsubnetgroupname)" : String,
    "[Engine](#cfn-rds-dbcluster-engine)" : String,
    "[EngineVersion](#cfn-rds-dbcluster-engineversion)" : String,
    "[KmsKeyId](#cfn-rds-dbcluster-kmskeyid)" : String,
    "[MasterUsername](#cfn-rds-dbcluster-masterusername)" : String,
    "[MasterUserPassword](#cfn-rds-dbcluster-masteruserpassword)" : String,
    "[Port](#cfn-rds-dbcluster-port)" : Integer,
    "[PreferredBackupWindow](#cfn-rds-dbcluster-preferredbackupwindow)" : String,
    "[PreferredMaintenanceWindow](#cfn-rds-dbcluster-preferredmaintenancewindow)" : String,
    "[ReplicationSourceIdentifier](#cfn-rds-dbcluster-replicationsourceidentifier)" : String,
    "[SnapshotIdentifier](#cfn-rds-dbcluster-snapshotidentifier)" : String,
    "[StorageEncrypted](#cfn-rds-dbcluster-storageencrypted)" : Boolean,
    "[Tags](#cfn-rds-dbcluster-tags)" : [ Resource Tag, ... ],
    "[VpcSecurityGroupIds](#cfn-rds-dbcluster-vpcsecuritygroupids)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-rds-dbcluster-syntax.yaml"></a>

```
Type: "AWS::RDS::DBCluster"
Properties:
  [AvailabilityZones](#cfn-rds-dbcluster-availabilityzones):
    - String
  [BackupRetentionPeriod](#cfn-rds-dbcluster-backuprententionperiod): Integer
  [DatabaseName](#cfn-rds-dbcluster-databasename): String
  [DBClusterIdentifier](#cfn-rds-dbcluster-dbclusteridentifier): String
  [DBClusterParameterGroupName](#cfn-rds-dbcluster-dbclusterparametergroupname): String
  [DBSubnetGroupName](#cfn-rds-dbcluster-dbsubnetgroupname): String
  [Engine](#cfn-rds-dbcluster-engine): String
  [EngineVersion](#cfn-rds-dbcluster-engineversion): String
  [KmsKeyId](#cfn-rds-dbcluster-kmskeyid): String
  [MasterUsername](#cfn-rds-dbcluster-masterusername): String
  [MasterUserPassword](#cfn-rds-dbcluster-masteruserpassword): String
  [Port](#cfn-rds-dbcluster-port): Integer
  [PreferredBackupWindow](#cfn-rds-dbcluster-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-rds-dbcluster-preferredmaintenancewindow): String
  [ReplicationSourceIdentifier](#cfn-rds-dbcluster-replicationsourceidentifier): String
  [SnapshotIdentifier](#cfn-rds-dbcluster-snapshotidentifier): String
  [StorageEncrypted](#cfn-rds-dbcluster-storageencrypted): Boolean
  [Tags](#cfn-rds-dbcluster-tags):
    - Resource Tag
  [VpcSecurityGroupIds](#cfn-rds-dbcluster-vpcsecuritygroupids):
    - String
```

## Properties<a name="w3ab2c21c10d947c15"></a>

`AvailabilityZones`  <a name="cfn-rds-dbcluster-availabilityzones"></a>
A list of Availability Zones \(AZs\) in which DB instances in the cluster can be created\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`BackupRetentionPeriod`  <a name="cfn-rds-dbcluster-backuprententionperiod"></a>
The number of days for which automatic backups are retained\. For more information, see [CreateDBCluster](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBCluster.html) in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. For more information, see [ModifyDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html) in the *Amazon RDS API Reference*\.

`DatabaseName`  <a name="cfn-rds-dbcluster-databasename"></a>
The name of your database\. If you don't provide a name, Amazon Relational Database Service \(Amazon RDS\) won't create a database in this DB cluster\. For naming constraints, see [ Naming Constraints in Amazon RDS](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Limits.html#RDS_Limits.Constraints) in the *Amazon RDS User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBClusterIdentifier`  <a name="cfn-rds-dbcluster-dbclusteridentifier"></a>
The DB cluster identifier\. This parameter is stored as a lowercase string\.   
Constraints:  
+ Must contain from 1 to 63 letters, numbers, or hyphens\.
+ First character must be a letter\.
+ Cannot end with a hyphen or contain two consecutive hyphens\.
For additional information, see the `DBClusterIdentifier` parameter of the [CreateDBCluster](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBCluster.html) action in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBClusterParameterGroupName`  <a name="cfn-rds-dbcluster-dbclusterparametergroupname"></a>
The name of the DB cluster parameter group to associate with this DB cluster\. For the default value, see the `DBClusterParameterGroupName` parameter of the [CreateDBCluster](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBCluster.html) action in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`DBSubnetGroupName`  <a name="cfn-rds-dbcluster-dbsubnetgroupname"></a>
A DB subnet group that you want to associate with this DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Engine`  <a name="cfn-rds-dbcluster-engine"></a>
The name of the database engine that you want to use for this DB cluster\.  
For valid values, see the `Engine` parameter of the [CreateDBCluster](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBCluster.html) action in the *Amazon RDS API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EngineVersion`  <a name="cfn-rds-dbcluster-engineversion"></a>
The version number of the database engine that you want to use\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`KmsKeyId`  <a name="cfn-rds-dbcluster-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of the AWS Key Management Service master key that is used to encrypt the database instances in the DB cluster, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the `StorageEncrypted` property but don't specify this property, the default master key is used\. If you specify this property, you must set the `StorageEncrypted` property to `true`\.  
If you specify the `SnapshotIdentifier`, do not specify this property\. The value is inherited from the snapshot DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`MasterUsername`  <a name="cfn-rds-dbcluster-masterusername"></a>
The master user name for the DB instance\.  
*Required*: Conditional\. You must specify this property unless you specify the `SnapshotIdentifier` property\. In that case, do not specify this property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`MasterUserPassword`  <a name="cfn-rds-dbcluster-masteruserpassword"></a>
The password for the master database user\.  
*Required*: Conditional\. You must specify this property unless you specify the `SnapshotIdentifier` property\. In that case, do not specify this property\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Port`  <a name="cfn-rds-dbcluster-port"></a>
The port number on which the DB instances in the cluster can accept connections\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PreferredBackupWindow`  <a name="cfn-rds-dbcluster-preferredbackupwindow"></a>
if automated backups are enabled \(see the `BackupRetentionPeriod` property\), the daily time range in UTC during which you want to create automated backups\.  
For valid values, see the `PreferredBackupWindow` parameter of the [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) action in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-rds-dbcluster-preferredmaintenancewindow"></a>
The weekly time range \(in UTC\) during which system maintenance can occur\.  
For valid values, see the `PreferredMaintenanceWindow` parameter of the [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) action in the *Amazon RDS API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. For more information, see [ModifyDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html) in the *Amazon RDS API Reference*\.

`ReplicationSourceIdentifier`  <a name="cfn-rds-dbcluster-replicationsourceidentifier"></a>
The Amazon Resource Name \(ARN\) of the source Amazon RDS MySQL DB instance or DB cluster, if this DB cluster is created as a Read Replica\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SnapshotIdentifier`  <a name="cfn-rds-dbcluster-snapshotidentifier"></a>
The identifier for the DB cluster snapshot from which you want to restore\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`StorageEncrypted`  <a name="cfn-rds-dbcluster-storageencrypted"></a>
Indicates whether the DB instances in the cluster are encrypted\.  
If you specify the `SnapshotIdentifier` property, do not specify this property\. The value is inherited from the snapshot DB cluster\.  
*Required*: Conditional\. If you specify the `KmsKeyId` property, you must enable encryption\.  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`Tags`  <a name="cfn-rds-dbcluster-tags"></a>
The tags that you want to attach to this DB cluster\.  
*Required*: No  
*Type*: A list of [resource tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-rds-dbcluster-vpcsecuritygroupids"></a>
A list of VPC security groups to associate with this DB cluster\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-rds-dbcluster-ref"></a>

### Ref<a name="w3ab2c21c10d947c17b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d947c17b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Endpoint.Address`  
The connection endpoint for the DB cluster\. For example: `mystack-mydbcluster-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`\.

`Endpoint.Port`  
The port number on which the Amazon Redshift cluster accepts connections\. For example: `5439`\.

`ReadEndpoint.Address`  
The reader endpoint for the DB cluster\. For example: `mystack-mydbcluster-ro-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="w3ab2c21c10d947c19"></a>

The following snippet creates an Amazon Aurora DB cluster and adds two DB instances to it\. Because Amazon RDS automatically assigns a writer and reader DB instances in the cluster, use the cluster endpoint to read and write data, not the individual DB instance endpoints\.

### JSON<a name="aws-resource-rds-dbcluster-example.json"></a>

```
"RDSCluster" : {
  "Type" : "AWS::RDS::DBCluster",
  "Properties" : {
    "MasterUsername" : { "Ref" : "username" },
    "MasterUserPassword" : { "Ref" : "password" },
    "Engine" : "aurora",
    "DBSubnetGroupName" : { "Ref" : "DBSubnetGroup" },
    "DBClusterParameterGroupName" : { "Ref" : "RDSDBClusterParameterGroup" }
  }
},
"RDSDBInstance1" : {
  "Type" : "AWS::RDS::DBInstance",
  "Properties" : {
    "DBSubnetGroupName" : {
      "Ref" : "DBSubnetGroup"
    },
    "DBParameterGroupName" :{"Ref": "RDSDBParameterGroup"},
    "Engine" : "aurora",
    "DBClusterIdentifier" : {
      "Ref" : "RDSCluster"
    },
    "PubliclyAccessible" : "true",
    "AvailabilityZone" : { "Fn::GetAtt" : [ "Subnet1", "AvailabilityZone" ] },
    "DBInstanceClass" : "db.r3.xlarge"
  }
},
"RDSDBInstance2" : {
  "Type" : "AWS::RDS::DBInstance",
  "Properties" : {
    "DBSubnetGroupName" : {
      "Ref" : "DBSubnetGroup"
    },
    "DBParameterGroupName" :{"Ref": "RDSDBParameterGroup"},
    "Engine" : "aurora",
    "DBClusterIdentifier" : {
      "Ref" : "RDSCluster"
    },
    "PubliclyAccessible" : "true",
    "AvailabilityZone" : { "Fn::GetAtt" : [ "Subnet2", "AvailabilityZone" ] },
    "DBInstanceClass" : "db.r3.xlarge"
  }
},
"RDSDBClusterParameterGroup" : {
  "Type": "AWS::RDS::DBClusterParameterGroup",
  "Properties" : {
    "Description" : "CloudFormation Sample Aurora Cluster Parameter Group",
    "Family" : "aurora5.6",
    "Parameters" : {
      "time_zone" : "US/Eastern"
    }
  }
},
"RDSDBParameterGroup": {
  "Type": "AWS::RDS::DBParameterGroup",
  "Properties" : {
    "Description" : "CloudFormation Sample Aurora Parameter Group",
    "Family" : "aurora5.6",
    "Parameters" : {
      "sql_mode": "IGNORE_SPACE"
    }
  }
}
```

### YAML<a name="aws-resource-rds-dbcluster-example.yaml"></a>

```
RDSCluster:
  Type: AWS::RDS::DBCluster
  Properties:
    MasterUsername:
      Ref: username
    MasterUserPassword:
      Ref: password
    Engine: aurora
    DBSubnetGroupName:
      Ref: DBSubnetGroup
    DBClusterParameterGroupName:
      Ref: RDSDBClusterParameterGroup
RDSDBInstance1:
  Type: AWS::RDS::DBInstance
  Properties:
    DBSubnetGroupName:
      Ref: DBSubnetGroup
    DBParameterGroupName:
      Ref: RDSDBParameterGroup
    Engine: aurora
    DBClusterIdentifier:
      Ref: RDSCluster
    PubliclyAccessible: 'true'
    AvailabilityZone:
      Fn::GetAtt:
      - Subnet1
      - AvailabilityZone
    DBInstanceClass: db.r3.xlarge
RDSDBInstance2:
  Type: AWS::RDS::DBInstance
  Properties:
    DBSubnetGroupName:
      Ref: DBSubnetGroup
    DBParameterGroupName:
      Ref: RDSDBParameterGroup
    Engine: aurora
    DBClusterIdentifier:
      Ref: RDSCluster
    PubliclyAccessible: 'true'
    AvailabilityZone:
      Fn::GetAtt:
      - Subnet2
      - AvailabilityZone
    DBInstanceClass: db.r3.xlarge
RDSDBClusterParameterGroup:
  Type: AWS::RDS::DBClusterParameterGroup
  Properties:
    Description: CloudFormation Sample Aurora Cluster Parameter Group
    Family: aurora5.6
    Parameters:
      time_zone: US/Eastern
RDSDBParameterGroup:
  Type: AWS::RDS::DBParameterGroup
  Properties:
    Description: CloudFormation Sample Aurora Parameter Group
    Family: aurora5.6
    Parameters:
      sql_mode: IGNORE_SPACE
```