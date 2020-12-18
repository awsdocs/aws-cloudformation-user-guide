# AWS::Redshift::ClusterSubnetGroup<a name="aws-resource-redshift-clustersubnetgroup"></a>

Specifies an Amazon Redshift subnet group\. You must provide a list of one or more subnets in your existing Amazon Virtual Private Cloud \(Amazon VPC\) when creating Amazon Redshift subnet group\.

 For information about subnet groups, go to [Amazon Redshift Cluster Subnet Groups](https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-cluster-subnet-groups.html) in the *Amazon Redshift Cluster Management Guide*\.

## Syntax<a name="aws-resource-redshift-clustersubnetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-clustersubnetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::ClusterSubnetGroup",
  "Properties" : {
      "[Description](#cfn-redshift-clustersubnetgroup-description)" : String,
      "[SubnetIds](#cfn-redshift-clustersubnetgroup-subnetids)" : [ String, ... ],
      "[Tags](#cfn-redshift-clustersubnetgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-redshift-clustersubnetgroup-syntax.yaml"></a>

```
Type: AWS::Redshift::ClusterSubnetGroup
Properties: 
  [Description](#cfn-redshift-clustersubnetgroup-description): String
  [SubnetIds](#cfn-redshift-clustersubnetgroup-subnetids): 
    - String
  [Tags](#cfn-redshift-clustersubnetgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-redshift-clustersubnetgroup-properties"></a>

`Description`  <a name="cfn-redshift-clustersubnetgroup-description"></a>
A description for the subnet group\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-redshift-clustersubnetgroup-subnetids"></a>
An array of VPC subnet IDs\. A maximum of 20 subnets can be modified in a single request\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-redshift-clustersubnetgroup-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this subnet group\. Use tags to manage your resources\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-redshift-clustersubnetgroup-return-values"></a>

### Ref<a name="aws-resource-redshift-clustersubnetgroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myClusterSubnetGroup" }` 

For the Amazon Redshift subnet group `myClusterSubnetGroup`, Ref returns the name of the cluster subnet group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-redshift-clustersubnetgroup--examples"></a>



### Specify a Subnet<a name="aws-resource-redshift-clustersubnetgroup--examples--Specify_a_Subnet"></a>

The following example specifies one subnet for an Amazon Redshift cluster subnet group\.

#### JSON<a name="aws-resource-redshift-clustersubnetgroup--examples--Specify_a_Subnet--json"></a>

```
"myClusterSubnetGroup": {
  "Type": "AWS::Redshift::ClusterSubnetGroup",
  "Properties": {
    "Description": "My ClusterSubnetGroup",
    "SubnetIds": [
      "subnet-7fbc2813"
    ],
    "Tags": [
      {
        "Key": "foo",
        "Value": "bar"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-redshift-clustersubnetgroup--examples--Specify_a_Subnet--yaml"></a>

```
myClusterSubnetGroup:
  Type: 'AWS::Redshift::ClusterSubnetGroup'
  Properties:
    Description: My ClusterSubnetGroup
    SubnetIds:
      - subnet-7fbc2813
    Tags:
      - Key: foo
        Value: bar
```