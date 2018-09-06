# AWS::DAX::Cluster<a name="aws-resource-dax-cluster"></a>

Use the `AWS::DAX::Cluster` resource to create a DAX cluster for use with Amazon DynamoDB\.

For information about creating a DAX cluster, see [Creating a DAX Cluster](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DAX.create-cluster.html) in the *Amazon DynamoDB Developer Guide* and [http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_dax_CreateCluster.html](http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_dax_CreateCluster.html) in the *Amazon DynamoDB Developer Guide*\.

## Syntax<a name="w3ab2c21c10d326b7"></a>

### JSON<a name="aws-resource-dax-cluster-syntax.json"></a>

```
{
   "Type": "AWS::DAX::Cluster",
   "Properties": {
      "[AvailabilityZones](#cfn-dax-cluster-availability-zones)": [ String, ... ],
      "[ClusterName](#cfn-dax-cluster-cluster-name)": String,
      "[Description](#cfn-dax-cluster-description)": String,
      "[IAMRoleARN](#cfn-dax-cluster-iam-role-arn)": String,
      "[NodeType](#cfn-dax-cluster-node-type)": String,
      "[NotificationTopicARN](#cfn-dax-cluster-notification-topic-arn)": String,
      "[ParameterGroupName](#cfn-dax-cluster-parameter-group-name)": String,
      "[PreferredMaintenanceWindow](#cfn-dax-cluster-preferred-maintenance-window)": String,
      "[ReplicationFactor](#cfn-dax-cluster-replication-factor)": Integer,
      "[SecurityGroupIds](#cfn-dax-cluster-security-group-ids)": [ String, ... ],
      "[SubnetGroupName](#cfn-dax-cluster-subnet-group-name)": String,
      "[Tags](#cfn-dax-cluster-tags)": { String:String, ... }
    }
}
```

### YAML<a name="aws-resource-dax-cluster-syntax.yaml"></a>

```
Type: "AWS::DAX::Cluster"
Properties:
      [AvailabilityZones](#cfn-dax-cluster-availability-zones): [ String, ... ]
      [ClusterName](#cfn-dax-cluster-cluster-name): String
      [Description](#cfn-dax-cluster-description): String
      [IAMRoleARN](#cfn-dax-cluster-iam-role-arn): String
      [NodeType](#cfn-dax-cluster-node-type): String
      [NotificationTopicARN](#cfn-dax-cluster-notification-topic-arn): String
      [ParameterGroupName](#cfn-dax-cluster-parameter-group-name): String
      [PreferredMaintenanceWindow](#cfn-dax-cluster-preferred-maintenance-window): String
      [ReplicationFactor](#cfn-dax-cluster-replication-factor): Integer
      [SecurityGroupIds](#cfn-dax-cluster-security-group-ids): [ String, ... ]
      [SubnetGroupName](#cfn-dax-cluster-subnet-group-name): String
      [Tags](#cfn-dax-cluster-tags): { String:String, ... }
```

## Properties<a name="aws-resource-dax-cluster-properties"></a>

`AvailabilityZones`  <a name="cfn-dax-cluster-availability-zones"></a>
The Availability Zones \(AZs\) in which the cluster nodes will be created\. All nodes belonging to the cluster are placed in these Availability Zones\. Use this parameter if you want to distribute the nodes across multiple AZs\.  
You must specify one AZ per DAX node in the cluster\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`ClusterName`  <a name="cfn-dax-cluster-cluster-name"></a>
The cluster identifier\. This parameter is stored as a lowercase string\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Description`  <a name="cfn-dax-cluster-description"></a>
A description of the cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`IAMRoleARN`  <a name="cfn-dax-cluster-iam-role-arn"></a>
A valid Amazon Resource Name \(ARN\) that identifies an IAM role\. At runtime, DAX will assume this role and use the role's permissions to access DynamoDB on your behalf\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`NodeType`  <a name="cfn-dax-cluster-node-type"></a>
The compute and memory capacity of the nodes in the cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`NotificationTopicARN`  <a name="cfn-dax-cluster-notification-topic-arn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to which notifications will be sent\.  
The Amazon SNS topic owner must be same as the DAX cluster owner\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ParameterGroupName`  <a name="cfn-dax-cluster-parameter-group-name"></a>
The parameter group to be associated with the DAX cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-dax-cluster-preferred-maintenance-window"></a>
Specifies the weekly time range during which maintenance on the DAX cluster is performed\. It is specified as a range in the format `ddd:hh24:mi-ddd:hh24:mi` \(24H Clock UTC\)\. The minimum maintenance window is a 60 minute period\. Valid values for `ddd` are:  
+  `sun` 
+  `mon` 
+  `tue` 
+  `wed` 
+  `thu` 
+  `fri` 
+  `sat` 
Example: `sun:05:00-sun:09:00`  
If you don't specify a preferred maintenance window when you create or modify a cache cluster, DAX assigns a 60\-minute maintenance window on a randomly selected day of the week\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ReplicationFactor`  <a name="cfn-dax-cluster-replication-factor"></a>
The number of nodes in the DAX cluster\. A replication factor of 1 will create a single\-node cluster, without any read replicas\. For additional fault tolerance, you can create a multiple node cluster with one or more read replicas\. To do this, set *ReplicationFactor* to 2 or more\.  
AWS recommends that you have at least two read replicas per cluster\.
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`SecurityGroupIds`  <a name="cfn-dax-cluster-security-group-ids"></a>
A list of security group IDs to be assigned to each node in the DAX cluster\. \(Each of the security group ID is system\-generated\.\)  
If this parameter is not specified, DAX assigns the default VPC security group to each node\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SubnetGroupName`  <a name="cfn-dax-cluster-subnet-group-name"></a>
The name of the subnet group to be used for the replication group\.  
DAX clusters can only run in an Amazon VPC environment\. All of the subnets that you specify in a subnet group must exist in the same VPC\.
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`Tags`  <a name="cfn-dax-cluster-tags"></a>
A map of tags to associate with the DAX cluster\.  
*Required*: No  
*Type*: String to String map  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-dax-cluster-returnvalues"></a>

### Ref<a name="aws-resource-dax-cluster-ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the name of the created DAX cluster\. For example:

```
{ "Ref": "MyDAXCluster" }
```

Returns a value similar to the following:

```
MyDAXCluster
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-dax-cluster-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
Returns the ARN of the DAX cluster\. For example:  

```
{ "Fn::GetAtt": ["MyDAXCluster", "Arn"] }
```
Returns a value similar to the following:  

```
arn:aws:dax:us-east-1:111122223333:cache/MyDAXCluster
```

`ClusterDiscoveryEndpoint`  
Returns the configuation endpoint of the DAX cluster\. For example:  

```
{ "Fn::GetAtt": ["MyDAXCluster", "ClusterDiscoveryEndpoint"] }
```
Returns a value similar to the following:  

```
mydaxcluster.0h3d6x.clustercfg.dax.use1.cache.amazonaws.com:8111
```

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="aws-resource-dax-cluster-example"></a>

The following example creates a DAX cluster\.

### JSON<a name="aws-resource-dax-cluster-example.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "Create a DAX cluster",
  "Resources": {
    "daxCluster": {
      "Type": "AWS::DAX::Cluster",
      "Properties": {
        "ClusterName": "MyDAXCluster",
        "NodeType": "dax.r3.large",
        "ReplicationFactor": 1,
        "IAMRoleARN": "arn:aws:iam::111122223333:role/DaxAccess",
        "Description": "DAX cluster created with CloudFormation",
        "SubnetGroupName": {"Ref":"subnetGroupClu"}
      }
    },
    "subnetGroupClu": {
      "Type": "AWS::DAX::SubnetGroup",
      "Properties": {
        "SubnetGroupName": "MySubnetGroup",
        "Description": "Subnet group for DAX cluster",
        "SubnetIds": [
          {"Ref":"subnet1"},
          {"Ref":"subnet2"}
        ]
      }
    },
    "subnet1": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId": {"Ref":"daxVpc"},
        "CidrBlock": "172.13.17.0/24",
        "AvailabilityZone": {
          "Fn::Select": [
            0,
            {
              "Fn::GetAZs": ""
            }
          ]
        }
      }
    },
    "subnet2": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId": {"Ref":"daxVpc"},
        "CidrBlock": "172.13.18.0/24",
        "AvailabilityZone": {
          "Fn::Select": [
            1,
            {
              "Fn::GetAZs": ""
            }
          ]
        }
      }
    },
    "daxVpc": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": "172.13.0.0/16"
      }
    }
  },
  "Outputs": {
    "Cluster": {
      "Value": {"Ref":"daxCluster"}
    }
  }
}
```

### YAML<a name="aws-resource-dax-cluster-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: "Create a DAX cluster"
Resources:
  daxCluster:
    Type: AWS::DAX::Cluster
    Properties:
      ClusterName: "MyDAXCluster"
      NodeType: "dax.r3.large"
      ReplicationFactor: 1
      IAMRoleARN: "arn:aws:iam::111122223333:role/DaxAccess"
      Description: "DAX cluster created with CloudFormation"
      SubnetGroupName: !Ref subnetGroupClu
  subnetGroupClu:
    Type: AWS::DAX::SubnetGroup
    Properties:
      SubnetGroupName: "CFNClusterSubnetGrp"
      Description: "Subnet group for DAX cluster"
      SubnetIds:
        - !Ref subnet1
        - !Ref subnet2
  subnet1:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        !Ref daxVpc
      CidrBlock: 172.13.17.0/24
      AvailabilityZone:
        Fn::Select:
          - 0
          - Fn::GetAZs: ""
  subnet2:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        !Ref daxVpc
      CidrBlock: 172.13.18.0/24
      AvailabilityZone:
        Fn::Select:
          - 1
          - Fn::GetAZs: ""
  daxVpc:
     Type: AWS::EC2::VPC
     Properties:
       CidrBlock: 172.13.0.0/16
Outputs:
  Cluster:
    Value: !Ref daxCluster
```