# AWS::Redshift::Cluster<a name="aws-resource-redshift-cluster"></a>

Use the `AWS::Redshift::Cluster` resource to create an Amazon Redshift cluster\. A *cluster* is a fully managed data warehouse that consists of a set of compute nodes\. For more information about default and valid values, see [CreateCluster](http://docs.aws.amazon.com/redshift/latest/APIReference/API_CreateCluster.html) in the *Amazon Redshift API Reference*\.


+ [Syntax](#aws-resource-redshift-cluster-syntax)
+ [Properties](#w3ab2c21c10d917b9)
+ [Return Values](#w3ab2c21c10d917c11)
+ [Example](#w3ab2c21c10d917c13)
+ [More Info](#w3ab2c21c10d917c15)

## Syntax<a name="aws-resource-redshift-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::Cluster",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-allowversionupgrade)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-automatedsnapshotretentionperiod)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-availabilityzone)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-clusterparametergroupname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-clustersecuritygroups)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-clustersubnetgroupname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-clustertype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-clusterversion)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-dbname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-elasticip)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-encrypted)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-hsmclientcertidentifier)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-hsmconfigidentifier)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-iamroles)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-kmskeyid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-loggingproperties)" :  LoggingProperties,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-masterusername)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-masteruserpassword)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-nodetype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-numberofnodes)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-owneraccount)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-port)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-preferredmaintenancewindow)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-publiclyaccessible)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-snapshotclusteridentifier)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-snapshotidentifier)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-tags)" : [ Resource Tag, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-vpcsecuritygroupids)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-redshift-cluster-syntax.yaml"></a>

```
Type: "AWS::Redshift::Cluster"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-allowversionupgrade): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-automatedsnapshotretentionperiod): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-availabilityzone): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-clusterparametergroupname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-clustersecuritygroups): 
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-clustersubnetgroupname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-clustertype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-clusterversion): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-dbname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-elasticip): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-encrypted): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-hsmclientcertidentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-hsmconfigidentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-iamroles): 
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-kmskeyid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-loggingproperties): 
     LoggingProperties
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-masterusername): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-masteruserpassword): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-nodetype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-numberofnodes): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-owneraccount): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-port): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-preferredmaintenancewindow): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-publiclyaccessible): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-snapshotclusteridentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-snapshotidentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-tags):
    - Resource Tag
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-cluster-vpcsecuritygroupids):
    - String
```

## Properties<a name="w3ab2c21c10d917b9"></a>

For more information about each property, including constraints and valid values, see [CreateCluster](http://docs.aws.amazon.com//redshift/latest/APIReference/API_CreateCluster.html) in the *Amazon Redshift API Reference*\.

`AllowVersionUpgrade`  
When a new version of Amazon Redshift is released, tells whether upgrades can be applied to the engine that is running on the cluster\. The upgrades are applied during the maintenance window\. The default value is `true`\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`AutomatedSnapshotRetentionPeriod`  
The number of days that automated snapshots are retained\. The default value is `1`\. To disable automated snapshots, set the value to `0`\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`AvailabilityZone`  
The Amazon Elastic Compute Cloud \(Amazon EC2\) Availability Zone in which you want to provision your Amazon Redshift cluster\. For example, if you have several EC2 instances running in a specific Availability Zone, you might want the cluster to be provisioned in the same zone to decrease network latency\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`ClusterParameterGroupName`  
The name of the parameter group that you want to associate with this cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Some interruptions

`ClusterSecurityGroups`  
A list of security groups that you want to associate with this cluster\. Applies to EC2\-Classic\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`ClusterSubnetGroupName`  
The name of a cluster subnet group that you want to associate with this cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`ClusterType`  
The type of cluster\. Specify `single-node` or `multi-node` \(default\)\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Some interruptions

`ClusterVersion`  
The version of the Amazon Redshift engine that you want to deploy on the cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`DBName`  
The name of the first database that will be created when the cluster is created\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`ElasticIp`  
The Elastic IP \(EIP\) address for the cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Encrypted`  
Indicates whether the data in the cluster is encrypted at rest\. The default value is `false`\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: Replacement

`HsmClientCertificateIdentifier`  
Specifies the name of the hardware security module \(HSM\) client certificate that the Amazon Redshift cluster uses to retrieve the data encryption keys stored in an HSM\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`HsmConfigurationIdentifier`  
The name of the HSM configuration that contains the information that the Amazon Redshift cluster can use to retrieve and store keys in an HSM\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`IamRoles`  
A list of AWS Identity and Access Management \(IAM\) roles that the cluster can use to access other AWS services\. Supply the IAM roles by their Amazon Resource Name \(ARN\)\. You can provide a maximum of 10 IAM roles in a single request\. A cluster can have a maximum of 10 IAM roles associated with it at a time\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`KmsKeyId`  
The ID of the AWS Key Management Service \(AWS KMS\) key that you want to use to encrypt data in the cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`LoggingProperties`  
Configures Amazon Redshift to create audit log files, containing logging information such as queries and connection attempts, for this cluster\.   
*Required: *No  
*Type*: [Amazon Redshift LoggingProperties ](aws-properties-redshift-cluster-loggingproperties.md)  
*Update requires*: No interruption

`MasterUsername`  
The user name that is associated with the master user account for this cluster\.  
You must specify values for `MasterUserName` and `MasterUserPassword`\. However, if you're restoring from an Amazon Redshift snapshot, AWS CloudFormation ignores the specified values and uses the values that are stored in the snapshot\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`MasterUserPassword`  
The password associated with the master user account for this cluster\.  
You must specify values for `MasterUserName` and `MasterUserPassword`\. However, if you're restoring from an Amazon Redshift snapshot, AWS CloudFormation ignores the specified values and uses the values that are stored in the snapshot\.  
*Required*: Yes  
*Type*: String  
*Update requires*: No interruption

`NodeType`  
The node type that is provisioned for this cluster\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`NumberOfNodes`  
The number of compute nodes in the cluster\. If you specify `multi-node` for the `ClusterType` parameter, you must specify a number greater than `1`\.  
You can't specify this parameter for a single\-node cluster\.
*Required: *Conditional  
*Type*: Integer  
*Update requires*: Some interruptions

`OwnerAccount`  
When you restore from a snapshot from another AWS account, the 12\-digit AWS account ID that contains that snapshot\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Port`  
The port number on which the cluster accepts incoming connections\. The default value is `5439`\.  
*Required: *No  
*Type*: Integer  
*Update requires*: Replacement

`PreferredMaintenanceWindow`  
The weekly time range \(in UTC\) during which automated cluster maintenance can occur\. The format of the time range is `ddd:hh24:mi-ddd:hh24:mi`\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`PubliclyAccessible`  
Indicates whether the cluster can be accessed from a public network\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: Replacement

`SnapshotClusterIdentifier`  
The name of the cluster that the source snapshot was created from\. For more information about restoring from a snapshot, see the [RestoreFromClusterSnapshot](http://docs.aws.amazon.com/redshift/latest/APIReference/API_RestoreFromClusterSnapshot.html) action in the *Amazon Redshift API Reference*\.  
*Required: *No  
*Required: *Conditional\. This property is required if your IAM policy includes a restriction on the cluster name and the resource element specifies anything other than the wildcard character \(`*`\) for the cluster name\.  
*Update requires*: Replacement

`SnapshotIdentifier`  
The name of the snapshot from which to create a new cluster\.  
*Required: *Conditional\. If you specified the `SnapshotClusterIdentifier` property, you must specify this property\.  
*Type*: String  
*Update requires*: Replacement

`Tags`  
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this cluster\. Use tags to manage your resources\.  
*Required: *No  
*Type*:   
*Update requires*: No interruption

`VpcSecurityGroupIds`  
A list of VPC security groups that are associated with this cluster\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

## Return Values<a name="w3ab2c21c10d917c11"></a>

### Ref<a name="w3ab2c21c10d917c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myCluster" }
```

For the Amazon Redshift cluster `myCluster`, `Ref` returns the name of the cluster\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d917c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Endpoint.Address`  
The connection endpoint for the Amazon Redshift cluster\. For example: `examplecluster.cg034hpkmmjt.us-east-1.redshift.amazonaws.com` \.

`Endpoint.Port`  
The port number on which the Amazon Redshift cluster accepts connections\. For example: `5439`\.

## Example<a name="w3ab2c21c10d917c13"></a>

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

## More Info<a name="w3ab2c21c10d917c15"></a>

For a complete example template, see [Amazon Redshift Template Snippets](quickref-redshift.md)\.