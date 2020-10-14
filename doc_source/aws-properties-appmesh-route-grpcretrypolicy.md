# AWS::AppMesh::Route GrpcRetryPolicy<a name="aws-properties-appmesh-route-grpcretrypolicy"></a>

An object that represents a retry policy\. Specify at least one value for at least one of the types of `RetryEvents`, a value for `maxRetries`, and a value for `perRetryTimeout`\.

## Syntax<a name="aws-properties-appmesh-route-grpcretrypolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-grpcretrypolicy-syntax.json"></a>

```
{
  "[GrpcRetryEvents](#cfn-appmesh-route-grpcretrypolicy-grpcretryevents)" : [ String, ... ],
  "[HttpRetryEvents](#cfn-appmesh-route-grpcretrypolicy-httpretryevents)" : [ String, ... ],
  "[MaxRetries](#cfn-appmesh-route-grpcretrypolicy-maxretries)" : Integer,
  "[PerRetryTimeout](#cfn-appmesh-route-grpcretrypolicy-perretrytimeout)" : Duration,
  "[TcpRetryEvents](#cfn-appmesh-route-grpcretrypolicy-tcpretryevents)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-appmesh-route-grpcretrypolicy-syntax.yaml"></a>

```
  [GrpcRetryEvents](#cfn-appmesh-route-grpcretrypolicy-grpcretryevents): 
    - String
  [HttpRetryEvents](#cfn-appmesh-route-grpcretrypolicy-httpretryevents): 
    - String
  [MaxRetries](#cfn-appmesh-route-grpcretrypolicy-maxretries): Integer
  [PerRetryTimeout](#cfn-appmesh-route-grpcretrypolicy-perretrytimeout): 
    Duration
  [TcpRetryEvents](#cfn-appmesh-route-grpcretrypolicy-tcpretryevents): 
    - String
```

## Properties<a name="aws-properties-appmesh-route-grpcretrypolicy-properties"></a>

`GrpcRetryEvents`  <a name="cfn-appmesh-route-grpcretrypolicy-grpcretryevents"></a>
Specify at least one of the valid values\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpRetryEvents`  <a name="cfn-appmesh-route-grpcretrypolicy-httpretryevents"></a>
Specify at least one of the following values\.  
+ **server\-error** – HTTP status codes 500, 501, 502, 503, 504, 505, 506, 507, 508, 510, and 511
+ **gateway\-error** – HTTP status codes 502, 503, and 504
+ **client\-error** – HTTP status code 409
+ **stream\-error** – Retry on refused stream
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxRetries`  <a name="cfn-appmesh-route-grpcretrypolicy-maxretries"></a>
The maximum number of retry attempts\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerRetryTimeout`  <a name="cfn-appmesh-route-grpcretrypolicy-perretrytimeout"></a>
The timeout for each retry attempt\.  
*Required*: Yes  
*Type*: [Duration](aws-properties-appmesh-route-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TcpRetryEvents`  <a name="cfn-appmesh-route-grpcretrypolicy-tcpretryevents"></a>
Specify a valid value\. The event occurs before any processing of a request has started and is encountered when the upstream is temporarily or permanently unavailable\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)