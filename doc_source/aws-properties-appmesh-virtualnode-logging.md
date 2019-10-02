# AWS::AppMesh::VirtualNode Logging<a name="aws-properties-appmesh-virtualnode-logging"></a>

An object representing the logging information for a virtual node\.

## Syntax<a name="aws-properties-appmesh-virtualnode-logging-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-logging-syntax.json"></a>

```
{
  "[AccessLog](#cfn-appmesh-virtualnode-logging-accesslog)" : [AccessLog](aws-properties-appmesh-virtualnode-accesslog.md)
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-logging-syntax.yaml"></a>

```
  [AccessLog](#cfn-appmesh-virtualnode-logging-accesslog): 
    [AccessLog](aws-properties-appmesh-virtualnode-accesslog.md)
```

## Properties<a name="aws-properties-appmesh-virtualnode-logging-properties"></a>

`AccessLog`  <a name="cfn-appmesh-virtualnode-logging-accesslog"></a>
The access log configuration for a virtual node\.  
*Required*: No  
*Type*: [AccessLog](aws-properties-appmesh-virtualnode-accesslog.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
