# AWS::EC2::PlacementGroup<a name="aws-resource-ec2-placementgroup"></a>

Specifies a placement group in which to launch instances\. The strategy of the placement group determines how the instances are organized within the group\. 

A `cluster` placement group is a logical grouping of instances within a single Availability Zone that benefit from low network latency, high network throughput\. A `spread` placement group places instances on distinct hardware\. A `partition` placement group places groups of instances in different partitions, where instances in one partition do not share the same hardware with instances in another partition\.

For more information, see [Placement Groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html) in the *Amazon EC2 User Guide*\.

## Syntax<a name="aws-resource-ec2-placementgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-placementgroup-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::PlacementGroup",
  "Properties" : {
      "[PartitionCount](#cfn-ec2-placementgroup-partitioncount)" : Integer,
      "[SpreadLevel](#cfn-ec2-placementgroup-spreadlevel)" : String,
      "[Strategy](#cfn-ec2-placementgroup-strategy)" : String,
      "[Tags](#cfn-ec2-placementgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-placementgroup-syntax.yaml"></a>

```
Type: AWS::EC2::PlacementGroup
Properties: 
  [PartitionCount](#cfn-ec2-placementgroup-partitioncount): Integer
  [SpreadLevel](#cfn-ec2-placementgroup-spreadlevel): String
  [Strategy](#cfn-ec2-placementgroup-strategy): String
  [Tags](#cfn-ec2-placementgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-placementgroup-properties"></a>

`PartitionCount`  <a name="cfn-ec2-placementgroup-partitioncount"></a>
The number of partitions\. Valid only when **Strategy** is set to `partition`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SpreadLevel`  <a name="cfn-ec2-placementgroup-spreadlevel"></a>
Determines how placement groups spread instances\.   
+ Host – You can use `host` only with Outpost placement groups\.
+ Rack – No usage restrictions\.
*Required*: No  
*Type*: String  
*Allowed values*: `host | rack`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Strategy`  <a name="cfn-ec2-placementgroup-strategy"></a>
The placement strategy\.  
*Required*: No  
*Type*: String  
*Allowed values*: `cluster | partition | spread`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-placementgroup-tags"></a>
The tags to apply to the new placement group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-placementgroup-return-values"></a>

### Ref<a name="aws-resource-ec2-placementgroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the placement group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-placementgroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-placementgroup-return-values-fn--getatt-fn--getatt"></a>

`GroupName`  <a name="GroupName-fn::getatt"></a>
The name of the placement group\.

## Examples<a name="aws-resource-ec2-placementgroup--examples"></a>



### Create a placement group<a name="aws-resource-ec2-placementgroup--examples--Create_a_placement_group"></a>

The following example declares a placement group with a cluster placement strategy\. 

#### JSON<a name="aws-resource-ec2-placementgroup--examples--Create_a_placement_group--json"></a>

```
"PlacementGroup" : {
   "Type" : "AWS::EC2::PlacementGroup",
   "Properties" : {
            "Strategy" : "cluster"
   }
}
```

#### YAML<a name="aws-resource-ec2-placementgroup--examples--Create_a_placement_group--yaml"></a>

```
PlacementGroup:
  Type: AWS::EC2::PlacementGroup
   Properties:
     Strategy: cluster
```