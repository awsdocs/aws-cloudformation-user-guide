# AWS::AppMesh::VirtualNode FileAccessLog<a name="aws-properties-appmesh-virtualnode-fileaccesslog"></a>

An object that represents an access log file\.

## Syntax<a name="aws-properties-appmesh-virtualnode-fileaccesslog-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-fileaccesslog-syntax.json"></a>

```
{
  "[Path](#cfn-appmesh-virtualnode-fileaccesslog-path)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-fileaccesslog-syntax.yaml"></a>

```
  [Path](#cfn-appmesh-virtualnode-fileaccesslog-path): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-fileaccesslog-properties"></a>

`Path`  <a name="cfn-appmesh-virtualnode-fileaccesslog-path"></a>
The file path to write access logs to\. You can use `/dev/stdout` to send access logs to standard out and configure your Envoy container to use a log driver, such as `awslogs`, to export the access logs to a log storage service such as Amazon CloudWatch Logs\. You can also specify a path in the Envoy container's file system to write the files to disk\.  
The Envoy process must have write permissions to the path that you specify here\. Otherwise, Envoy fails to bootstrap properly\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)