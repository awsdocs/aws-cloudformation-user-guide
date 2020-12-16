# AWS::DAX::Cluster<a name="aws-resource-dax-cluster"></a>

Creates a DAX cluster\. All nodes in the cluster run the same DAX caching software\.

## Syntax<a name="aws-resource-dax-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dax-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::DAX::Cluster",
  "Properties" : {
      "[AvailabilityZones](#cfn-dax-cluster-availabilityzones)" : [ String, ... ],
      "[ClusterName](#cfn-dax-cluster-clustername)" : String,
      "[Description](#cfn-dax-cluster-description)" : String,
      "[IAMRoleARN](#cfn-dax-cluster-iamrolearn)" : String,
      "[NodeType](#cfn-dax-cluster-nodetype)" : String,
      "[NotificationTopicARN](#cfn-dax-cluster-notificationtopicarn)" : String,
      "[ParameterGroupName](#cfn-dax-cluster-parametergroupname)" : String,
      "[PreferredMaintenanceWindow](#cfn-dax-cluster-preferredmaintenancewindow)" : String,
      "[ReplicationFactor](#cfn-dax-cluster-replicationfactor)" : Integer,
      "[SecurityGroupIds](#cfn-dax-cluster-securitygroupids)" : [ String, ... ],
      "[SSESpecification](#cfn-dax-cluster-ssespecification)" : SSESpecification,
      "[SubnetGroupName](#cfn-dax-cluster-subnetgroupname)" : String,
      "[Tags](#cfn-dax-cluster-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-dax-cluster-syntax.yaml"></a>

```
Type: AWS::DAX::Cluster
Properties: 
  [AvailabilityZones](#cfn-dax-cluster-availabilityzones): 
    - String
  [ClusterName](#cfn-dax-cluster-clustername): String
  [Description](#cfn-dax-cluster-description): String
  [IAMRoleARN](#cfn-dax-cluster-iamrolearn): String
  [NodeType](#cfn-dax-cluster-nodetype): String
  [NotificationTopicARN](#cfn-dax-cluster-notificationtopicarn): String
  [ParameterGroupName](#cfn-dax-cluster-parametergroupname): String
  [PreferredMaintenanceWindow](#cfn-dax-cluster-preferredmaintenancewindow): String
  [ReplicationFactor](#cfn-dax-cluster-replicationfactor): Integer
  [SecurityGroupIds](#cfn-dax-cluster-securitygroupids): 
    - String
  [SSESpecification](#cfn-dax-cluster-ssespecification): 
    SSESpecification
  [SubnetGroupName](#cfn-dax-cluster-subnetgroupname): String
  [Tags](#cfn-dax-cluster-tags): Json
```

## Properties<a name="aws-resource-dax-cluster-properties"></a>

`AvailabilityZones`  <a name="cfn-dax-cluster-availabilityzones"></a>
The Availability Zones \(AZs\) in which the cluster nodes will reside after the cluster has been created or updated\. If provided, the length of this list must equal the `ReplicationFactor` parameter\. If you omit this parameter, DAX will spread the nodes across Availability Zones for the highest availability\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterName`  <a name="cfn-dax-cluster-clustername"></a>
The name of the DAX cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Description`  <a name="cfn-dax-cluster-description"></a>
The description of the cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IAMRoleARN`  <a name="cfn-dax-cluster-iamrolearn"></a>
A valid Amazon Resource Name \(ARN\) that identifies an IAM role\. At runtime, DAX will assume this role and use the role's permissions to access DynamoDB on your behalf\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`NodeType`  <a name="cfn-dax-cluster-nodetype"></a>
The node type for the nodes in the cluster\. \(All nodes in a DAX cluster are of the same type\.\)  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`NotificationTopicARN`  <a name="cfn-dax-cluster-notificationtopicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to which notifications will be sent\.  
The Amazon SNS topic owner must be same as the DAX cluster owner\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterGroupName`  <a name="cfn-dax-cluster-parametergroupname"></a>
The parameter group to be associated with the DAX cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-dax-cluster-preferredmaintenancewindow"></a>
A range of time when maintenance of DAX cluster software will be performed\. For example: `sun:01:00-sun:09:00`\. Cluster maintenance normally takes less than 30 minutes, and is performed automatically within the maintenance window\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationFactor`  <a name="cfn-dax-cluster-replicationfactor"></a>
The number of nodes in the DAX cluster\. A replication factor of 1 will create a single\-node cluster, without any read replicas\. For additional fault tolerance, you can create a multiple node cluster with one or more read replicas\. To do this, set `ReplicationFactor` to a number between 3 \(one primary and two read replicas\) and 10 \(one primary and nine read replicas\)\. `If the AvailabilityZones` parameter is provided, its length must equal the `ReplicationFactor`\.  
AWS recommends that you have at least two read replicas per cluster\.
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-dax-cluster-securitygroupids"></a>
A list of security group IDs to be assigned to each node in the DAX cluster\. \(Each of the security group ID is system\-generated\.\)  
If this parameter is not specified, DAX assigns the default VPC security group to each node\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SSESpecification`  <a name="cfn-dax-cluster-ssespecification"></a>
Represents the settings used to enable server\-side encryption on the cluster\.  
*Required*: No  
*Type*: [SSESpecification](aws-properties-dax-cluster-ssespecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetGroupName`  <a name="cfn-dax-cluster-subnetgroupname"></a>
The name of the subnet group to be used for the replication group\.  
DAX clusters can only run in an Amazon VPC environment\. All of the subnets that you specify in a subnet group must exist in the same VPC\.
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Tags`  <a name="cfn-dax-cluster-tags"></a>
A set of tags to associate with the DAX cluster\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-dax-cluster-return-values"></a>

### Ref<a name="aws-resource-dax-cluster-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the created DAX cluster\. For example:

```
{ "Ref": "MyResource" }
```

 Returns a value similar to the following: 

```
MyDAXCluster
```

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-dax-cluster-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

#### <a name="aws-resource-dax-cluster-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the ARN of the DAX cluster\. For example:  

```
{ "Fn::GetAtt": ["MyDAXCluster", "Arn"] }
```
Returns a value similar to the following:  

```
arn:aws:dax:us-east-1:111122223333:cache/MyDAXCluster
```

`ClusterDiscoveryEndpoint`  <a name="ClusterDiscoveryEndpoint-fn::getatt"></a>
Returns the configuration endpoint of the DAX cluster\. For example:  

```
{ "Fn::GetAtt": ["MyDAXCluster", "ClusterDiscoveryEndpoint"] }
```
Returns a value similar to the following:  

```
mydaxcluster.0h3d6x.clustercfg.dax.use1.cache.amazonaws.com:8111
```

## Examples<a name="aws-resource-dax-cluster--examples"></a>

### Create Cluster<a name="aws-resource-dax-cluster--examples--Create_Cluster"></a>

The following example creates a DAX cluster\.

#### JSON<a name="aws-resource-dax-cluster--examples--Create_Cluster--json"></a>

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

#### YAML<a name="aws-resource-dax-cluster--examples--Create_Cluster--yaml"></a>

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