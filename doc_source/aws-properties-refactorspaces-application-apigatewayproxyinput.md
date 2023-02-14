# AWS::RefactorSpaces::Application ApiGatewayProxyInput<a name="aws-properties-refactorspaces-application-apigatewayproxyinput"></a>

A wrapper object holding the Amazon API Gateway endpoint input\. 

## Syntax<a name="aws-properties-refactorspaces-application-apigatewayproxyinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-refactorspaces-application-apigatewayproxyinput-syntax.json"></a>

```
{
  "[EndpointType](#cfn-refactorspaces-application-apigatewayproxyinput-endpointtype)" : String,
  "[StageName](#cfn-refactorspaces-application-apigatewayproxyinput-stagename)" : String
}
```

### YAML<a name="aws-properties-refactorspaces-application-apigatewayproxyinput-syntax.yaml"></a>

```
  [EndpointType](#cfn-refactorspaces-application-apigatewayproxyinput-endpointtype): String
  [StageName](#cfn-refactorspaces-application-apigatewayproxyinput-stagename): String
```

## Properties<a name="aws-properties-refactorspaces-application-apigatewayproxyinput-properties"></a>

`EndpointType`  <a name="cfn-refactorspaces-application-apigatewayproxyinput-endpointtype"></a>
The type of endpoint to use for the API Gateway proxy\. If no value is specified in the request, the value is set to `REGIONAL` by default\.  
If the value is set to `PRIVATE` in the request, this creates a private API endpoint that is isolated from the public internet\. The private endpoint can only be accessed by using Amazon Virtual Private Cloud \(Amazon VPC\) endpoints for Amazon API Gateway that have been granted access\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StageName`  <a name="cfn-refactorspaces-application-apigatewayproxyinput-stagename"></a>
The name of the API Gateway stage\. The name defaults to `prod`\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)