# AWS::EMR::Cluster PlacementType<a name="aws-properties-elasticmapreduce-cluster-placementtype"></a>

`PlacementType` is a property of the `AWS::EMR::Cluster` resource\. `PlacementType` determines the Amazon EC2 Availability Zone configuration of the cluster \(job flow\)\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-placementtype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-placementtype-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-elasticmapreduce-cluster-placementtype-availabilityzone)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-placementtype-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-elasticmapreduce-cluster-placementtype-availabilityzone): String
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-placementtype-properties"></a>

`AvailabilityZone`  <a name="cfn-elasticmapreduce-cluster-placementtype-availabilityzone"></a>
The Amazon EC2 Availability Zone for the cluster\. `AvailabilityZone` is used for uniform instance groups, while `AvailabilityZones` \(plural\) is used for instance fleets\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10280`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)