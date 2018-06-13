# AWS::Redshift::Cluster<a name="aws-resource-redshift-cluster"></a>

Use the `AWS::Redshift::Cluster` resource to create an Amazon Redshift cluster\. A *cluster* is a fully managed data warehouse that consists of a set of compute nodes\. For more information about default and valid values, see [CreateCluster](http://docs.aws.amazon.com/redshift/latest/APIReference/API_CreateCluster.html) in the *Amazon Redshift API Reference*\.

**Topics**
+ [Syntax](#aws-resource-redshift-cluster-syntax)
+ [Properties](#w3ab2c21c10d989b9)
+ [Return Values](#w3ab2c21c10d989c11)
+ [Example](#w3ab2c21c10d989c13)
+ [More Info](#w3ab2c21c10d989c15)

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
    "[HsmConfigurationIdentifier](#cfn-redshift-cluster-hsmconfigidentifier)" : String,
    "[IamRoles](#cfn-redshift-cluster-iamroles)" : [ String, ... ],
    "[KmsKeyId](#cfn-redshift-cluster-kmskeyid)" : String,
    "[LoggingProperties](#cfn-redshift-cluster-loggingproperties)" :  [LoggingProperties](aws-properties-redshift-cluster-loggingproperties.md),
    "[MasterUsername](#cfn-redshift-cluster-masterusername)" : String,
    "[MasterUserPassword](#cfn-redshift-cluster-masteruserpassword)" : String,
    "[NodeType](#cfn-redshift-cluster-nodetype)" : String,
    "[NumberOfNodes](#cfn-redshift-cluster-numberofnodes)" : Integer,
    "[OwnerAccount](#cfn-redshift-cluster-owneraccount)" : String,
    "[Port](#cfn-redshift-cluster-port)" : Integer,
    "[PreferredMaintenanceWindow](#cfn-redshift-cluster-preferredmaintenancewindow)" : String,
    "[PubliclyAccessible](#cfn-redshift-cluster-publiclyaccessible)" : Boolean,
    "[SnapshotClusterIdentifier](#cfn-redshift-cluster-snapshotclusteridentifier)" : String,
    "[SnapshotIdentifier](#cfn-redshift-cluster-snapshotidentifier)" : String,
    "[Tags](#cfn-redshift-cluster-tags)" : [ Resource Tag, ... ],
    "[VpcSecurityGroupIds](#cfn-redshift-cluster-vpcsecuritygroupids)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-redshift-cluster-syntax.yaml"></a>

```
Type: "AWS::Redshift::Cluster"
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
  [HsmConfigurationIdentifier](#cfn-redshift-cluster-hsmconfigidentifier): String
  [IamRoles](#cfn-redshift-cluster-iamroles): 
    - String
  [KmsKeyId](#cfn-redshift-cluster-kmskeyid): String
  [LoggingProperties](#cfn-redshift-cluster-loggingproperties): 
     [LoggingProperties](aws-properties-redshift-cluster-loggingproperties.md)
  [MasterUsername](#cfn-redshift-cluster-masterusername): String
  [MasterUserPassword](#cfn-redshift-cluster-masteruserpassword): String
  [NodeType](#cfn-redshift-cluster-nodetype): String
  [NumberOfNodes](#cfn-redshift-cluster-numberofnodes): Integer
  [OwnerAccount](#cfn-redshift-cluster-owneraccount): String
  [Port](#cfn-redshift-cluster-port): Integer
  [PreferredMaintenanceWindow](#cfn-redshift-cluster-preferredmaintenancewindow): String
  [PubliclyAccessible](#cfn-redshift-cluster-publiclyaccessible): Boolean
  [SnapshotClusterIdentifier](#cfn-redshift-cluster-snapshotclusteridentifier): String
  [SnapshotIdentifier](#cfn-redshift-cluster-snapshotidentifier): String
  [Tags](#cfn-redshift-cluster-tags):
    - Resource Tag
  [VpcSecurityGroupIds](#cfn-redshift-cluster-vpcsecuritygroupids):
    - String
```

## Properties<a name="w3ab2c21c10d989b9"></a>

For more information about each property, including constraints and valid values, see [CreateCluster](http://docs.aws.amazon.com//redshift/latest/APIReference/API_CreateCluster.html) in the *Amazon Redshift API Reference*\.

`AllowVersionUpgrade`  <a name="cfn-redshift-cluster-allowversionupgrade"></a>
When a new version of Amazon Redshift is released, tells whether upgrades can be applied to the engine that is running on the cluster\. The upgrades are applied during the maintenance window\. The default value is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AutomatedSnapshotRetentionPeriod`  <a name="cfn-redshift-cluster-automatedsnapshotretentionperiod"></a>
The number of days that automated snapshots are retained\. The default value is `1`\. To disable automated snapshots, set the value to `0`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-redshift-cluster-availabilityzone"></a>
The Amazon Elastic Compute Cloud \(Amazon EC2\) Availability Zone in which you want to provision your Amazon Redshift cluster\. For example, if you have several EC2 instances running in a specific Availability Zone, you might want the cluster to be provisioned in the same zone to decrease network latency\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ClusterIdentifier`  <a name="cfn-redshift-cluster-clusteridentifier"></a>
The unique identifier of the cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ClusterParameterGroupName`  <a name="cfn-redshift-cluster-clusterparametergroupname"></a>
The name of the parameter group that you want to associate with this cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`ClusterSecurityGroups`  <a name="cfn-redshift-cluster-clustersecuritygroups"></a>
A list of security groups that you want to associate with this cluster\. Applies to EC2\-Classic\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ClusterSubnetGroupName`  <a name="cfn-redshift-cluster-clustersubnetgroupname"></a>
The name of a cluster subnet group that you want to associate with this cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ClusterType`  <a name="cfn-redshift-cluster-clustertype"></a>
The type of cluster\. Specify `single-node` or `multi-node` \(default\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`ClusterVersion`  <a name="cfn-redshift-cluster-clusterversion"></a>
The version of the Amazon Redshift engine that you want to deploy on the cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DBName`  <a name="cfn-redshift-cluster-dbname"></a>
The name of the first database that will be created when the cluster is created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ElasticIp`  <a name="cfn-redshift-cluster-elasticip"></a>
The Elastic IP \(EIP\) address for the cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Encrypted`  <a name="cfn-redshift-cluster-encrypted"></a>
Indicates whether the data in the cluster is encrypted at rest\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`HsmClientCertificateIdentifier`  <a name="cfn-redshift-cluster-hsmclientcertidentifier"></a>
Specifies the name of the hardware security module \(HSM\) client certificate that the Amazon Redshift cluster uses to retrieve the data encryption keys stored in an HSM\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HsmConfigurationIdentifier`  <a name="cfn-redshift-cluster-hsmconfigidentifier"></a>
The name of the HSM configuration that contains the information that the Amazon Redshift cluster can use to retrieve and store keys in an HSM\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`IamRoles`  <a name="cfn-redshift-cluster-iamroles"></a>
A list of AWS Identity and Access Management \(IAM\) roles that the cluster can use to access other AWS services\. Supply the IAM roles by their Amazon Resource Name \(ARN\)\. You can provide a maximum of 10 IAM roles in a single request\. A cluster can have a maximum of 10 IAM roles associated with it at a time\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KmsKeyId`  <a name="cfn-redshift-cluster-kmskeyid"></a>
The ID of the AWS Key Management Service \(AWS KMS\) key that you want to use to encrypt data in the cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LoggingProperties`  <a name="cfn-redshift-cluster-loggingproperties"></a>
Configures Amazon Redshift to create audit log files, containing logging information such as queries and connection attempts, for this cluster\.   
*Required*: No  
*Type*: [Amazon Redshift LoggingProperties ](aws-properties-redshift-cluster-loggingproperties.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MasterUsername`  <a name="cfn-redshift-cluster-masterusername"></a>
The user name that is associated with the master user account for this cluster\.  
You must specify values for `MasterUserName` and `MasterUserPassword`\. However, if you're restoring from an Amazon Redshift snapshot, AWS CloudFormation ignores the specified values and uses the values that are stored in the snapshot\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`MasterUserPassword`  <a name="cfn-redshift-cluster-masteruserpassword"></a>
The password associated with the master user account for this cluster\.  
You must specify values for `MasterUserName` and `MasterUserPassword`\. However, if you're restoring from an Amazon Redshift snapshot, AWS CloudFormation ignores the specified values and uses the values that are stored in the snapshot\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NodeType`  <a name="cfn-redshift-cluster-nodetype"></a>
The node type that is provisioned for this cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NumberOfNodes`  <a name="cfn-redshift-cluster-numberofnodes"></a>
The number of compute nodes in the cluster\. If you specify `multi-node` for the `ClusterType` parameter, you must specify a number greater than `1`\.  
You can't specify this parameter for a single\-node cluster\.
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`OwnerAccount`  <a name="cfn-redshift-cluster-owneraccount"></a>
When you restore from a snapshot from another AWS account, the 12\-digit AWS account ID that contains that snapshot\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Port`  <a name="cfn-redshift-cluster-port"></a>
The port number on which the cluster accepts incoming connections\. The default value is `5439`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PreferredMaintenanceWindow`  <a name="cfn-redshift-cluster-preferredmaintenancewindow"></a>
The weekly time range \(in UTC\) during which automated cluster maintenance can occur\. The format of the time range is `ddd:hh24:mi-ddd:hh24:mi`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PubliclyAccessible`  <a name="cfn-redshift-cluster-publiclyaccessible"></a>
Indicates whether the cluster can be accessed from a public network\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SnapshotClusterIdentifier`  <a name="cfn-redshift-cluster-snapshotclusteridentifier"></a>
The name of the cluster that the source snapshot was created from\. For more information about restoring from a snapshot, see the [RestoreFromClusterSnapshot](http://docs.aws.amazon.com/redshift/latest/APIReference/API_RestoreFromClusterSnapshot.html) action in the *Amazon Redshift API Reference*\.  
*Required*: No  
*Required*: Conditional\. This property is required if your IAM policy includes a restriction on the cluster name and the resource element specifies anything other than the wildcard character \(`*`\) for the cluster name\.  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SnapshotIdentifier`  <a name="cfn-redshift-cluster-snapshotidentifier"></a>
The name of the snapshot from which to create a new cluster\.  
*Required*: Conditional\. If you specified the `SnapshotClusterIdentifier` property, you must specify this property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-redshift-cluster-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this cluster\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-redshift-cluster-vpcsecuritygroupids"></a>
A list of VPC security groups that are associated with this cluster\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d989c11"></a>

### Ref<a name="w3ab2c21c10d989c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myCluster" }
```

For the Amazon Redshift cluster `myCluster`, `Ref` returns the name of the cluster\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d989c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Endpoint.Address`  
The connection endpoint for the Amazon Redshift cluster\. For example: `examplecluster.cg034hpkmmjt.us-east-1.redshift.amazonaws.com` \.

`Endpoint.Port`  
The port number on which the Amazon Redshift cluster accepts connections\. For example: `5439`\.

## Example<a name="w3ab2c21c10d989c13"></a>

The following example describes a single\-node Amazon Redshift cluster\. The master user password is referenced from an input parameter that is in the same template\.

### JSON<a name="aws-resource-redshift-cluster-example.json"></a>

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
      {
        "Key": "foo",
        "Value": "bar"
      }
    ]
  }
}
```

### YAML<a name="aws-resource-redshift-cluster-example.yaml"></a>

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

## More Info<a name="w3ab2c21c10d989c15"></a>

For a complete example template, see [Amazon Redshift Template Snippets](quickref-redshift.md)\.