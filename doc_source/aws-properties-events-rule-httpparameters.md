# AWS::Events::Rule HttpParameters<a name="aws-properties-events-rule-httpparameters"></a>

These are custom parameter to be used when the target is an API Gateway REST APIs\.

`HttpParameters` is a property of the `Target` property type\.

## Syntax<a name="aws-properties-events-rule-httpparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-httpparameters-syntax.json"></a>

```
{
  "[HeaderParameters](#cfn-events-rule-httpparameters-headerparameters)" : {Key : Value, ...},
  "[PathParameterValues](#cfn-events-rule-httpparameters-pathparametervalues)" : [ String, ... ],
  "[QueryStringParameters](#cfn-events-rule-httpparameters-querystringparameters)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-events-rule-httpparameters-syntax.yaml"></a>

```
  [HeaderParameters](#cfn-events-rule-httpparameters-headerparameters): 
    Key : Value
  [PathParameterValues](#cfn-events-rule-httpparameters-pathparametervalues): 
    - String
  [QueryStringParameters](#cfn-events-rule-httpparameters-querystringparameters): 
    Key : Value
```

## Properties<a name="aws-properties-events-rule-httpparameters-properties"></a>

`HeaderParameters`  <a name="cfn-events-rule-httpparameters-headerparameters"></a>
The headers that need to be sent as part of request invoking the API Gateway REST API\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PathParameterValues`  <a name="cfn-events-rule-httpparameters-pathparametervalues"></a>
The path parameter values to be used to populate API Gateway REST API path wildcards \("\*"\)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStringParameters`  <a name="cfn-events-rule-httpparameters-querystringparameters"></a>
The query string keys/values that need to be sent as part of request invoking the API Gateway REST API\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)