# AWS::DocDB::DBCluster<a name="aws-resource-docdb-dbcluster"></a>

The `AWS::DocDB::DBCluster` Amazon DocumentDB \(with MongoDB compatibility\) resource describes a DBCluster\. Amazon DocumentDB is a fully managed, MongoDB\-compatible document database engine\. For more information, see [DBCluster](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DBCluster.html) in the *Amazon DocumentDB Developer Guide*\. 

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
      "[DeletionProtection](#cfn-docdb-dbcluster-deletionprotection)" : Boolean,
      "[EnableCloudwatchLogsExports](#cfn-docdb-dbcluster-enablecloudwatchlogsexports)" : [ String, ... ],
      "[EngineVersion](#cfn-docdb-dbcluster-engineversion)" : String,
      "[KmsKeyId](#cfn-docdb-dbcluster-kmskeyid)" : String,
      "[MasterUsername](#cfn-docdb-dbcluster-masterusername)" : String,
      "[MasterUserPassword](#cfn-docdb-dbcluster-masteruserpassword)" : String,
      "[Port](#cfn-docdb-dbcluster-port)" : Integer,
      "[PreferredBackupWindow](#cfn-docdb-dbcluster-preferredbackupwindow)" : String,
      "[PreferredMaintenanceWindow](#cfn-docdb-dbcluster-preferredmaintenancewindow)" : String,
      "[SnapshotIdentifier](#cfn-docdb-dbcluster-snapshotidentifier)" : String,
      "[StorageEncrypted](#cfn-docdb-dbcluster-storageencrypted)" : Boolean,
      "[Tags](#cfn-docdb-dbcluster-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcSecurityGroupIds](#cfn-docdb-dbcluster-vpcsecuritygroupids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-docdb-dbcluster-syntax.yaml"></a>

```
Type: AWS::DocDB::DBCluster
Properties: 
  [AvailabilityZones](#cfn-docdb-dbcluster-availabilityzones): 
    - String
  [BackupRetentionPeriod](#cfn-docdb-dbcluster-backupretentionperiod): Integer
  [DBClusterIdentifier](#cfn-docdb-dbcluster-dbclusteridentifier): String
  [DBClusterParameterGroupName](#cfn-docdb-dbcluster-dbclusterparametergroupname): String
  [DBSubnetGroupName](#cfn-docdb-dbcluster-dbsubnetgroupname): String
  [DeletionProtection](#cfn-docdb-dbcluster-deletionprotection): Boolean
  [EnableCloudwatchLogsExports](#cfn-docdb-dbcluster-enablecloudwatchlogsexports): 
    - String
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
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcSecurityGroupIds](#cfn-docdb-dbcluster-vpcsecuritygroupids): 
    - String
```

## Properties<a name="aws-resource-docdb-dbcluster-properties"></a>

`AvailabilityZones`  <a name="cfn-docdb-dbcluster-availabilityzones"></a>
A list of Amazon EC2 Availability Zones that instances in the cluster can be created in\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BackupRetentionPeriod`  <a name="cfn-docdb-dbcluster-backupretentionperiod"></a>
The number of days for which automated backups are retained\. You must specify a minimum value of 1\.  
Default: 1  
Constraints:  
+ Must be a value from 1 to 35\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBClusterIdentifier`  <a name="cfn-docdb-dbcluster-dbclusteridentifier"></a>
The cluster identifier\. This parameter is stored as a lowercase string\.  
Constraints:  
+ Must contain from 1 to 63 letters, numbers, or hyphens\. 
+ The first character must be a letter\.
+ Cannot end with a hyphen or contain two consecutive hyphens\. 
Example: `my-cluster`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBClusterParameterGroupName`  <a name="cfn-docdb-dbcluster-dbclusterparametergroupname"></a>
The name of the cluster parameter group to associate with this cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBSubnetGroupName`  <a name="cfn-docdb-dbcluster-dbsubnetgroupname"></a>
A subnet group to associate with this cluster\.  
Constraints: Must match the name of an existing `DBSubnetGroup`\. Must not be default\.  
Example: `mySubnetgroup`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeletionProtection`  <a name="cfn-docdb-dbcluster-deletionprotection"></a>
Protects clusters from being accidentally deleted\. If enabled, the cluster cannot be deleted unless it is modified and `DeletionProtection` is disabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableCloudwatchLogsExports`  <a name="cfn-docdb-dbcluster-enablecloudwatchlogsexports"></a>
The list of log types that need to be enabled for exporting to Amazon CloudWatch Logs\. You can enable audit logs or profiler logs\. For more information, see [Auditing Amazon DocumentDB Events](https://docs.aws.amazon.com/documentdb/latest/developerguide/event-auditing.html) and [Profiling Amazon DocumentDB Operations](https://docs.aws.amazon.com/documentdb/latest/developerguide/profiling.html)\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineVersion`  <a name="cfn-docdb-dbcluster-engineversion"></a>
The version number of the database engine to use\. The \-\-engine\-version will default to the latest major engine version\. For production workloads, we recommend explicitly declaring this parameter with the intended major engine version\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-docdb-dbcluster-kmskeyid"></a>
The AWS KMS key identifier for an encrypted cluster\.  
The AWS KMS key identifier is the Amazon Resource Name \(ARN\) for the AWS KMS encryption key\. If you are creating a cluster using the same AWS account that owns the AWS KMS encryption key that is used to encrypt the new cluster, you can use the AWS KMS key alias instead of the ARN for the AWS KMS encryption key\.  
If an encryption key is not specified in `KmsKeyId`:   
+ If the `StorageEncrypted` parameter is `true`, Amazon DocumentDB uses your default encryption key\. 
AWS KMS creates the default encryption key for your AWS account\. Your AWS account has a different default encryption key for each AWS Region\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUsername`  <a name="cfn-docdb-dbcluster-masterusername"></a>
The name of the master user for the cluster\.  
Constraints:  
+ Must be from 1 to 63 letters or numbers\.
+ The first character must be a letter\.
+ Cannot be a reserved word for the chosen database engine\. 
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUserPassword`  <a name="cfn-docdb-dbcluster-masteruserpassword"></a>
The password for the master database user\. This password can contain any printable ASCII character except forward slash \(/\), double quote \("\), or the "at" symbol \(@\)\.  
Constraints: Must contain from 8 to 100 characters\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-docdb-dbcluster-port"></a>
Specifies the port that the database engine is listening on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredBackupWindow`  <a name="cfn-docdb-dbcluster-preferredbackupwindow"></a>
The daily time range during which automated backups are created if automated backups are enabled using the `BackupRetentionPeriod` parameter\.   
The default is a 30\-minute window selected at random from an 8\-hour block of time for each AWS Region\.   
Constraints:  
+ Must be in the format `hh24:mi-hh24:mi`\.
+ Must be in Universal Coordinated Time \(UTC\)\.
+ Must not conflict with the preferred maintenance window\. 
+ Must be at least 30 minutes\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-docdb-dbcluster-preferredmaintenancewindow"></a>
The weekly time range during which system maintenance can occur, in Universal Coordinated Time \(UTC\)\.  
Format: `ddd:hh24:mi-ddd:hh24:mi`   
The default is a 30\-minute window selected at random from an 8\-hour block of time for each AWS Region, occurring on a random day of the week\.  
Valid days: Mon, Tue, Wed, Thu, Fri, Sat, Sun  
Constraints: Minimum 30\-minute window\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotIdentifier`  <a name="cfn-docdb-dbcluster-snapshotidentifier"></a>
The identifier for the snapshot or cluster snapshot to restore from\.  
You can use either the name or the Amazon Resource Name \(ARN\) to specify a cluster snapshot\. However, you can use only the ARN to specify a snapshot\.  
Constraints:  
+ Must match the identifier of an existing snapshot\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageEncrypted`  <a name="cfn-docdb-dbcluster-storageencrypted"></a>
Specifies whether the cluster is encrypted\.  
*Required*: Conditional  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-docdb-dbcluster-tags"></a>
The tags to be assigned to the cluster\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-docdb-dbcluster-vpcsecuritygroupids"></a>
A list of EC2 VPC security groups to associate with this cluster\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-docdb-dbcluster-return-values"></a>

### Ref<a name="aws-resource-docdb-dbcluster-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the DBClusterIdentifier, such as `mycluster`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-docdb-dbcluster-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-docdb-dbcluster-return-values-fn--getatt-fn--getatt"></a>

`ClusterResourceId`  <a name="ClusterResourceId-fn::getatt"></a>
The resource id for the cluster; for example: `cluster-ABCD1234EFGH5678IJKL90MNOP`\. The cluster ID uniquely identifies the cluster and is used in things like IAM authentication policies\. 

`Endpoint`  <a name="Endpoint-fn::getatt"></a>
The connection endpoint for the cluster, such as `sample-cluster.cluster-cozrlsfrcjoc.us-east-1.docdb.amazonaws.com`\.

`Port`  <a name="Port-fn::getatt"></a>
The port number on which the cluster accepts connections\. For example: `27017`\.

`ReadEndpoint`  <a name="ReadEndpoint-fn::getatt"></a>
The reader endpoint for the cluster\. For example: `sample-cluster.cluster-ro-cozrlsfrcjoc.us-east-1.docdb.amazonaws.com`\.

## Examples<a name="aws-resource-docdb-dbcluster--examples"></a>



### <a name="aws-resource-docdb-dbcluster--examples--"></a>



#### JSON<a name="aws-resource-docdb-dbcluster--examples----json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myDBInstance" : {
         "Type" : "AWS::DocDB::DBCluster",
         "Properties" : {
            "BackupRetentionPeriod" : 8,
            "DBClusterIdentifier" : "sample-cluster",
            "DBClusterParameterGroupName" : "default.docdb3.6",
            "DBSubnetGroupName" : "default",
            "KmsKeyId" : "your-kms-key-id",
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

#### YAML<a name="aws-resource-docdb-dbcluster--examples----yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
   myDBInstance: 
      Type: "AWS::DocDB::DBCluster"
      Properties: 
         BackupRetentionPeriod : 8
         DBClusterIdentifier : "sample-cluster"
         DBClusterParameterGroupName : "default.docdb3.6"
         DBSubnetGroupName : "default"
         KmsKeyId : "your-kms-key-id"
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

## See also<a name="aws-resource-docdb-dbcluster--seealso"></a>
+  [DBCluster](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DBCluster.html) 
+  [CreateDBCluster](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_CreateDBCluster.html) 
+  [DeleteDBCluster](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DeleteDBCluster.html) 
+  [DescribeDBClusters](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DescribeDBClusters.html) 
+  [ModifyDBCluster](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_ModifyDBCluster.html) 

