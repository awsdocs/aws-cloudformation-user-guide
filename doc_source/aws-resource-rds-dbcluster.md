# AWS::RDS::DBCluster<a name="aws-resource-rds-dbcluster"></a>

The `AWS::RDS::DBCluster` resource creates a cluster, such as an Aurora for Amazon RDS \(Amazon Aurora\) DB cluster\. Amazon Aurora is a fully managed, MySQL\-compatible, relational database engine\. For more information, see [Aurora on Amazon RDS](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Aurora.html) in the *Amazon Relational Database Service User Guide*\.

**Note**  
Currently, you can create this resource only in regions in which Amazon Aurora is supported\.

The default DeletionPolicy for `AWS::RDS::DBCluster` resources is `Snapshot`\. For more information about how AWS CloudFormation deletes resources, see \.


+ [Syntax](#aws-resource-rds-dbcluster-syntax)
+ [Properties](#w3ab2c21c10d875c13)
+ [Return Values](#aws-resource-rds-dbcluster-ref)
+ [Example](#w3ab2c21c10d875c17)

## Syntax<a name="aws-resource-rds-dbcluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbcluster-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBCluster",
  "Properties" :
  {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-availabilityzones)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-backuprententionperiod)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-databasename)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-dbclusterparametergroupname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-dbsubnetgroupname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-engine)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-engineversion)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-kmskeyid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-masterusername)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-masteruserpassword)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-port)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-preferredbackupwindow)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-preferredmaintenancewindow)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-replicationsourceidentifier)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-snapshotidentifier)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-storageencrypted)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-tags)" : [ Resource Tag, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-vpcsecuritygroupids)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-rds-dbcluster-syntax.yaml"></a>

```
Type: "AWS::RDS::DBCluster"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-availabilityzones):
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-backuprententionperiod): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-databasename): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-dbclusterparametergroupname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-dbsubnetgroupname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-engine): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-engineversion): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-kmskeyid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-masterusername): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-masteruserpassword): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-port): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-preferredbackupwindow): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-preferredmaintenancewindow): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-replicationsourceidentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-snapshotidentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-storageencrypted): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-tags):
    - Resource Tag
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbcluster-vpcsecuritygroupids):
    - String
```

## Properties<a name="w3ab2c21c10d875c13"></a>

`AvailabilityZones`  
A list of Availability Zones \(AZs\) in which DB instances in the cluster can be created\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`BackupRetentionPeriod`  
The number of days for which automatic backups are retained\. For more information, see [CreateDBCluster](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBCluster.html) in the *Amazon Relational Database Service API Reference*\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption or some interruptions\. For more information, see [ModifyDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html) in the *Amazon Relational Database Service API Reference*\.

`DatabaseName`  
The name of your database\. If you don't provide a name, Amazon Relational Database Service \(Amazon RDS\) won't create a database in this DB cluster\. For naming constraints, see [ Naming Constraints in Amazon RDS](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Limits.html#RDS_Limits.Constraints) in the *Amazon Relational Database Service User Guide*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`DBClusterParameterGroupName`  
The name of the DB cluster parameter group to associate with this DB cluster\. For the default value, see the `DBClusterParameterGroupName` parameter of the [CreateDBCluster](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBCluster.html) action in the *Amazon Relational Database Service API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: Some interruptions

`DBSubnetGroupName`  
A DB subnet group that you want to associate with this DB cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Engine`  
The name of the database engine that you want to use for this DB cluster\.  
For valid values, see the `Engine` parameter of the [CreateDBCluster](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBCluster.html) action in the *Amazon Relational Database Service API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`EngineVersion`  
The version number of the database engine that you want to use\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`KmsKeyId`  
The Amazon Resource Name \(ARN\) of the AWS Key Management Service master key that is used to encrypt the database instances in the DB cluster, such as `arn:aws:kms:us-east-1:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you enable the `StorageEncrypted` property but don't specify this property, the default master key is used\. If you specify this property, you must set the `StorageEncrypted` property to `true`\.  
If you specify the `SnapshotIdentifier`, do not specify this property\. The value is inherited from the snapshot DB cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement\.

`MasterUsername`  
The master user name for the DB instance\.  
*Required: *Conditional\. You must specify this property unless you specify the `SnapshotIdentifier` property\. In that case, do not specify this property\.  
*Type*: String  
*Update requires*: Replacement\.

`MasterUserPassword`  
The password for the master database user\.  
*Required: *Conditional\. You must specify this property unless you specify the `SnapshotIdentifier` property\. In that case, do not specify this property\.  
*Type*: String  
*Update requires*: No interruption

`Port`  
The port number on which the DB instances in the cluster can accept connections\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`PreferredBackupWindow`  
if automated backups are enabled \(see the `BackupRetentionPeriod` property\), the daily time range in UTC during which you want to create automated backups\.  
For valid values, see the `PreferredBackupWindow` parameter of the [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) action in the *Amazon Relational Database Service API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`PreferredMaintenanceWindow`  
The weekly time range \(in UTC\) during which system maintenance can occur\.  
For valid values, see the `PreferredMaintenanceWindow` parameter of the [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html) action in the *Amazon Relational Database Service API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption or some interruptions\. For more information, see [ModifyDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html) in the *Amazon Relational Database Service API Reference*\.

`ReplicationSourceIdentifier`  
The Amazon Resource Name \(ARN\) of the source Amazon RDS MySQL DB instance or DB cluster, if this DB cluster is created as a Read Replica\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`SnapshotIdentifier`  
The identifier for the DB cluster snapshot from which you want to restore\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`StorageEncrypted`  
Indicates whether the DB instances in the cluster are encrypted\.  
If you specify the `SnapshotIdentifier` property, do not specify this property\. The value is inherited from the snapshot DB cluster\.  
*Required: *Conditional\. If you specify the `KmsKeyId` property, you must enable encryption\.  
*Type*: Boolean  
*Update requires*: Replacement\.

`Tags`  
The tags that you want to attach to this DB cluster\.  
*Required: *No  
*Type*: A list of resource tags  
*Update requires*: No interruption

`VpcSecurityGroupIds`  
A list of VPC security groups to associate with this DB cluster\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

## Return Values<a name="aws-resource-rds-dbcluster-ref"></a>

### Ref<a name="w3ab2c21c10d875c15b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d875c15b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Endpoint.Address`  
The connection endpoint for the DB cluster\. For example: `mystack-mydbcluster-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`\.

`Endpoint.Port`  
The port number on which the Amazon Redshift cluster accepts connections\. For example: `5439`\.

`ReadEndpoint.Address`  
The reader endpoint for the DB cluster\. For example: `mystack-mydbcluster-ro-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Example<a name="w3ab2c21c10d875c17"></a>

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