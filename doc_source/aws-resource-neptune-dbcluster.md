# AWS::Neptune::DBCluster<a name="aws-resource-neptune-dbcluster"></a>

The `AWS::Neptune::DBCluster` resource creates an Amazon Neptune DB cluster\. Neptune is a fully managed graph database\.

**Note**  
Currently, you can create this resource only in AWS Regions in which Amazon Neptune is supported\.

If no `DeletionPolicy` is set for `AWS::Neptune::DBCluster` resources, the default deletion behavior is that the entire volume will be deleted without a snapshot\. To retain a backup of the volume, the `DeletionPolicy` should be set to `Snapshot`\. For more information about how AWS CloudFormation deletes resources, see [DeletionPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.

You can use `AWS::Neptune::DBCluster.DeletionProtection` to help guard against unintended deletion of your DB cluster\.

## Syntax<a name="aws-resource-neptune-dbcluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-neptune-dbcluster-syntax.json"></a>

```
{
  "Type" : "AWS::Neptune::DBCluster",
  "Properties" : {
      "[AssociatedRoles](#cfn-neptune-dbcluster-associatedroles)" : [ DBClusterRole, ... ],
      "[AvailabilityZones](#cfn-neptune-dbcluster-availabilityzones)" : [ String, ... ],
      "[BackupRetentionPeriod](#cfn-neptune-dbcluster-backupretentionperiod)" : Integer,
      "[DBClusterIdentifier](#cfn-neptune-dbcluster-dbclusteridentifier)" : String,
      "[DBClusterParameterGroupName](#cfn-neptune-dbcluster-dbclusterparametergroupname)" : String,
      "[DBSubnetGroupName](#cfn-neptune-dbcluster-dbsubnetgroupname)" : String,
      "[DeletionProtection](#cfn-neptune-dbcluster-deletionprotection)" : Boolean,
      "[EnableCloudwatchLogsExports](#cfn-neptune-dbcluster-enablecloudwatchlogsexports)" : [ String, ... ],
      "[EngineVersion](#cfn-neptune-dbcluster-engineversion)" : String,
      "[IamAuthEnabled](#cfn-neptune-dbcluster-iamauthenabled)" : Boolean,
      "[KmsKeyId](#cfn-neptune-dbcluster-kmskeyid)" : String,
      "[Port](#cfn-neptune-dbcluster-port)" : Integer,
      "[PreferredBackupWindow](#cfn-neptune-dbcluster-preferredbackupwindow)" : String,
      "[PreferredMaintenanceWindow](#cfn-neptune-dbcluster-preferredmaintenancewindow)" : String,
      "[RestoreToTime](#cfn-neptune-dbcluster-restoretotime)" : String,
      "[RestoreType](#cfn-neptune-dbcluster-restoretype)" : String,
      "[SnapshotIdentifier](#cfn-neptune-dbcluster-snapshotidentifier)" : String,
      "[SourceDBClusterIdentifier](#cfn-neptune-dbcluster-sourcedbclusteridentifier)" : String,
      "[StorageEncrypted](#cfn-neptune-dbcluster-storageencrypted)" : Boolean,
      "[Tags](#cfn-neptune-dbcluster-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UseLatestRestorableTime](#cfn-neptune-dbcluster-uselatestrestorabletime)" : Boolean,
      "[VpcSecurityGroupIds](#cfn-neptune-dbcluster-vpcsecuritygroupids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-neptune-dbcluster-syntax.yaml"></a>

```
Type: AWS::Neptune::DBCluster
Properties: 
  [AssociatedRoles](#cfn-neptune-dbcluster-associatedroles): 
    - DBClusterRole
  [AvailabilityZones](#cfn-neptune-dbcluster-availabilityzones): 
    - String
  [BackupRetentionPeriod](#cfn-neptune-dbcluster-backupretentionperiod): Integer
  [DBClusterIdentifier](#cfn-neptune-dbcluster-dbclusteridentifier): String
  [DBClusterParameterGroupName](#cfn-neptune-dbcluster-dbclusterparametergroupname): String
  [DBSubnetGroupName](#cfn-neptune-dbcluster-dbsubnetgroupname): String
  [DeletionProtection](#cfn-neptune-dbcluster-deletionprotection): Boolean
  [EnableCloudwatchLogsExports](#cfn-neptune-dbcluster-enablecloudwatchlogsexports): 
    - String
  [EngineVersion](#cfn-neptune-dbcluster-engineversion): String
  [IamAuthEnabled](#cfn-neptune-dbcluster-iamauthenabled): Boolean
  [KmsKeyId](#cfn-neptune-dbcluster-kmskeyid): String
  [Port](#cfn-neptune-dbcluster-port): Integer
  [PreferredBackupWindow](#cfn-neptune-dbcluster-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-neptune-dbcluster-preferredmaintenancewindow): String
  [RestoreToTime](#cfn-neptune-dbcluster-restoretotime): String
  [RestoreType](#cfn-neptune-dbcluster-restoretype): String
  [SnapshotIdentifier](#cfn-neptune-dbcluster-snapshotidentifier): String
  [SourceDBClusterIdentifier](#cfn-neptune-dbcluster-sourcedbclusteridentifier): String
  [StorageEncrypted](#cfn-neptune-dbcluster-storageencrypted): Boolean
  [Tags](#cfn-neptune-dbcluster-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UseLatestRestorableTime](#cfn-neptune-dbcluster-uselatestrestorabletime): Boolean
  [VpcSecurityGroupIds](#cfn-neptune-dbcluster-vpcsecuritygroupids): 
    - String
```

## Properties<a name="aws-resource-neptune-dbcluster-properties"></a>

`AssociatedRoles`  <a name="cfn-neptune-dbcluster-associatedroles"></a>
Provides a list of the AWS Identity and Access Management \(IAM\) roles that are associated with the DB cluster\. IAM roles that are associated with a DB cluster grant permission for the DB cluster to access other AWS services on your behalf\.  
*Required*: No  
*Type*: List of [DBClusterRole](aws-properties-neptune-dbcluster-dbclusterrole.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZones`  <a name="cfn-neptune-dbcluster-availabilityzones"></a>
Provides the list of EC2 Availability Zones that instances in the DB cluster can be created in\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BackupRetentionPeriod`  <a name="cfn-neptune-dbcluster-backupretentionperiod"></a>
Specifies the number of days for which automatic DB snapshots are retained\.  
An update may require some interruption\. See [ModifyDBInstance](https://docs.aws.amazon.com/neptune/latest/userguide/api-instances.html#ModifyDBInstance) in the Amazon Neptune User Guide for more information\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBClusterIdentifier`  <a name="cfn-neptune-dbcluster-dbclusteridentifier"></a>
Contains a user\-supplied DB cluster identifier\. This identifier is the unique key that identifies a DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBClusterParameterGroupName`  <a name="cfn-neptune-dbcluster-dbclusterparametergroupname"></a>
Provides the name of the DB cluster parameter group\.  
An update may require some interruption\. See [ModifyDBInstance](https://docs.aws.amazon.com/neptune/latest/userguide/api-instances.html#ModifyDBInstance) in the Amazon Neptune User Guide for more information\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBSubnetGroupName`  <a name="cfn-neptune-dbcluster-dbsubnetgroupname"></a>
Specifies information on the subnet group associated with the DB cluster, including the name, description, and subnets in the subnet group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeletionProtection`  <a name="cfn-neptune-dbcluster-deletionprotection"></a>
Indicates whether or not the DB cluster has deletion protection enabled\. The database can't be deleted when deletion protection is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableCloudwatchLogsExports`  <a name="cfn-neptune-dbcluster-enablecloudwatchlogsexports"></a>
Specifies a list of log types that are enabled for export to CloudWatch Logs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineVersion`  <a name="cfn-neptune-dbcluster-engineversion"></a>
Indicates the database engine version\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IamAuthEnabled`  <a name="cfn-neptune-dbcluster-iamauthenabled"></a>
True if mapping of AWS Identity and Access Management \(IAM\) accounts to database accounts is enabled, and otherwise false\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-neptune-dbcluster-kmskeyid"></a>
If `StorageEncrypted` is true, the AWS KMS key identifier for the encrypted DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-neptune-dbcluster-port"></a>
Specifies the port that the database engine is listening on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredBackupWindow`  <a name="cfn-neptune-dbcluster-preferredbackupwindow"></a>
Specifies the daily time range during which automated backups are created if automated backups are enabled, as determined by the `BackupRetentionPeriod`\.  
An update may require some interruption\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-neptune-dbcluster-preferredmaintenancewindow"></a>
Specifies the weekly time range during which system maintenance can occur, in Universal Coordinated Time \(UTC\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestoreToTime`  <a name="cfn-neptune-dbcluster-restoretotime"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RestoreType`  <a name="cfn-neptune-dbcluster-restoretype"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnapshotIdentifier`  <a name="cfn-neptune-dbcluster-snapshotidentifier"></a>
Specifies the identifier for a DB cluster snapshot\. Must match the identifier of an existing snapshot\.  
After you restore a DB cluster using a `SnapshotIdentifier`, you must specify the same `SnapshotIdentifier` for any future updates to the DB cluster\. When you specify this property for an update, the DB cluster is not restored from the snapshot again, and the data in the database is not changed\.  
However, if you don't specify the `SnapshotIdentifier`, an empty DB cluster is created, and the original DB cluster is deleted\. If you specify a property that is different from the previous snapshot restore property, the DB cluster is restored from the snapshot specified by the `SnapshotIdentifier`, and the original DB cluster is deleted\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceDBClusterIdentifier`  <a name="cfn-neptune-dbcluster-sourcedbclusteridentifier"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageEncrypted`  <a name="cfn-neptune-dbcluster-storageencrypted"></a>
Indicates whether the DB cluster is encrypted\.  
If you specify the `DBClusterIdentifier`, `DBSnapshotIdentifier`, or `SourceDBInstanceIdentifier` property, don't specify this property\. The value is inherited from the cluster, snapshot, or source DB instance\. If you specify the `KmsKeyId` property, you must enable encryption\.  
If you specify the `KmsKeyId`, you must enable encryption by setting `StorageEncrypted` to true\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-neptune-dbcluster-tags"></a>
The tags assigned to this cluster\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseLatestRestorableTime`  <a name="cfn-neptune-dbcluster-uselatestrestorabletime"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcSecurityGroupIds`  <a name="cfn-neptune-dbcluster-vpcsecuritygroupids"></a>
Provides a list of VPC security groups that the DB cluster belongs to\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-neptune-dbcluster-return-values"></a>

### Ref<a name="aws-resource-neptune-dbcluster-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-neptune-dbcluster-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-neptune-dbcluster-return-values-fn--getatt-fn--getatt"></a>

`ClusterResourceId`  <a name="ClusterResourceId-fn::getatt"></a>
The resource id for the DB cluster\. For example: `cluster-ABCD1234EFGH5678IJKL90MNOP`\. The cluster ID uniquely identifies the cluster and is used in things like IAM authentication policies\.

`Endpoint`  <a name="Endpoint-fn::getatt"></a>
The connection endpoint for the DB cluster\. For example: `mystack-mydbcluster-1apw1j4phylrk.cg034hpkmmjt.us-east-2.rds.amazonaws.com` 

`Port`  <a name="Port-fn::getatt"></a>
The port number on which the DB cluster accepts connections\. For example: `8182`\.

`ReadEndpoint`  <a name="ReadEndpoint-fn::getatt"></a>
The reader endpoint for the DB cluster\. For example: `mystack-mydbcluster-ro-1apw1j4phylrk.cg034hpkmmjt.us-east-2.rds.amazonaws.com` 