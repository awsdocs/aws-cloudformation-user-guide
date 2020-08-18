# AWS::AppMesh::Route TcpTimeout<a name="aws-properties-appmesh-route-tcptimeout"></a>

An object that represents types of timeouts\. 

## Syntax<a name="aws-properties-appmesh-route-tcptimeout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-tcptimeout-syntax.json"></a>

```
{
  "[Idle](#cfn-appmesh-route-tcptimeout-idle)" : Duration
}
```

### YAML<a name="aws-properties-appmesh-route-tcptimeout-syntax.yaml"></a>

```
  [Idle](#cfn-appmesh-route-tcptimeout-idle): 
    Duration
```

## Properties<a name="aws-properties-appmesh-route-tcptimeout-properties"></a>

`Idle`  <a name="cfn-appmesh-route-tcptimeout-idle"></a>
An object that represents an idle timeout\. An idle timeout bounds the amount of time that a connection may be idle\. The default value is none\.  
*Required*: No  
*Type*: [Duration](aws-properties-appmesh-route-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)