# AWS::Events::Connection ConnectionHttpParameters<a name="aws-properties-events-connection-connectionhttpparameters"></a>

The headers that need to be sent as part of the request that invokes any Api destinations that use this connection to authorize with the invocation HTTP endpoint\.

## Syntax<a name="aws-properties-events-connection-connectionhttpparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-connection-connectionhttpparameters-syntax.json"></a>

```
{
  "[BodyParameters](#cfn-events-connection-connectionhttpparameters-bodyparameters)" : [ Parameter, ... ],
  "[HeaderParameters](#cfn-events-connection-connectionhttpparameters-headerparameters)" : [ Parameter, ... ],
  "[QueryStringParameters](#cfn-events-connection-connectionhttpparameters-querystringparameters)" : [ Parameter, ... ]
}
```

### YAML<a name="aws-properties-events-connection-connectionhttpparameters-syntax.yaml"></a>

```
  [BodyParameters](#cfn-events-connection-connectionhttpparameters-bodyparameters): 
    - Parameter
  [HeaderParameters](#cfn-events-connection-connectionhttpparameters-headerparameters): 
    - Parameter
  [QueryStringParameters](#cfn-events-connection-connectionhttpparameters-querystringparameters): 
    - Parameter
```

## Properties<a name="aws-properties-events-connection-connectionhttpparameters-properties"></a>

`BodyParameters`  <a name="cfn-events-connection-connectionhttpparameters-bodyparameters"></a>
The body parameters that need to be sent as part of the request that invokes any Api destinations that use this connection to authorize with the invocation HTTP endpoint\.  
*Required*: No  
*Type*: List of [Parameter](aws-properties-events-connection-parameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderParameters`  <a name="cfn-events-connection-connectionhttpparameters-headerparameters"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Parameter](aws-properties-events-connection-parameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStringParameters`  <a name="cfn-events-connection-connectionhttpparameters-querystringparameters"></a>
The query string parameters to include in the request for an Api destination that uses this connection to authorize with the invocation HTTP endpoint\.   
*Required*: No  
*Type*: List of [Parameter](aws-properties-events-connection-parameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)