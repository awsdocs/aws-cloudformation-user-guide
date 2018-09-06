# AWS::EC2::PlacementGroup<a name="aws-resource-ec2-placementgroup"></a>

The `AWS::EC2::PlacementGroup` resource is a logical grouping of instances within a single Availability Zone \(AZ\) that enables applications to participate in a low\-latency, 10 Gbps network\. You create a placement group first, and then you can launch instances in the placement group\.

**Topics**
+ [Syntax](#aws-resource-ec2-placementgroup-syntax)
+ [Properties](#w3ab2c21c10d449b9)
+ [Return Values](#w3ab2c21c10d449c11)
+ [Example](#w3ab2c21c10d449c13)

## Syntax<a name="aws-resource-ec2-placementgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-placementgroup-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::PlacementGroup",
  "Properties" : {
    "[Strategy](#cfn-ec2-placementgroup-strategy)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-placementgroup-syntax.yaml"></a>

```
Type: "AWS::EC2::PlacementGroup"
Properties: 
  [Strategy](#cfn-ec2-placementgroup-strategy): String
```

## Properties<a name="w3ab2c21c10d449b9"></a>

`Strategy`  <a name="cfn-ec2-placementgroup-strategy"></a>
The placement strategy, which relates to the instance types that can be added to the placement group\. For example, for the `cluster` strategy, you can cluster C4 instance types but not T2 instance types\. For valid values, see [CreatePlacementGroup](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreatePlacementGroup.html) in the *Amazon EC2 API Reference*\. By default, AWS CloudFormation sets the value of this property to `cluster`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d449c11"></a>

### Ref<a name="w3ab2c21c10d449c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d449c13"></a>

### <a name="w3ab2c21c10d449c13b2"></a>

The following example creates a placement group with a `cluster` placement strategy\.

#### JSON<a name="aws-resource-ec2-placementgroup-example-1.json"></a>

```
"PlacementGroup" : {
  "Type" : "AWS::EC2::PlacementGroup",
  "Properties" : {
    "Strategy" : "cluster"
  }
}
```

#### YAML<a name="aws-resource-ec2-placementgroup-example-1.yaml"></a>

```
PlacementGroup:
  Type: AWS::EC2::PlacementGroup
  Properties:
    Strategy: cluster
```