# AWS::EC2::PlacementGroup<a name="aws-resource-ec2-placementgroup"></a>

Specifies a placement group in which to launch instances\. The strategy of the placement group determines how the instances are organized within the group\. 

A `cluster` placement group is a logical grouping of instances within a single Availability Zone that benefit from low network latency, high network throughput\. A `spread` placement group places instances on distinct hardware\. A `partition` placement group places groups of instances in different partitions, where instances in one partition do not share the same hardware with instances in another partition\.

For more information, see [Placement Groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html) in the *Amazon Elastic Compute Cloud User Guide*\.

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
Type: AWS::EC2::PlacementGroup
Properties: 
  [Strategy](#cfn-ec2-placementgroup-strategy): String
```

## Properties<a name="aws-resource-ec2-placementgroup-properties"></a>

`Strategy`  <a name="cfn-ec2-placementgroup-strategy"></a>
The placement strategy\.  
*Required*: No  
*Type*: String  
*Allowed values*: `cluster | partition | spread`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-placementgroup-return-values"></a>

### Ref<a name="aws-resource-ec2-placementgroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the placement group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-placementgroup--examples"></a>



### Create a Placement Group<a name="aws-resource-ec2-placementgroup--examples--Create_a_Placement_Group"></a>

The following example declares a placement group with a cluster placement strategy\. 

#### JSON<a name="aws-resource-ec2-placementgroup--examples--Create_a_Placement_Group--json"></a>

```
"PlacementGroup" : {
   "Type" : "AWS::EC2::PlacementGroup",
   "Properties" : {
            "Strategy" : "cluster"
   }
}
```

#### YAML<a name="aws-resource-ec2-placementgroup--examples--Create_a_Placement_Group--yaml"></a>

```
PlacementGroup:
  Type: AWS::EC2::PlacementGroup
   Properties:
     Strategy: cluster
```