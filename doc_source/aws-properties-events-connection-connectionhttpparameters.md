# AWS::Events::Connection ConnectionHttpParameters<a name="aws-properties-events-connection-connectionhttpparameters"></a>

Contains additional parameters for the connection\.

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
Contains additional body string parameters for the connection\.  
*Required*: No  
*Type*: List of [Parameter](aws-properties-events-connection-parameter.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderParameters`  <a name="cfn-events-connection-connectionhttpparameters-headerparameters"></a>
Contains additional header parameters for the connection\.  
*Required*: No  
*Type*: List of [Parameter](aws-properties-events-connection-parameter.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStringParameters`  <a name="cfn-events-connection-connectionhttpparameters-querystringparameters"></a>
Contains additional query string parameters for the connection\.  
*Required*: No  
*Type*: List of [Parameter](aws-properties-events-connection-parameter.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)