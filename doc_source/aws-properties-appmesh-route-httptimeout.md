# AWS::AppMesh::Route HttpTimeout<a name="aws-properties-appmesh-route-httptimeout"></a>

An object that represents types of timeouts\. 

## Syntax<a name="aws-properties-appmesh-route-httptimeout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-httptimeout-syntax.json"></a>

```
{
  "[Idle](#cfn-appmesh-route-httptimeout-idle)" : [Duration](aws-properties-appmesh-route-duration.md),
  "[PerRequest](#cfn-appmesh-route-httptimeout-perrequest)" : [Duration](aws-properties-appmesh-route-duration.md)
}
```

### YAML<a name="aws-properties-appmesh-route-httptimeout-syntax.yaml"></a>

```
  [Idle](#cfn-appmesh-route-httptimeout-idle): 
    [Duration](aws-properties-appmesh-route-duration.md)
  [PerRequest](#cfn-appmesh-route-httptimeout-perrequest): 
    [Duration](aws-properties-appmesh-route-duration.md)
```

## Properties<a name="aws-properties-appmesh-route-httptimeout-properties"></a>

`Idle`  <a name="cfn-appmesh-route-httptimeout-idle"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [Duration](aws-properties-appmesh-route-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerRequest`  <a name="cfn-appmesh-route-httptimeout-perrequest"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [Duration](aws-properties-appmesh-route-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)