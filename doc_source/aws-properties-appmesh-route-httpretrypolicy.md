# AWS::AppMesh::Route HttpRetryPolicy<a name="aws-properties-appmesh-route-httpretrypolicy"></a>

An object that represents a retry policy\.

## Syntax<a name="aws-properties-appmesh-route-httpretrypolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-httpretrypolicy-syntax.json"></a>

```
{
  "[HttpRetryEvents](#cfn-appmesh-route-httpretrypolicy-httpretryevents)" : [ String, ... ],
  "[MaxRetries](#cfn-appmesh-route-httpretrypolicy-maxretries)" : Integer,
  "[PerRetryTimeout](#cfn-appmesh-route-httpretrypolicy-perretrytimeout)" : [Duration](aws-properties-appmesh-route-duration.md),
  "[TcpRetryEvents](#cfn-appmesh-route-httpretrypolicy-tcpretryevents)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-appmesh-route-httpretrypolicy-syntax.yaml"></a>

```
  [HttpRetryEvents](#cfn-appmesh-route-httpretrypolicy-httpretryevents): 
    - String
  [MaxRetries](#cfn-appmesh-route-httpretrypolicy-maxretries): Integer
  [PerRetryTimeout](#cfn-appmesh-route-httpretrypolicy-perretrytimeout): 
    [Duration](aws-properties-appmesh-route-duration.md)
  [TcpRetryEvents](#cfn-appmesh-route-httpretrypolicy-tcpretryevents): 
    - String
```

## Properties<a name="aws-properties-appmesh-route-httpretrypolicy-properties"></a>

`HttpRetryEvents`  <a name="cfn-appmesh-route-httpretrypolicy-httpretryevents"></a>
Specify at least one of the following values\.  
+  **server\-error** – HTTP status codes 500, 501, 502, 503, 504, 505, 506, 507, 508, 510, and 511
+  **gateway\-error** – HTTP status codes 502, 503, and 504
+  **client\-error** – HTTP status code 409
+  **stream\-error** – Retry on refused stream
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxRetries`  <a name="cfn-appmesh-route-httpretrypolicy-maxretries"></a>
The maximum number of retry attempts\. If no value is specified, the default is 1\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerRetryTimeout`  <a name="cfn-appmesh-route-httpretrypolicy-perretrytimeout"></a>
An object that represents the retry duration\.  
*Required*: Yes  
*Type*: [Duration](aws-properties-appmesh-route-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TcpRetryEvents`  <a name="cfn-appmesh-route-httpretrypolicy-tcpretryevents"></a>
Specify a valid value\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)