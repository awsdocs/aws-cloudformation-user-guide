# AWS::Redshift::ClusterSubnetGroup<a name="aws-resource-redshift-clustersubnetgroup"></a>

Creates an Amazon Redshift subnet group\. You must provide a list of one or more subnets in your existing Amazon VPC when creating an Amazon Redshift subnet group\.

**Topics**
+ [Syntax](#aws-resource-redshift-clustersubnetgroup-syntax)
+ [Properties](#w3ab2c21c10e1010b9)
+ [Return Values](#w3ab2c21c10e1010c11)
+ [Example](#w3ab2c21c10e1010c13)

## Syntax<a name="aws-resource-redshift-clustersubnetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-clustersubnetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::ClusterSubnetGroup",
  "Properties" : {
    "[Description](#cfn-redshift-clustersubnetgroup-description)" : String,
    "[SubnetIds](#cfn-redshift-clustersubnetgroup-subnetids)" : [ String, ... ],
    "[Tags](#cfn-redshift-clustersubnetgroup-tags)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-redshift-clustersubnetgroup-syntax.yaml"></a>

```
Type: "AWS::Redshift::ClusterSubnetGroup"
Properties: 
  [Description](#cfn-redshift-clustersubnetgroup-description): String
  [SubnetIds](#cfn-redshift-clustersubnetgroup-subnetids):
    - String
  [Tags](#cfn-redshift-clustersubnetgroup-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10e1010b9"></a>

`Description`  <a name="cfn-redshift-clustersubnetgroup-description"></a>
A description of the subnet group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SubnetIds`  <a name="cfn-redshift-clustersubnetgroup-subnetids"></a>
A list of VPC subnet IDs\. You can modify a maximum of 20 subnets\.  
*Required*: Yes  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-redshift-clustersubnetgroup-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this subnet group\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10e1010c11"></a>

### Ref<a name="w3ab2c21c10e1010c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myClusterSubnetGroup" }
```

For the Amazon Redshift cluster subnet group `myClusterSubnetGroup`, `Ref` returns the name of the cluster subnet group\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10e1010c13"></a>

The following example specifies one subnet for an Amazon Redshift cluster subnet group\.

### JSON<a name="aws-resource-redshift-clustersubnetgroup-example-json"></a>

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

### YAML<a name="aws-resource-redshift-clustersubnetgroup-example-yaml"></a>

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