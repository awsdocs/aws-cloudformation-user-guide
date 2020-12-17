# AWS::AppMesh::Route WeightedTarget<a name="aws-properties-appmesh-route-weightedtarget"></a>

An object that represents a target and its relative weight\. Traffic is distributed across targets according to their relative weight\. For example, a weighted target with a relative weight of 50 receives five times as much traffic as one with a relative weight of 10\. The total weight for all targets combined must be less than or equal to 100\.

## Syntax<a name="aws-properties-appmesh-route-weightedtarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-weightedtarget-syntax.json"></a>

```
{
  "[VirtualNode](#cfn-appmesh-route-weightedtarget-virtualnode)" : String,
  "[Weight](#cfn-appmesh-route-weightedtarget-weight)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-route-weightedtarget-syntax.yaml"></a>

```
  [VirtualNode](#cfn-appmesh-route-weightedtarget-virtualnode): String
  [Weight](#cfn-appmesh-route-weightedtarget-weight): Integer
```

## Properties<a name="aws-properties-appmesh-route-weightedtarget-properties"></a>

`VirtualNode`  <a name="cfn-appmesh-route-weightedtarget-virtualnode"></a>
The virtual node to associate with the weighted target\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-appmesh-route-weightedtarget-weight"></a>
The relative weight of the weighted target\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)