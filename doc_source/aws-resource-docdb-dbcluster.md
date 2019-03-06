# AWS::DocDB::DBCluster<a name="aws-resource-docdb-dbcluster"></a>

The `AWS::DocDB::DBCluster` Amazon DocumentDB \(with MongoDB compatibility\) resource describes a DBCluster\. Amazon DocumentDB is a fully managed, MongoDB\-compatible document database engine\. For more information, see [DBCluster](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DBCluster) in the *Amazon DocumentDB Developer Guide*\.

You can only use this resource in regions supported by Amazon DocumentDB\. For more information, see [Choosing Regions and Availability Zones](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/regions-and-azs.html)\.

**Topics**
+ [Syntax](#aws-resource-docdb-dbcluster-syntax)
+ [Properties](#aws-resource-docdb-dbcluster-properties)
+ [Return Values](#aws-resource-docdb-dbcluster-returnvalues)
+ [Examples](#aws-resource-docdb-dbcluster-examples)
+ [See Also](#aws-resource-docdb-dbcluster-seealso)

## Syntax<a name="aws-resource-docdb-dbcluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-docdb-dbcluster-syntax.json"></a>

```
{
  "Type" : "AWS::DocDB::DBCluster",
  "Properties" : {
    "[AvailabilityZones](#cfn-docdb-dbcluster-availabilityzones)" : [ String, ... ],
    "[BackupRetentionPeriod](#cfn-docdb-dbcluster-backupretentionperiod)" : Integer,
    "[DBClusterIdentifier](#cfn-docdb-dbcluster-dbclusteridentifier)" : String,
    "[DBClusterParameterGroupName](#cfn-docdb-dbcluster-dbclusterparametergroupname)" : String,
    "[DBSubnetGroupName](#cfn-docdb-dbcluster-dbsubnetgroupname)" : String,
    "[EngineVersion](#cfn-docdb-dbcluster-engineversion) : String,
    "[KmsKeyId](#cfn-docdb-dbcluster-kmskeyid)" : String,
    "[MasterUsername](#cfn-docdb-dbcluster-masterusername)" : String,
    "[MasterUserPassword](#cfn-docdb-dbcluster-masteruserpassword)" : String,
    "[Port](#cfn-docdb-dbcluster-port)" : Integer,
    "[PreferredBackupWindow](#cfn-docdb-dbcluster-preferredbackupwindow)" : String,
    "[PreferredMaintenanceWindow](#cfn-docdb-dbcluster-preferredmaintenancewindow)" : String,
    "[SnapshotIdentifier](#cfn-docdb-dbcluster-snapshotidentifier)" : String,
    "[StorageEncrypted](#cfn-docdb-dbcluster-storageencrypted)" : Boolean,
    "[Tags](#cfn-docdb-dbcluster-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ],
    "[VpcSecurityGroupIds](#cfn-docdb-dbcluster-vpcsecuritygroupids)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-docdb-dbcluster-syntax.yaml"></a>

```
Type: "AWS::DocDB::DBCluster"
Properties:
  [AvailabilityZones](#cfn-docdb-dbcluster-availabilityzones): 
    - String
  [BackupRetentionPeriod](#cfn-docdb-dbcluster-backupretentionperiod): Integer
  [DBClusterIdentifier](#cfn-docdb-dbcluster-dbclusteridentifier): String
  [DBClusterParameterGroupName](#cfn-docdb-dbcluster-dbclusterparametergroupname): String
  [DBSubnetGroupName](#cfn-docdb-dbcluster-dbsubnetgroupname): String
  [EngineVersion](#cfn-docdb-dbcluster-engineversion): String
  [KmsKeyId](#cfn-docdb-dbcluster-kmskeyid): String
  [MasterUsername](#cfn-docdb-dbcluster-masterusername): String
  [MasterUserPassword](#cfn-docdb-dbcluster-masteruserpassword): String
  [Port](#cfn-docdb-dbcluster-port): Integer
  [PreferredBackupWindow](#cfn-docdb-dbcluster-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-docdb-dbcluster-preferredmaintenancewindow): String
  [SnapshotIdentifier](#cfn-docdb-dbcluster-snapshotidentifier): String
  [StorageEncrypted](#cfn-docdb-dbcluster-storageencrypted): Boolean
  [Tags](#cfn-docdb-dbcluster-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
  [VpcSecurityGroupIds](#cfn-docdb-dbcluster-vpcsecuritygroupids): 
    - String
```

## Properties<a name="aws-resource-docdb-dbcluster-properties"></a>

`AvailabilityZones`  <a name="cfn-docdb-dbcluster-availabilityzones"></a>
A list of Availability Zones \(AZs\) in which DB instances in the cluster can be created\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`BackupRetentionPeriod`  <a name="cfn-docdb-dbcluster-backupretentionperiod"></a>
The number of days for which automatic backups are retained\. For more information, see [Comparing Automatic and Manual Snapshots](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/backup-restore.snapshots.html) in the *Amazon DocumentDB Developer Guide*\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DBClusterIdentifier`  <a name="cfn-docdb-dbcluster-dbclusteridentifier"></a>
The DB cluster identifier\. This parameter is stored as a lowercase string\.  

**Constraints:**
+ Length is between \[1\-63\] letters, numbers, or hyphens
+ First character must be a letter
+ Cannot end with a hyphen or contain two consecutive hyphens
+ Must be unique for all clusters \(across Amazon RDS, Neptune and Amazon DocumentDB\) per AWS account, per region\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DBClusterParameterGroupName`  <a name="cfn-docdb-dbcluster-dbclusterparametergroupname"></a>
The name of the DB cluster parameter group to associate with this DB cluster\.   
If this argument is omitted, `default.docdb3.6` is used\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DBSubnetGroupName`  <a name="cfn-docdb-dbcluster-dbsubnetgroupname"></a>
A DB subnet group that you want to associate with this DB cluster\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`EngineVersion`  <a name="cfn-docdb-dbcluster-engineversion"></a>
The version number of the database engine that you want to use\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`KmsKeyId`  <a name="cfn-docdb-dbcluster-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of the AWS Key Management Service master key that is used to encrypt the DB instances in the DB cluster, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the `StorageEncrypted` property but don't specify this property, the default master key is used\. If you specify this property, you must set the `StorageEncrypted` property to `true`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`MasterUsername`  <a name="cfn-docdb-dbcluster-masterusername"></a>
The master user name for the DB instance\.  
*Required*: Conditional\. You must specify this property unless you specify the `SnapshotIdentifier` property\. In that case, do not specify this property\.  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`MasterUserPassword`  <a name="cfn-docdb-dbcluster-masteruserpassword"></a>
The password for the master database user\.  
*Required*: Conditional\. You must specify this property unless you specify the `SnapshotIdentifier` property\. In that case, do not specify this property\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Port`  <a name="cfn-docdb-dbcluster-port"></a>
The port number on which the DB instances in the cluster can accept connections\. If this argument is omitted, `27017` is used\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PreferredBackupWindow`  <a name="cfn-docdb-dbcluster-preferredbackupwindow"></a>
If automated backups are enabled \(see the `BackupRetentionPeriod` property\), the daily time range in UTC during which automated backups are created\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PreferredMaintenanceWindow`  <a name="cfn-docdb-dbcluster-preferredmaintenancewindow"></a>
The weekly time range \(in UTC\) during which system maintenance can occur\.  
For valid values, see the `PreferredMaintenanceWindow` parameter of the [CreateDBCluster](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_CreateDBCluster.html) action in the *Amazon DocumentDB Developer Guide*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SnapshotIdentifier`  <a name="cfn-docdb-dbcluster-snapshotidentifier"></a>
The identifier for the DB cluster snapshot from which you want to restore\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`StorageEncrypted`  <a name="cfn-docdb-dbcluster-storageencrypted"></a>
Indicates whether the DB instances in the cluster are encrypted\.  
*Required*: Conditional\. If you specify the `KmsKeyId` property, you must enable encryption\.  
 *Type*: Boolean  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-docdb-dbcluster-tags"></a>
A list of up to 50 tags\. A tag is metadata assigned to an Amazon DocumentDB resource consisting of a key\-value pair\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VpcSecurityGroupIds`  <a name="cfn-docdb-dbcluster-vpcsecuritygroupids"></a>
A list of VPC security groups to associate with this DB cluster\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-docdb-dbcluster-returnvalues"></a>

### Ref<a name="aws-resource-docdb-dbcluster-ref"></a>

When you pass the logical ID of an `AWS::DocDB::DBCluster` resource to the intrinsic `Ref` function, the function returns the DB cluster identifier, such as `MyCluster`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-docdb-dbcluster-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`ClusterResourceId`  
The resource id for the DB cluster; for example: `cluster-ABCD1234EFGH5678IJKL90MNOP`\. The cluster ID uniquely identifies the cluster and is used in things like IAM authentication policies\.

`Endpoint`  
The connection endpoint for the DB cluster, such as `"sample-cluster.cluster-cozrlsfrcjoc.us-east-1.docdb.amazonaws.com`\.

`Port`  
The port number on which the DB cluster accepts connections\. For example: `27017`\.

`ReadEndpoint`  
The reader endpoint for the DB cluster\. For example: `sample-cluster.cluster-ro-cozrlsfrcjoc.us-east-1.docdb.amazonaws.com`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-docdb-dbcluster-examples"></a>

### JSON<a name="aws-resource-docdb-dbcluster-example1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myDBInstance" : {
         "Type" : "AWS::DocDB::DBCluster",
         "Properties" : {
            "BackupRetentionPeriod" : 8,
            "DBClusterIdentufier" : "sample-cluster",
            "DBClusterParameterGroupName" : "default.docdb3.6",
            "DBSubnetGroupName" : "default",
            "KMSKeyId" : "your-kms-key-id",
            "MasterUsername" : "your-master-username",
            "MasterUserPassword" : "your-master-user-password",
            "Port" : "27017",
            "PreferredBackupWindow" : "07:34-08:04",
            "PreferredMaintenanceWindow" : "sat:04:51-sat:05:21",
            "SnapshotIdentifier" : "sample-cluster-snapshot-id",
            "StorageEncrypted" : true,
            "Tags" : [ {"Key" : "String", "Value" : "String"} ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-docdb-dbcluster-example1.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myDBInstance: 
    Type: "AWS::DocDB::DBCluster"
    Properties: 
      BackupRetentionPeriod : 8
      DBClusterIdentufier : "sample-cluster"
      DBClusterParameterGroupName : "default.docdb3.6"
      DBSubnetGroupName : "default"
      KMSKeyId : "your-kms-key-id"
      MasterUsername : "your-master-username"
      MasterUserPassword : "your-master-user-password"
      Port : "27017"
      PreferredBackupWindow : "07:34-08:04"
      PreferredMaintenanceWindow : "sat:04:51-sat:05:21"
      SnapshotIdentifier : "sample-cluster-snapshot-id"
      StorageEncrypted : true
      Tags: 
        - 
          Key: "String"
          Value: "String"
```

## See Also<a name="aws-resource-docdb-dbcluster-seealso"></a>

For more information, see the following topics in the *Amazon DocumentDB Developer Guide*\.
+ [DBCluster](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DBCluster.html)
+ [CreateDBCluster](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_CreateDBCluster.html)
+ [DeleteDBCluster](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DeleteDBCluster.html)
+ [DescribeDBClusters](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DescribeDBClusters.html)
+ [ModifyDBCluster](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_ModifyDBCluster.html)