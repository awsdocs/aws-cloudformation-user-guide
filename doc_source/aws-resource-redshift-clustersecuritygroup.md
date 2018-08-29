# AWS::Redshift::ClusterSecurityGroup<a name="aws-resource-redshift-clustersecuritygroup"></a>

Creates an Amazon Redshift security group\. You use security groups to control access to Amazon Redshift clusters that are not in a VPC\.

**Topics**
+ [Syntax](#aws-resource-redshift-clustersecuritygroup-syntax)
+ [Properties](#w3ab2c21c10e1000b9)
+ [Return Values](#w3ab2c21c10e1000c11)
+ [Example](#w3ab2c21c10e1000c13)
+ [See Also](#w3ab2c21c10e1000c15)

## Syntax<a name="aws-resource-redshift-clustersecuritygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-clustersecuritygroup-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::ClusterSecurityGroup",
  "Properties" : {
    "[Description](#cfn-redshift-clustersecuritygroup-description)" : String,
    "[Tags](#cfn-redshift-clustersecuritygroup-tags)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-redshift-clustersecuritygroup-syntax.yaml"></a>

```
Type: "AWS::Redshift::ClusterSecurityGroup"
Properties: 
  [Description](#cfn-redshift-clustersecuritygroup-description): String
  [Tags](#cfn-redshift-clustersecuritygroup-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10e1000b9"></a>

`Description`  <a name="cfn-redshift-clustersecuritygroup-description"></a>
A description of the security group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-redshift-clustersecuritygroup-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this security group\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10e1000c11"></a>

### Ref<a name="w3ab2c21c10e1000c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myClusterSecurityGroup" }
```

For the Amazon Redshift cluster security group `myClusterSecurityGroup`, `Ref` returns the name of the cluster security group\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10e1000c13"></a>

The following example creates an Amazon Redshift cluster security group that you can associate cluster security group ingress rules with:

### JSON<a name="aws-resource-redshift-clustersecuritygroup-example.json"></a>

```
"myClusterSecurityGroup": {
  "Type": "AWS::Redshift::ClusterSecurityGroup",
  "Properties": {
    "Description": "Security group to determine where connections to the Amazon Redshift cluster can come from",
    "Tags": [
      {
        "Key": "foo",
        "Value": "bar"
      }
    ]
  }
}
```

### YAML<a name="aws-resource-redshift-clustersecuritygroup-example.yaml"></a>

```
myClusterSecurityGroup: 
  Type: "AWS::Redshift::ClusterSecurityGroup"
  Properties: 
    Description: "Security group to determine where connections to the Amazon Redshift cluster can come from"
    Tags:
      - Key: foo
        Value: bar
```

## See Also<a name="w3ab2c21c10e1000c15"></a>
+ [AWS::Redshift::ClusterSecurityGroupIngress](aws-resource-redshift-clustersecuritygroupingress.md)