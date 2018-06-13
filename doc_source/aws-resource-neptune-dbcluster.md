# AWS::Neptune::DBCluster<a name="aws-resource-neptune-dbcluster"></a>

The `AWS::Neptune::DBCluster` resource creates a Amazon Neptune DB Cluster\. Neptune is a fully managed graph database\. \.

**Note**  
Currently, you can create this resource only in regions in which Amazon Neptune is supported\.

The default DeletionPolicy for `AWS::Neptune::DBCluster` resources is `Snapshot`\. For more information about how AWS CloudFormation deletes resources, see [DeletionPolicy Attribute](aws-attribute-deletionpolicy.md)\.

**Topics**
+ [Syntax](#aws-resource-neptune-dbcluster-syntax)
+ [Properties](#w3ab2c21c10d888c15)
+ [Return Values](#aws-resource-neptune-dbcluster-ref)

## Syntax<a name="aws-resource-neptune-dbcluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-neptune-dbcluster-syntax.json"></a>

```
{
  "Type" : "AWS::Neptune::DBCluster",
  "Properties" :
  {
    "[AvailabilityZones](#cfn-neptune-dbcluster-availabilityzones)" : [ String, ... ],
    "[BackupRetentionPeriod](#cfn-neptune-dbcluster-backuprententionperiod)" : Integer,
    "[DBClusterIdentifier](#cfn-neptune-dbcluster-dbclusteridentifier)" : String,
    "[DBClusterParameterGroupName](#cfn-neptune-dbcluster-dbclusterparametergroupname)" : String,
    "[DBSubnetGroupName](#cfn-neptune-dbcluster-dbsubnetgroupname)" : String,
    "[IamAuthEnabled](#cfn-neptune-dbcluster-iamauthenabled)" : Boolean,
    "[KmsKeyId](#cfn-neptune-dbcluster-kmskeyid)" : String,
    "[Port](#cfn-neptune-dbcluster-port)" : Integer,
    "[PreferredBackupWindow](#cfn-neptune-dbcluster-preferredbackupwindow)" : String,
    "[PreferredMaintenanceWindow](#cfn-neptune-dbcluster-preferredmaintenancewindow)" : String,
    "[SnapshotIdentifier](#cfn-neptune-dbcluster-snapshotidentifier)" : String,
    "[StorageEncrypted](#cfn-neptune-dbcluster-storageencrypted)" : Boolean,
    "[Tags](#cfn-neptune-dbcluster-tags)" : [ Resource Tag, ... ],
    "[VpcSecurityGroupIds](#cfn-neptune-dbcluster-vpcsecuritygroupids)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-neptune-dbcluster-syntax.yaml"></a>

```
Type: "AWS::Neptune::DBCluster"
Properties:
  [AvailabilityZones](#cfn-neptune-dbcluster-availabilityzones):
    - String
  [BackupRetentionPeriod](#cfn-neptune-dbcluster-backuprententionperiod): Integer
  [DBClusterIdentifier](#cfn-neptune-dbcluster-dbclusteridentifier): String
  [DBClusterParameterGroupName](#cfn-neptune-dbcluster-dbclusterparametergroupname): String
  [DBSubnetGroupName](#cfn-neptune-dbcluster-dbsubnetgroupname): String
  [IamAuthEnabled](#cfn-neptune-dbcluster-iamauthenabled): Boolean
  [KmsKeyId](#cfn-neptune-dbcluster-kmskeyid): String
  [Port](#cfn-neptune-dbcluster-port): Integer
  [PreferredBackupWindow](#cfn-neptune-dbcluster-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-neptune-dbcluster-preferredmaintenancewindow): String
  [SnapshotIdentifier](#cfn-neptune-dbcluster-snapshotidentifier): String
  [StorageEncrypted](#cfn-neptune-dbcluster-storageencrypted): Boolean
  [Tags](#cfn-neptune-dbcluster-tags):
    - Resource Tag
  [VpcSecurityGroupIds](#cfn-neptune-dbcluster-vpcsecuritygroupids):
    - String
```

## Properties<a name="w3ab2c21c10d888c15"></a>

`AvailabilityZones`  <a name="cfn-neptune-dbcluster-availabilityzones"></a>
A list of Availability Zones \(AZs\) in which DB instances in the cluster can be created\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`BackupRetentionPeriod`  <a name="cfn-neptune-dbcluster-backuprententionperiod"></a>
The number of days for which automatic backups are retained\. For more information, see [CreateDBCluster](docs.aws.amazon.com/neptune/latest/userguide/API_CreateDBCluster.html)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. For more information, see [ModifyDBInstance](docs.aws.amazon.com/neptune/latest/userguide/API_ModifyDBInstance.html)\.

`DBClusterIdentifier`  <a name="cfn-neptune-dbcluster-dbclusteridentifier"></a>
The DB cluster identifier\. This parameter is stored as a lowercase string\.   
Constraints:  
+ Must contain from 1 to 63 letters, numbers, or hyphens\.
+ First character must be a letter\.
+ Cannot end with a hyphen or contain two consecutive hyphens\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBClusterParameterGroupName`  <a name="cfn-neptune-dbcluster-dbclusterparametergroupname"></a>
The name of the DB cluster parameter group to associate with this DB cluster\.   
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`DBSubnetGroupName`  <a name="cfn-neptune-dbcluster-dbsubnetgroupname"></a>
A DB subnet group that you want to associate with this DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`IamAuthEnabled`  <a name="cfn-neptune-dbcluster-iamauthenabled"></a>
Enable IAM authentication and authoriation on this cluster\.  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KmsKeyId`  <a name="cfn-neptune-dbcluster-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of the AWS Key Management Service master key that is used to encrypt the database instances in the DB cluster, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the `StorageEncrypted` property but don't specify this property, the default master key is used\. If you specify this property, you must set the `StorageEncrypted` property to `true`\.  
If you specify the `SnapshotIdentifier`, do not specify this property\. The value is inherited from the snapshot DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`Port`  <a name="cfn-neptune-dbcluster-port"></a>
The port number on which the DB instances in the cluster can accept connections\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PreferredBackupWindow`  <a name="cfn-neptune-dbcluster-preferredbackupwindow"></a>
if automated backups are enabled \(see the `BackupRetentionPeriod` property\), the daily time range in UTC during which you want to create automated backups\.  
For valid values, see the `PreferredBackupWindow` parameter of the [CreateDBInstance](docs.aws.amazon.com/neptune/latest/userguide/API_CreateDBInstance.html) action\.\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-neptune-dbcluster-preferredmaintenancewindow"></a>
The weekly time range \(in UTC\) during which system maintenance can occur\.  
For valid values, see the `PreferredMaintenanceWindow` parameter of the [CreateDBInstance](docs.aws.amazon.com/neptune/latest/userguide/API_CreateDBInstance.html) action\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. For more information, see [ModifyDBInstance](docs.aws.amazon.com/neptune/latest/userguide/API_ModifyDBInstance.html)\.

`SnapshotIdentifier`  <a name="cfn-neptune-dbcluster-snapshotidentifier"></a>
The identifier for the DB cluster snapshot from which you want to restore\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`StorageEncrypted`  <a name="cfn-neptune-dbcluster-storageencrypted"></a>
Indicates whether the DB instances in the cluster are encrypted\.  
If you specify the `SnapshotIdentifier` property, do not specify this property\. The value is inherited from the snapshot DB cluster\.  
*Required*: Conditional\. If you specify the `KmsKeyId` property, you must enable encryption\.  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`Tags`  <a name="cfn-neptune-dbcluster-tags"></a>
The tags that you want to attach to this DB cluster\.  
*Required*: No  
*Type*: A list of [resource tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-neptune-dbcluster-vpcsecuritygroupids"></a>
A list of VPC security groups to associate with this DB cluster\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-neptune-dbcluster-ref"></a>

### Ref<a name="w3ab2c21c10d888c17b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d888c17b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Endpoint`  
The connection endpoint for the DB cluster\. For example: `mystack-mydbcluster-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`\.

`Port`  
The port number on which the DB cluster accepts connections\. For example: `8182`\.

`ReadEndpoint`  
The reader endpoint for the DB cluster\. For example: `mystack-mydbcluster-ro-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`\.

`ClusterResouceId`  
The resource id for the DB cluster\. For example: `cluster-ABCD1234EFGH5678IJKL90MNOP`\. The cluster ID uniquely identifies the cluster and is used in things like IAM authentication policies\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.