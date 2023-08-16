# AWS::AppMesh::VirtualNode LoggingFormat<a name="aws-properties-appmesh-virtualnode-loggingformat"></a>

An object that represents the format for the logs\.

## Syntax<a name="aws-properties-appmesh-virtualnode-loggingformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-loggingformat-syntax.json"></a>

```
{
  "[Json](#cfn-appmesh-virtualnode-loggingformat-json)" : [ JsonFormatRef, ... ],
  "[Text](#cfn-appmesh-virtualnode-loggingformat-text)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-loggingformat-syntax.yaml"></a>

```
  [Json](#cfn-appmesh-virtualnode-loggingformat-json): 
    - JsonFormatRef
  [Text](#cfn-appmesh-virtualnode-loggingformat-text): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-loggingformat-properties"></a>

`Json`  <a name="cfn-appmesh-virtualnode-loggingformat-json"></a>
The logging format for JSON\.  
*Required*: No  
*Type*: List of [JsonFormatRef](aws-properties-appmesh-virtualnode-jsonformatref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Text`  <a name="cfn-appmesh-virtualnode-loggingformat-text"></a>
The logging format for text\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)