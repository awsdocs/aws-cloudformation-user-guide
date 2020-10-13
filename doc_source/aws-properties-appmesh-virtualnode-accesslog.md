# AWS::AppMesh::VirtualNode AccessLog<a name="aws-properties-appmesh-virtualnode-accesslog"></a>

An object that represents the access logging information for a virtual node\.

## Syntax<a name="aws-properties-appmesh-virtualnode-accesslog-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-accesslog-syntax.json"></a>

```
{
  "[File](#cfn-appmesh-virtualnode-accesslog-file)" : FileAccessLog
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-accesslog-syntax.yaml"></a>

```
  [File](#cfn-appmesh-virtualnode-accesslog-file): 
    FileAccessLog
```

## Properties<a name="aws-properties-appmesh-virtualnode-accesslog-properties"></a>

`File`  <a name="cfn-appmesh-virtualnode-accesslog-file"></a>
The file object to send virtual node access logs to\.  
*Required*: No  
*Type*: [FileAccessLog](aws-properties-appmesh-virtualnode-fileaccesslog.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)