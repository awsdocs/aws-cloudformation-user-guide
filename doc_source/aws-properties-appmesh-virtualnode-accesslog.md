# AWS::AppMesh::VirtualNode AccessLog<a name="aws-properties-appmesh-virtualnode-accesslog"></a>

An object representing the access logging information for a virtual node\.

## Syntax<a name="aws-properties-appmesh-virtualnode-accesslog-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-accesslog-syntax.json"></a>

```
{
  "[File](#cfn-appmesh-virtualnode-accesslog-file)" : [FileAccessLog](aws-properties-appmesh-virtualnode-fileaccesslog.md)
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-accesslog-syntax.yaml"></a>

```
  [File](#cfn-appmesh-virtualnode-accesslog-file): 
    [FileAccessLog](aws-properties-appmesh-virtualnode-fileaccesslog.md)
```

## Properties<a name="aws-properties-appmesh-virtualnode-accesslog-properties"></a>

`File`  <a name="cfn-appmesh-virtualnode-accesslog-file"></a>
The file object to send virtual node access logs to\.  
*Required*: No  
*Type*: [FileAccessLog](aws-properties-appmesh-virtualnode-fileaccesslog.md)  
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
