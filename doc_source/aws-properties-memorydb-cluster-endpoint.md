# AWS::MemoryDB::Cluster Endpoint<a name="aws-properties-memorydb-cluster-endpoint"></a>

Represents the information required for client programs to connect to the cluster and its nodes\.

## Syntax<a name="aws-properties-memorydb-cluster-endpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-memorydb-cluster-endpoint-syntax.json"></a>

```
{
  "[Address](#cfn-memorydb-cluster-endpoint-address)" : String,
  "[Port](#cfn-memorydb-cluster-endpoint-port)" : Integer
}
```

### YAML<a name="aws-properties-memorydb-cluster-endpoint-syntax.yaml"></a>

```
  [Address](#cfn-memorydb-cluster-endpoint-address): String
  [Port](#cfn-memorydb-cluster-endpoint-port): Integer
```

## Properties<a name="aws-properties-memorydb-cluster-endpoint-properties"></a>

`Address`  <a name="cfn-memorydb-cluster-endpoint-address"></a>
The DNS hostname of the node\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-memorydb-cluster-endpoint-port"></a>
The port number that the engine is listening on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)