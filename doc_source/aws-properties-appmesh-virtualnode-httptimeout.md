# AWS::AppMesh::VirtualNode HttpTimeout<a name="aws-properties-appmesh-virtualnode-httptimeout"></a>

An object that represents types of timeouts\. 

## Syntax<a name="aws-properties-appmesh-virtualnode-httptimeout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-httptimeout-syntax.json"></a>

```
{
  "[Idle](#cfn-appmesh-virtualnode-httptimeout-idle)" : Duration,
  "[PerRequest](#cfn-appmesh-virtualnode-httptimeout-perrequest)" : Duration
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-httptimeout-syntax.yaml"></a>

```
  [Idle](#cfn-appmesh-virtualnode-httptimeout-idle): 
    Duration
  [PerRequest](#cfn-appmesh-virtualnode-httptimeout-perrequest): 
    Duration
```

## Properties<a name="aws-properties-appmesh-virtualnode-httptimeout-properties"></a>

`Idle`  <a name="cfn-appmesh-virtualnode-httptimeout-idle"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [Duration](aws-properties-appmesh-virtualnode-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerRequest`  <a name="cfn-appmesh-virtualnode-httptimeout-perrequest"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [Duration](aws-properties-appmesh-virtualnode-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)