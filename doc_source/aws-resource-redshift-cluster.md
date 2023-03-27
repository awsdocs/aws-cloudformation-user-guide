# AWS::Redshift::Cluster<a name="aws-resource-redshift-cluster"></a>

Specifies a cluster\. A *cluster* is a fully managed data warehouse that consists of a set of compute nodes\.

To create a cluster in Virtual Private Cloud \(VPC\), you must provide a cluster subnet group name\. The cluster subnet group identifies the subnets of your VPC that Amazon Redshift uses when creating the cluster\. For more information about managing clusters, go to [Amazon Redshift Clusters](https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-clusters.html) in the *Amazon Redshift Cluster Management Guide*\.

## Syntax<a name="aws-resource-redshift-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::Cluster",
  "Properties" : {
      "[AllowVersionUpgrade](#cfn-redshift-cluster-allowversionupgrade)" : Boolean,
      "[AquaConfigurationStatus](#cfn-redshift-cluster-aquaconfigurationstatus)" : String,
      "[AutomatedSnapshotRetentionPeriod](#cfn-redshift-cluster-automatedsnapshotretentionperiod)" : Integer,
      "[AvailabilityZone](#cfn-redshift-cluster-availabilityzone)" : String,
      "[AvailabilityZoneRelocation](#cfn-redshift-cluster-availabilityzonerelocation)" : Boolean,
      "[AvailabilityZoneRelocationStatus](#cfn-redshift-cluster-availabilityzonerelocationstatus)" : String,
      "[Classic](#cfn-redshift-cluster-classic)" : Boolean,
      "[ClusterIdentifier](#cfn-redshift-cluster-clusteridentifier)" : String,
      "[ClusterParameterGroupName](#cfn-redshift-cluster-clusterparametergroupname)" : String,
      "[ClusterSecurityGroups](#cfn-redshift-cluster-clustersecuritygroups)" : [ String, ... ],
      "[ClusterSubnetGroupName](#cfn-redshift-cluster-clustersubnetgroupname)" : String,
      "[ClusterType](#cfn-redshift-cluster-clustertype)" : String,
      "[ClusterVersion](#cfn-redshift-cluster-clusterversion)" : String,
      "[DBName](#cfn-redshift-cluster-dbname)" : String,
      "[DeferMaintenance](#cfn-redshift-cluster-defermaintenance)" : Boolean,
      "[DeferMaintenanceDuration](#cfn-redshift-cluster-defermaintenanceduration)" : Integer,
      "[DeferMaintenanceEndTime](#cfn-redshift-cluster-defermaintenanceendtime)" : String,
      "[DeferMaintenanceStartTime](#cfn-redshift-cluster-defermaintenancestarttime)" : String,
      "[DestinationRegion](#cfn-redshift-cluster-destinationregion)" : String,
      "[ElasticIp](#cfn-redshift-cluster-elasticip)" : String,
      "[Encrypted](#cfn-redshift-cluster-encrypted)" : Boolean,
      "[Endpoint](#cfn-redshift-cluster-endpoint)" : Endpoint,
      "[EnhancedVpcRouting](#cfn-redshift-cluster-enhancedvpcrouting)" : Boolean,
      "[HsmClientCertificateIdentifier](#cfn-redshift-cluster-hsmclientcertificateidentifier)" : String,
      "[HsmConfigurationIdentifier](#cfn-redshift-cluster-hsmconfigurationidentifier)" : String,
      "[IamRoles](#cfn-redshift-cluster-iamroles)" : [ String, ... ],
      "[KmsKeyId](#cfn-redshift-cluster-kmskeyid)" : String,
      "[LoggingProperties](#cfn-redshift-cluster-loggingproperties)" : LoggingProperties,
      "[MaintenanceTrackName](#cfn-redshift-cluster-maintenancetrackname)" : String,
      "[ManualSnapshotRetentionPeriod](#cfn-redshift-cluster-manualsnapshotretentionperiod)" : Integer,
      "[MasterUsername](#cfn-redshift-cluster-masterusername)" : String,
      "[MasterUserPassword](#cfn-redshift-cluster-masteruserpassword)" : String,
      "[NodeType](#cfn-redshift-cluster-nodetype)" : String,
      "[NumberOfNodes](#cfn-redshift-cluster-numberofnodes)" : Integer,
      "[OwnerAccount](#cfn-redshift-cluster-owneraccount)" : String,
      "[Port](#cfn-redshift-cluster-port)" : Integer,
      "[PreferredMaintenanceWindow](#cfn-redshift-cluster-preferredmaintenancewindow)" : String,
      "[PubliclyAccessible](#cfn-redshift-cluster-publiclyaccessible)" : Boolean,
      "[ResourceAction](#cfn-redshift-cluster-resourceaction)" : String,
      "[RevisionTarget](#cfn-redshift-cluster-revisiontarget)" : String,
      "[RotateEncryptionKey](#cfn-redshift-cluster-rotateencryptionkey)" : Boolean,
      "[SnapshotClusterIdentifier](#cfn-redshift-cluster-snapshotclusteridentifier)" : String,
      "[SnapshotCopyGrantName](#cfn-redshift-cluster-snapshotcopygrantname)" : String,
      "[SnapshotCopyManual](#cfn-redshift-cluster-snapshotcopymanual)" : Boolean,
      "[SnapshotCopyRetentionPeriod](#cfn-redshift-cluster-snapshotcopyretentionperiod)" : Integer,
      "[SnapshotIdentifier](#cfn-redshift-cluster-snapshotidentifier)" : String,
      "[Tags](#cfn-redshift-cluster-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcSecurityGroupIds](#cfn-redshift-cluster-vpcsecuritygroupids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-redshift-cluster-syntax.yaml"></a>

```
Type: AWS::Redshift::Cluster
Properties: 
  [AllowVersionUpgrade](#cfn-redshift-cluster-allowversionupgrade): Boolean
  [AquaConfigurationStatus](#cfn-redshift-cluster-aquaconfigurationstatus): String
  [AutomatedSnapshotRetentionPeriod](#cfn-redshift-cluster-automatedsnapshotretentionperiod): Integer
  [AvailabilityZone](#cfn-redshift-cluster-availabilityzone): String
  [AvailabilityZoneRelocation](#cfn-redshift-cluster-availabilityzonerelocation): Boolean
  [AvailabilityZoneRelocationStatus](#cfn-redshift-cluster-availabilityzonerelocationstatus): String
  [Classic](#cfn-redshift-cluster-classic): Boolean
  [ClusterIdentifier](#cfn-redshift-cluster-clusteridentifier): String
  [ClusterParameterGroupName](#cfn-redshift-cluster-clusterparametergroupname): String
  [ClusterSecurityGroups](#cfn-redshift-cluster-clustersecuritygroups): 
    - String
  [ClusterSubnetGroupName](#cfn-redshift-cluster-clustersubnetgroupname): String
  [ClusterType](#cfn-redshift-cluster-clustertype): String
  [ClusterVersion](#cfn-redshift-cluster-clusterversion): String
  [DBName](#cfn-redshift-cluster-dbname): String
  [DeferMaintenance](#cfn-redshift-cluster-defermaintenance): Boolean
  [DeferMaintenanceDuration](#cfn-redshift-cluster-defermaintenanceduration): Integer
  [DeferMaintenanceEndTime](#cfn-redshift-cluster-defermaintenanceendtime): String
  [DeferMaintenanceStartTime](#cfn-redshift-cluster-defermaintenancestarttime): String
  [DestinationRegion](#cfn-redshift-cluster-destinationregion): String
  [ElasticIp](#cfn-redshift-cluster-elasticip): String
  [Encrypted](#cfn-redshift-cluster-encrypted): Boolean
  [Endpoint](#cfn-redshift-cluster-endpoint): 
    Endpoint
  [EnhancedVpcRouting](#cfn-redshift-cluster-enhancedvpcrouting): Boolean
  [HsmClientCertificateIdentifier](#cfn-redshift-cluster-hsmclientcertificateidentifier): String
  [HsmConfigurationIdentifier](#cfn-redshift-cluster-hsmconfigurationidentifier): String
  [IamRoles](#cfn-redshift-cluster-iamroles): 
    - String
  [KmsKeyId](#cfn-redshift-cluster-kmskeyid): String
  [LoggingProperties](#cfn-redshift-cluster-loggingproperties): 
    LoggingProperties
  [MaintenanceTrackName](#cfn-redshift-cluster-maintenancetrackname): String
  [ManualSnapshotRetentionPeriod](#cfn-redshift-cluster-manualsnapshotretentionperiod): Integer
  [MasterUsername](#cfn-redshift-cluster-masterusername): String
  [MasterUserPassword](#cfn-redshift-cluster-masteruserpassword): String
  [NodeType](#cfn-redshift-cluster-nodetype): String
  [NumberOfNodes](#cfn-redshift-cluster-numberofnodes): Integer
  [OwnerAccount](#cfn-redshift-cluster-owneraccount): String
  [Port](#cfn-redshift-cluster-port): Integer
  [PreferredMaintenanceWindow](#cfn-redshift-cluster-preferredmaintenancewindow): String
  [PubliclyAccessible](#cfn-redshift-cluster-publiclyaccessible): Boolean
  [ResourceAction](#cfn-redshift-cluster-resourceaction): String
  [RevisionTarget](#cfn-redshift-cluster-revisiontarget): String
  [RotateEncryptionKey](#cfn-redshift-cluster-rotateencryptionkey): Boolean
  [SnapshotClusterIdentifier](#cfn-redshift-cluster-snapshotclusteridentifier): String
  [SnapshotCopyGrantName](#cfn-redshift-cluster-snapshotcopygrantname): String
  [SnapshotCopyManual](#cfn-redshift-cluster-snapshotcopymanual): Boolean
  [SnapshotCopyRetentionPeriod](#cfn-redshift-cluster-snapshotcopyretentionperiod): Integer
  [SnapshotIdentifier](#cfn-redshift-cluster-snapshotidentifier): String
  [Tags](#cfn-redshift-cluster-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcSecurityGroupIds](#cfn-redshift-cluster-vpcsecuritygroupids): 
    - String
```

## Properties<a name="aws-resource-redshift-cluster-properties"></a>

`AllowVersionUpgrade`  <a name="cfn-redshift-cluster-allowversionupgrade"></a>
If `true`, major version upgrades can be applied during the maintenance window to the Amazon Redshift engine that is running on the cluster\.  
When a new major version of the Amazon Redshift engine is released, you can request that the service automatically apply upgrades during the maintenance window to the Amazon Redshift engine that is running on your cluster\.  
Default: `true`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AquaConfigurationStatus`  <a name="cfn-redshift-cluster-aquaconfigurationstatus"></a>
This parameter is retired\. It does not set the AQUA configuration status\. Amazon Redshift automatically determines whether to use AQUA \(Advanced Query Accelerator\)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `auto | disabled | enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutomatedSnapshotRetentionPeriod`  <a name="cfn-redshift-cluster-automatedsnapshotretentionperiod"></a>
The number of days that automated snapshots are retained\. If the value is 0, automated snapshots are disabled\. Even if automated snapshots are disabled, you can still create manual snapshots when you want with [CreateClusterSnapshot](https://docs.aws.amazon.com/redshift/latest/APIReference/API_CreateClusterSnapshot.html) in the *Amazon Redshift API Reference*\.   
Default: `1`   
Constraints: Must be a value from 0 to 35\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-redshift-cluster-availabilityzone"></a>
The EC2 Availability Zone \(AZ\) in which you want Amazon Redshift to provision the cluster\. For example, if you have several EC2 instances running in a specific Availability Zone, then you might want the cluster to be provisioned in the same zone in order to decrease network latency\.  
Default: A random, system\-chosen Availability Zone in the region that is specified by the endpoint\.  
Example: `us-east-2d`   
Constraint: The specified Availability Zone must be in the same region as the current endpoint\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZoneRelocation`  <a name="cfn-redshift-cluster-availabilityzonerelocation"></a>
The option to enable relocation for an Amazon Redshift cluster between Availability Zones after the cluster is created\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZoneRelocationStatus`  <a name="cfn-redshift-cluster-availabilityzonerelocationstatus"></a>
Describes the status of the Availability Zone relocation operation\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Classic`  <a name="cfn-redshift-cluster-classic"></a>
A boolean value indicating whether the resize operation is using the classic resize process\. If you don't provide this parameter or set the value to `false`, the resize type is elastic\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterIdentifier`  <a name="cfn-redshift-cluster-clusteridentifier"></a>
A unique identifier for the cluster\. You use this identifier to refer to the cluster for any subsequent cluster operations such as deleting or modifying\. The identifier also appears in the Amazon Redshift console\.  
Constraints:  
+ Must contain from 1 to 63 alphanumeric characters or hyphens\.
+ Alphabetic characters must be lowercase\.
+ First character must be a letter\.
+ Cannot end with a hyphen or contain two consecutive hyphens\.
+ Must be unique for all clusters within an AWS account\.
Example: `myexamplecluster`   
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterParameterGroupName`  <a name="cfn-redshift-cluster-clusterparametergroupname"></a>
The name of the parameter group to be associated with this cluster\.  
Default: The default Amazon Redshift cluster parameter group\. For information about the default parameter group, go to [Working with Amazon Redshift Parameter Groups](https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-parameter-groups.html)   
Constraints:  
+ Must be 1 to 255 alphanumeric characters or hyphens\.
+ First character must be a letter\.
+ Cannot end with a hyphen or contain two consecutive hyphens\.
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterSecurityGroups`  <a name="cfn-redshift-cluster-clustersecuritygroups"></a>
A list of security groups to be associated with this cluster\.  
Default: The default cluster security group for Amazon Redshift\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterSubnetGroupName`  <a name="cfn-redshift-cluster-clustersubnetgroupname"></a>
The name of a cluster subnet group to be associated with this cluster\.  
If this parameter is not provided the resulting cluster will be deployed outside virtual private cloud \(VPC\)\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterType`  <a name="cfn-redshift-cluster-clustertype"></a>
The type of the cluster\. When cluster type is specified as  
+  `single-node`, the **NumberOfNodes** parameter is not required\.
+  `multi-node`, the **NumberOfNodes** parameter is required\.
Valid Values: `multi-node` \| `single-node`   
Default: `multi-node`   
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterVersion`  <a name="cfn-redshift-cluster-clusterversion"></a>
The version of the Amazon Redshift engine software that you want to deploy on the cluster\.  
The version selected runs on all the nodes in the cluster\.  
Constraints: Only version 1\.0 is currently available\.  
Example: `1.0`   
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBName`  <a name="cfn-redshift-cluster-dbname"></a>
The name of the first database to be created when the cluster is created\.  
To create additional databases after the cluster is created, connect to the cluster with a SQL client and use SQL commands to create a database\. For more information, go to [Create a Database](https://docs.aws.amazon.com/redshift/latest/dg/t_creating_database.html) in the Amazon Redshift Database Developer Guide\.   
Default: `dev`   
Constraints:  
+ Must contain 1 to 64 alphanumeric characters\.
+ Must contain only lowercase letters\.
+ Cannot be a word that is reserved by the service\. A list of reserved words can be found in [Reserved Words](https://docs.aws.amazon.com/redshift/latest/dg/r_pg_keywords.html) in the Amazon Redshift Database Developer Guide\. 
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeferMaintenance`  <a name="cfn-redshift-cluster-defermaintenance"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeferMaintenanceDuration`  <a name="cfn-redshift-cluster-defermaintenanceduration"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeferMaintenanceEndTime`  <a name="cfn-redshift-cluster-defermaintenanceendtime"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeferMaintenanceStartTime`  <a name="cfn-redshift-cluster-defermaintenancestarttime"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationRegion`  <a name="cfn-redshift-cluster-destinationregion"></a>
The destination region that snapshots are automatically copied to when cross\-region snapshot copy is enabled\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElasticIp`  <a name="cfn-redshift-cluster-elasticip"></a>
The Elastic IP \(EIP\) address for the cluster\.  
Constraints: The cluster must be provisioned in EC2\-VPC and publicly\-accessible through an Internet gateway\. Don't specify the Elastic IP address for a publicly accessible cluster with availability zone relocation turned on\. For more information about provisioning clusters in EC2\-VPC, go to [Supported Platforms to Launch Your Cluster](https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-clusters.html#cluster-platforms) in the Amazon Redshift Cluster Management Guide\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-redshift-cluster-encrypted"></a>
If `true`, the data in the cluster is encrypted at rest\.   
Default: false  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Endpoint`  <a name="cfn-redshift-cluster-endpoint"></a>
The connection endpoint\.  
*Required*: No  
*Type*: [Endpoint](aws-properties-redshift-cluster-endpoint.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnhancedVpcRouting`  <a name="cfn-redshift-cluster-enhancedvpcrouting"></a>
An option that specifies whether to create the cluster with enhanced VPC routing enabled\. To create a cluster that uses enhanced VPC routing, the cluster must be in a VPC\. For more information, see [Enhanced VPC Routing](https://docs.aws.amazon.com/redshift/latest/mgmt/enhanced-vpc-routing.html) in the Amazon Redshift Cluster Management Guide\.  
If this option is `true`, enhanced VPC routing is enabled\.   
Default: false  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HsmClientCertificateIdentifier`  <a name="cfn-redshift-cluster-hsmclientcertificateidentifier"></a>
Specifies the name of the HSM client certificate the Amazon Redshift cluster uses to retrieve the data encryption keys stored in an HSM\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HsmConfigurationIdentifier`  <a name="cfn-redshift-cluster-hsmconfigurationidentifier"></a>
Specifies the name of the HSM configuration that contains the information the Amazon Redshift cluster can use to retrieve and store keys in an HSM\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamRoles`  <a name="cfn-redshift-cluster-iamroles"></a>
A list of AWS Identity and Access Management \(IAM\) roles that can be used by the cluster to access other AWS services\. You must supply the IAM roles in their Amazon Resource Name \(ARN\) format\.   
The maximum number of IAM roles that you can associate is subject to a quota\. For more information, go to [Quotas and limits](https://docs.aws.amazon.com/redshift/latest/mgmt/amazon-redshift-limits.html) in the *Amazon Redshift Cluster Management Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-redshift-cluster-kmskeyid"></a>
The AWS Key Management Service \(KMS\) key ID of the encryption key that you want to use to encrypt data in the cluster\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingProperties`  <a name="cfn-redshift-cluster-loggingproperties"></a>
Specifies logging information, such as queries and connection attempts, for the specified Amazon Redshift cluster\.  
*Required*: No  
*Type*: [LoggingProperties](aws-properties-redshift-cluster-loggingproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaintenanceTrackName`  <a name="cfn-redshift-cluster-maintenancetrackname"></a>
An optional parameter for the name of the maintenance track for the cluster\. If you don't provide a maintenance track name, the cluster is assigned to the `current` track\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManualSnapshotRetentionPeriod`  <a name="cfn-redshift-cluster-manualsnapshotretentionperiod"></a>
The default number of days to retain a manual snapshot\. If the value is \-1, the snapshot is retained indefinitely\. This setting doesn't change the retention period of existing snapshots\.  
The value must be either \-1 or an integer between 1 and 3,653\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUsername`  <a name="cfn-redshift-cluster-masterusername"></a>
The user name associated with the admin user for the cluster that is being created\.  
Constraints:  
+ Must be 1 \- 128 alphanumeric characters or hyphens\. The user name can't be `PUBLIC`\.
+ Must contain only lowercase letters, numbers, underscore, plus sign, period \(dot\), at symbol \(@\), or hyphen\.
+ The first character must be a letter\.
+ Must not contain a colon \(:\) or a slash \(/\)\.
+ Cannot be a reserved word\. A list of reserved words can be found in [Reserved Words](https://docs.aws.amazon.com/redshift/latest/dg/r_pg_keywords.html) in the Amazon Redshift Database Developer Guide\. 
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUserPassword`  <a name="cfn-redshift-cluster-masteruserpassword"></a>
The password associated with the admin user for the cluster that is being created\.  
Constraints:  
+ Must be between 8 and 64 characters in length\.
+ Must contain at least one uppercase letter\.
+ Must contain at least one lowercase letter\.
+ Must contain one number\.
+ Can be any printable ASCII character \(ASCII code 33\-126\) except `'` \(single quote\), `"` \(double quote\), `\`, `/`, or `@`\.
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NodeType`  <a name="cfn-redshift-cluster-nodetype"></a>
The node type to be provisioned for the cluster\. For information about node types, go to [ Working with Clusters](https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-clusters.html#how-many-nodes) in the *Amazon Redshift Cluster Management Guide*\.   
Valid Values: `ds2.xlarge` \| `ds2.8xlarge` \| `dc1.large` \| `dc1.8xlarge` \| `dc2.large` \| `dc2.8xlarge` \| `ra3.xlplus` \| `ra3.4xlarge` \| `ra3.16xlarge`   
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfNodes`  <a name="cfn-redshift-cluster-numberofnodes"></a>
The number of compute nodes in the cluster\. This parameter is required when the **ClusterType** parameter is specified as `multi-node`\.   
For information about determining how many nodes you need, go to [ Working with Clusters](https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-clusters.html#how-many-nodes) in the *Amazon Redshift Cluster Management Guide*\.   
If you don't specify this parameter, you get a single\-node cluster\. When requesting a multi\-node cluster, you must specify the number of nodes that you want in the cluster\.  
Default: `1`   
Constraints: Value must be at least 1 and no more than 100\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OwnerAccount`  <a name="cfn-redshift-cluster-owneraccount"></a>
The AWS account used to create or copy the snapshot\. Required if you are restoring a snapshot you do not own, optional if you own the snapshot\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-redshift-cluster-port"></a>
The port number on which the cluster accepts incoming connections\.  
The cluster is accessible only via the JDBC and ODBC connection strings\. Part of the connection string requires the port on which the cluster will listen for incoming connections\.  
Default: `5439`   
Valid Values: `1150-65535`   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-redshift-cluster-preferredmaintenancewindow"></a>
The weekly time range \(in UTC\) during which automated cluster maintenance can occur\.  
 Format: `ddd:hh24:mi-ddd:hh24:mi`   
 Default: A 30\-minute window selected at random from an 8\-hour block of time per region, occurring on a random day of the week\. For more information about the time blocks for each region, see [Maintenance Windows](https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-clusters.html#rs-maintenance-windows) in Amazon Redshift Cluster Management Guide\.  
Valid Days: Mon \| Tue \| Wed \| Thu \| Fri \| Sat \| Sun  
Constraints: Minimum 30\-minute window\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PubliclyAccessible`  <a name="cfn-redshift-cluster-publiclyaccessible"></a>
If `true`, the cluster can be accessed from a public network\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceAction`  <a name="cfn-redshift-cluster-resourceaction"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RevisionTarget`  <a name="cfn-redshift-cluster-revisiontarget"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotateEncryptionKey`  <a name="cfn-redshift-cluster-rotateencryptionkey"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotClusterIdentifier`  <a name="cfn-redshift-cluster-snapshotclusteridentifier"></a>
The name of the cluster the source snapshot was created from\. This parameter is required if your user or role has a policy containing a snapshot resource element that specifies anything other than \* for the cluster name\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnapshotCopyGrantName`  <a name="cfn-redshift-cluster-snapshotcopygrantname"></a>
The name of the snapshot copy grant\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotCopyManual`  <a name="cfn-redshift-cluster-snapshotcopymanual"></a>
Indicates whether to apply the snapshot retention period to newly copied manual snapshots instead of automated snapshots\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotCopyRetentionPeriod`  <a name="cfn-redshift-cluster-snapshotcopyretentionperiod"></a>
The number of days to retain automated snapshots in the destination AWS Region after they are copied from the source AWS Region\.  
By default, this only changes the retention period of copied automated snapshots\.   
If you decrease the retention period for automated snapshots that are copied to a destination AWS Region, Amazon Redshift deletes any existing automated snapshots that were copied to the destination AWS Region and that fall outside of the new retention period\.  
Constraints: Must be at least 1 and no more than 35 for automated snapshots\.   
If you specify the `manual` option, only newly copied manual snapshots will have the new retention period\.   
If you specify the value of \-1 newly copied manual snapshots are retained indefinitely\.  
Constraints: The number of days must be either \-1 or an integer between 1 and 3,653 for manual snapshots\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotIdentifier`  <a name="cfn-redshift-cluster-snapshotidentifier"></a>
The name of the snapshot from which to create the new cluster\. This parameter isn't case sensitive\. You must specify this parameter or `snapshotArn`, but not both\.  
Example: `my-snapshot-id`   
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-redshift-cluster-tags"></a>
A list of tag instances\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-redshift-cluster-vpcsecuritygroupids"></a>
A list of Virtual Private Cloud \(VPC\) security groups to be associated with the cluster\.  
Default: The default VPC security group is associated with the cluster\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-redshift-cluster-return-values"></a>

### Ref<a name="aws-resource-redshift-cluster-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myCluster" }` 

For the Amazon Redshift cluster `myCluster`, `Ref` returns the name of the cluster\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-redshift-cluster-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-redshift-cluster-return-values-fn--getatt-fn--getatt"></a>

`DeferMaintenanceIdentifier`  <a name="DeferMaintenanceIdentifier-fn::getatt"></a>
Property description not available\.

`Endpoint.Address`  <a name="Endpoint.Address-fn::getatt"></a>
The connection endpoint for the Amazon Redshift cluster\. For example: `examplecluster.cg034hpkmmjt.us-east-1.redshift.amazonaws.com`\.

`Endpoint.Port`  <a name="Endpoint.Port-fn::getatt"></a>
The port number on which the Amazon Redshift cluster accepts connections\. For example: `5439`\.

`Id`  <a name="Id-fn::getatt"></a>
A unique identifier for the cluster\. You use this identifier to refer to the cluster for any subsequent cluster operations such as deleting or modifying\. The identifier also appears in the Amazon Redshift console\.  
Example: `myexamplecluster` 

## Examples<a name="aws-resource-redshift-cluster--examples"></a>



### Single\-Node Cluster<a name="aws-resource-redshift-cluster--examples--Single-Node_Cluster"></a>

The following example describes a single\-node Redshift cluster\. The master user password is referenced from an input parameter that's in the same template\.

#### JSON<a name="aws-resource-redshift-cluster--examples--Single-Node_Cluster--json"></a>

```
{
"myCluster": {
  "Type": "AWS::Redshift::Cluster",
  "Properties": {
    "DBName": "mydb",
    "MasterUsername": "master",
    "MasterUserPassword": { "Ref" : "MasterUserPassword" },
    "NodeType": "ds2.xlarge",
    "ClusterType": "single-node",
    "Tags": [{
        "Key": "foo",
        "Value": "bar"
     }
    ]
  }
}
```

#### YAML<a name="aws-resource-redshift-cluster--examples--Single-Node_Cluster--yaml"></a>

```
myCluster:
  Type: "AWS::Redshift::Cluster"
  Properties:
    DBName: "mydb"
    MasterUsername: "master"
    MasterUserPassword:
      Ref: "MasterUserPassword"
    NodeType: "ds2.xlarge"
    ClusterType: "single-node"
    Tags:
      - Key: foo
        Value: bar
```

## See also<a name="aws-resource-redshift-cluster--seealso"></a>
+ For a complete example template, see [Amazon Redshift Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-redshift.html) \.
+  [CreateCluster](https://docs.aws.amazon.com/redshift/latest/APIReference/API_CreateCluster.html) in the *Redshift API Reference*\.

