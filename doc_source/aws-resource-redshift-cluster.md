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
      "[AutomatedSnapshotRetentionPeriod](#cfn-redshift-cluster-automatedsnapshotretentionperiod)" : Integer,
      "[AvailabilityZone](#cfn-redshift-cluster-availabilityzone)" : String,
      "[ClusterIdentifier](#cfn-redshift-cluster-clusteridentifier)" : String,
      "[ClusterParameterGroupName](#cfn-redshift-cluster-clusterparametergroupname)" : String,
      "[ClusterSecurityGroups](#cfn-redshift-cluster-clustersecuritygroups)" : [ String, ... ],
      "[ClusterSubnetGroupName](#cfn-redshift-cluster-clustersubnetgroupname)" : String,
      "[ClusterType](#cfn-redshift-cluster-clustertype)" : String,
      "[ClusterVersion](#cfn-redshift-cluster-clusterversion)" : String,
      "[DBName](#cfn-redshift-cluster-dbname)" : String,
      "[ElasticIp](#cfn-redshift-cluster-elasticip)" : String,
      "[Encrypted](#cfn-redshift-cluster-encrypted)" : Boolean,
      "[HsmClientCertificateIdentifier](#cfn-redshift-cluster-hsmclientcertidentifier)" : String,
      "[HsmConfigurationIdentifier](#cfn-redshift-cluster-HsmConfigurationIdentifier)" : String,
      "[IamRoles](#cfn-redshift-cluster-iamroles)" : [ String, ... ],
      "[KmsKeyId](#cfn-redshift-cluster-kmskeyid)" : String,
      "[LoggingProperties](#cfn-redshift-cluster-loggingproperties)" : LoggingProperties,
      "[MasterUsername](#cfn-redshift-cluster-masterusername)" : String,
      "[MasterUserPassword](#cfn-redshift-cluster-masteruserpassword)" : String,
      "[NodeType](#cfn-redshift-cluster-nodetype)" : String,
      "[NumberOfNodes](#cfn-redshift-cluster-nodetype)" : Integer,
      "[OwnerAccount](#cfn-redshift-cluster-owneraccount)" : String,
      "[Port](#cfn-redshift-cluster-port)" : Integer,
      "[PreferredMaintenanceWindow](#cfn-redshift-cluster-preferredmaintenancewindow)" : String,
      "[PubliclyAccessible](#cfn-redshift-cluster-publiclyaccessible)" : Boolean,
      "[SnapshotClusterIdentifier](#cfn-redshift-cluster-snapshotclusteridentifier)" : String,
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
  [AutomatedSnapshotRetentionPeriod](#cfn-redshift-cluster-automatedsnapshotretentionperiod): Integer
  [AvailabilityZone](#cfn-redshift-cluster-availabilityzone): String
  [ClusterIdentifier](#cfn-redshift-cluster-clusteridentifier): String
  [ClusterParameterGroupName](#cfn-redshift-cluster-clusterparametergroupname): String
  [ClusterSecurityGroups](#cfn-redshift-cluster-clustersecuritygroups): 
    - String
  [ClusterSubnetGroupName](#cfn-redshift-cluster-clustersubnetgroupname): String
  [ClusterType](#cfn-redshift-cluster-clustertype): String
  [ClusterVersion](#cfn-redshift-cluster-clusterversion): String
  [DBName](#cfn-redshift-cluster-dbname): String
  [ElasticIp](#cfn-redshift-cluster-elasticip): String
  [Encrypted](#cfn-redshift-cluster-encrypted): Boolean
  [HsmClientCertificateIdentifier](#cfn-redshift-cluster-hsmclientcertidentifier): String
  [HsmConfigurationIdentifier](#cfn-redshift-cluster-HsmConfigurationIdentifier): String
  [IamRoles](#cfn-redshift-cluster-iamroles): 
    - String
  [KmsKeyId](#cfn-redshift-cluster-kmskeyid): String
  [LoggingProperties](#cfn-redshift-cluster-loggingproperties): 
    LoggingProperties
  [MasterUsername](#cfn-redshift-cluster-masterusername): String
  [MasterUserPassword](#cfn-redshift-cluster-masteruserpassword): String
  [NodeType](#cfn-redshift-cluster-nodetype): String
  [NumberOfNodes](#cfn-redshift-cluster-nodetype): Integer
  [OwnerAccount](#cfn-redshift-cluster-owneraccount): String
  [Port](#cfn-redshift-cluster-port): Integer
  [PreferredMaintenanceWindow](#cfn-redshift-cluster-preferredmaintenancewindow): String
  [PubliclyAccessible](#cfn-redshift-cluster-publiclyaccessible): Boolean
  [SnapshotClusterIdentifier](#cfn-redshift-cluster-snapshotclusteridentifier): String
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

`AutomatedSnapshotRetentionPeriod`  <a name="cfn-redshift-cluster-automatedsnapshotretentionperiod"></a>
The number of days that automated snapshots are retained\. If the value is 0, automated snapshots are disabled\. Even if automated snapshots are disabled, you can still create manual snapshots when you want with CreateClusterSnapshot\.   
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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

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

`ElasticIp`  <a name="cfn-redshift-cluster-elasticip"></a>
The Elastic IP \(EIP\) address for the cluster\.  
Constraints: The cluster must be provisioned in EC2\-VPC and publicly\-accessible through an Internet gateway\. For more information about provisioning clusters in EC2\-VPC, go to [Supported Platforms to Launch Your Cluster](https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-clusters.html#cluster-platforms) in the Amazon Redshift Cluster Management Guide\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Encrypted`  <a name="cfn-redshift-cluster-encrypted"></a>
If `true`, the data in the cluster is encrypted at rest\.   
Default: false  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HsmClientCertificateIdentifier`  <a name="cfn-redshift-cluster-hsmclientcertidentifier"></a>
Specifies the name of the HSM client certificate the Amazon Redshift cluster uses to retrieve the data encryption keys stored in an HSM\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HsmConfigurationIdentifier`  <a name="cfn-redshift-cluster-HsmConfigurationIdentifier"></a>
Specifies the name of the HSM configuration that contains the information the Amazon Redshift cluster can use to retrieve and store keys in an HSM\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamRoles`  <a name="cfn-redshift-cluster-iamroles"></a>
A list of AWS Identity and Access Management \(IAM\) roles that can be used by the cluster to access other AWS services\. You must supply the IAM roles in their Amazon Resource Name \(ARN\) format\. You can supply up to 10 IAM roles in a single request\.  
A cluster can have up to 10 IAM roles associated with it at any time\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-redshift-cluster-kmskeyid"></a>
The AWS Key Management Service \(KMS\) key ID of the encryption key that you want to use to encrypt data in the cluster\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoggingProperties`  <a name="cfn-redshift-cluster-loggingproperties"></a>
Specifies logging information, such as queries and connection attempts, for the specified Amazon Redshift cluster\.  
*Required*: No  
*Type*: [LoggingProperties](aws-properties-redshift-cluster-loggingproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUsername`  <a name="cfn-redshift-cluster-masterusername"></a>
The user name associated with the master user account for the cluster that is being created\.  
Constraints:  
+ Must be 1 \- 128 alphanumeric characters\. The user name can't be `PUBLIC`\.
+ First character must be a letter\.
+ Cannot be a reserved word\. A list of reserved words can be found in [Reserved Words](https://docs.aws.amazon.com/redshift/latest/dg/r_pg_keywords.html) in the Amazon Redshift Database Developer Guide\. 
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUserPassword`  <a name="cfn-redshift-cluster-masteruserpassword"></a>
The password associated with the master user account for the cluster that is being created\.  
Constraints:  
+ Must be between 8 and 64 characters in length\.
+ Must contain at least one uppercase letter\.
+ Must contain at least one lowercase letter\.
+ Must contain one number\.
+ Can be any printable ASCII character \(ASCII code 33 to 126\) except ' \(single quote\), " \(double quote\), \\, /, @, or space\.
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

`NumberOfNodes`  <a name="cfn-redshift-cluster-nodetype"></a>
The number of compute nodes in the cluster\. This parameter is required when the **ClusterType** parameter is specified as `multi-node`\.   
For information about determining how many nodes you need, go to [ Working with Clusters](https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-clusters.html#how-many-nodes) in the *Amazon Redshift Cluster Management Guide*\.   
If you don't specify this parameter, you get a single\-node cluster\. When requesting a multi\-node cluster, you must specify the number of nodes that you want in the cluster\.  
Default: `1`   
Constraints: Value must be at least 1 and no more than 100\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OwnerAccount`  <a name="cfn-redshift-cluster-owneraccount"></a>
The AWS customer account used to create or copy the snapshot\. Required if you are restoring a snapshot you do not own, optional if you own the snapshot\.  
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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

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

`SnapshotClusterIdentifier`  <a name="cfn-redshift-cluster-snapshotclusteridentifier"></a>
The name of the cluster the source snapshot was created from\. This parameter is required if your IAM user has a policy containing a snapshot resource element that specifies anything other than \* for the cluster name\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnapshotIdentifier`  <a name="cfn-redshift-cluster-snapshotidentifier"></a>
The name of the snapshot from which to create the new cluster\. This parameter isn't case sensitive\.  
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

`Endpoint.Address`  <a name="Endpoint.Address-fn::getatt"></a>
The connection endpoint for the Amazon Redshift cluster\. For example: `examplecluster.cg034hpkmmjt.us-east-1.redshift.amazonaws.com`\.

`Endpoint.Port`  <a name="Endpoint.Port-fn::getatt"></a>
The port number on which the Amazon Redshift cluster accepts connections\. For example: `5439`\.

## Examples<a name="aws-resource-redshift-cluster--examples"></a>



### Single\-Node Cluster<a name="aws-resource-redshift-cluster--examples--Single-Node_Cluster"></a>

The following example describes a single\-node Redshift cluster\. The master user password is referenced from an input parameter that is in the same template\.

#### JSON<a name="aws-resource-redshift-cluster--examples--Single-Node_Cluster--json"></a>

```
"myCluster": {
  "Type": "AWS::Redshift::Cluster",
  "Properties": {
    "DBName": "mydb", 
    "MasterUsername": "master",
    "MasterUserPassword": { "Ref" : "MasterUserPassword" },
    "NodeType": "ds2.xlarge",
    "ClusterType": "single-node",
    "Tags": [
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
+ For a complete example template, see [Amazon Redshift Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-redshift.html)\.
+  [CreateCluster](https://docs.aws.amazon.com/redshift/latest/APIReference/API_CreateCluster.html) in the *Redshift API Reference*\.

