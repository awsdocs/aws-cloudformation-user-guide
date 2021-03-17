# AWS::Events::Connection HttpParameters<a name="aws-properties-events-connection-httpparameters"></a>

These are custom parameter to be used when the target is an API Gateway REST APIs or EventBridge ApiDestinations\. In the latter case, these are merged with any InvocationParameters specified on the Connection, with any values from the Connection taking precedence\.

## Syntax<a name="aws-properties-events-connection-httpparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-connection-httpparameters-syntax.json"></a>

```
{
  "[BodyParameters](#cfn-events-connection-httpparameters-bodyparameters)" : [ Parameter, ... ],
  "[HeaderParameters](#cfn-events-connection-httpparameters-headerparameters)" : [ Parameter, ... ],
  "[QueryStringParameters](#cfn-events-connection-httpparameters-querystringparameters)" : [ Parameter, ... ]
}
```

### YAML<a name="aws-properties-events-connection-httpparameters-syntax.yaml"></a>

```
  [BodyParameters](#cfn-events-connection-httpparameters-bodyparameters): 
    - Parameter
  [HeaderParameters](#cfn-events-connection-httpparameters-headerparameters): 
    - Parameter
  [QueryStringParameters](#cfn-events-connection-httpparameters-querystringparameters): 
    - Parameter
```

## Properties<a name="aws-properties-events-connection-httpparameters-properties"></a>

`BodyParameters`  <a name="cfn-events-connection-httpparameters-bodyparameters"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Parameter](aws-properties-events-connection-parameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderParameters`  <a name="cfn-events-connection-httpparameters-headerparameters"></a>
The headers that need to be sent as part of request invoking the API Gateway REST API or EventBridge ApiDestination\.  
*Required*: No  
*Type*: List of [Parameter](aws-properties-events-connection-parameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStringParameters`  <a name="cfn-events-connection-httpparameters-querystringparameters"></a>
The query string keys/values that need to be sent as part of request invoking the API Gateway REST API or EventBridge ApiDestination\.  
*Required*: No  
*Type*: List of [Parameter](aws-properties-events-connection-parameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)