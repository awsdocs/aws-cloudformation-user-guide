# AWS::ApiGateway::DocumentationPart Location<a name="aws-properties-apigateway-documentationpart-location"></a>

The `Location` property specifies the location of the Amazon API Gateway API entity that the documentation applies to\. `Location` is a property of the [AWS::ApiGateway::DocumentationPart](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-documentationpart.html) resource\.

**Note**  
For more information about each property, including constraints and valid values, see [DocumentationPart](https://docs.aws.amazon.com/apigateway/latest/api/API_DocumentationPartLocation.html) in the *Amazon API Gateway REST API Reference*\.

## Syntax<a name="aws-properties-apigateway-documentationpart-location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-documentationpart-location-syntax.json"></a>

```
{
  "[Method](#cfn-apigateway-documentationpart-location-method)" : String,
  "[Name](#cfn-apigateway-documentationpart-location-name)" : String,
  "[Path](#cfn-apigateway-documentationpart-location-path)" : String,
  "[StatusCode](#cfn-apigateway-documentationpart-location-statuscode)" : String,
  "[Type](#cfn-apigateway-documentationpart-location-type)" : String
}
```

### YAML<a name="aws-properties-apigateway-documentationpart-location-syntax.yaml"></a>

```
  [Method](#cfn-apigateway-documentationpart-location-method): String
  [Name](#cfn-apigateway-documentationpart-location-name): String
  [Path](#cfn-apigateway-documentationpart-location-path): String
  [StatusCode](#cfn-apigateway-documentationpart-location-statuscode): String
  [Type](#cfn-apigateway-documentationpart-location-type): String
```

## Properties<a name="aws-properties-apigateway-documentationpart-location-properties"></a>

`Method`  <a name="cfn-apigateway-documentationpart-location-method"></a>
The HTTP verb of a method\. It is a valid field for the API entity types of `METHOD`, `PATH_PARAMETER`, `QUERY_PARAMETER`, `REQUEST_HEADER`, `REQUEST_BODY`, `RESPONSE`, `RESPONSE_HEADER`, and `RESPONSE_BODY`\. The default value is `*` for any method\. When an applicable child entity inherits the content of an entity of the same type with more general specifications of the other `location` attributes, the child entity's `method` attribute must match that of the parent entity exactly\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-apigateway-documentationpart-location-name"></a>
The name of the targeted API entity\. It is a valid and required field for the API entity types of `AUTHORIZER`, `MODEL`, `PATH_PARAMETER`, `QUERY_PARAMETER`, `REQUEST_HEADER`, `REQUEST_BODY` and `RESPONSE_HEADER`\. It is an invalid field for any other entity type\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Path`  <a name="cfn-apigateway-documentationpart-location-path"></a>
The URL path of the target\. It is a valid field for the API entity types of `RESOURCE`, `METHOD`, `PATH_PARAMETER`, `QUERY_PARAMETER`, `REQUEST_HEADER`, `REQUEST_BODY`, `RESPONSE`, `RESPONSE_HEADER`, and `RESPONSE_BODY`\. The default value is `/` for the root resource\. When an applicable child entity inherits the content of another entity of the same type with more general specifications of the other `location` attributes, the child entity's `path` attribute must match that of the parent entity as a prefix\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StatusCode`  <a name="cfn-apigateway-documentationpart-location-statuscode"></a>
The HTTP status code of a response\. It is a valid field for the API entity types of `RESPONSE`, `RESPONSE_HEADER`, and `RESPONSE_BODY`\. The default value is `*` for any status code\. When an applicable child entity inherits the content of an entity of the same type with more general specifications of the other `location` attributes, the child entity's `statusCode` attribute must match that of the parent entity exactly\.  
*Required*: No  
*Type*: String  
*Pattern*: `^([1-5]\d\d|\*|\s*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-apigateway-documentationpart-location-type"></a>
The type of API entity to which the documentation content applies\. Valid values are `API`, `AUTHORIZER`, `MODEL`, `RESOURCE`, `METHOD`, `PATH_PARAMETER`, `QUERY_PARAMETER`, `REQUEST_HEADER`, `REQUEST_BODY`, `RESPONSE`, `RESPONSE_HEADER`, and `RESPONSE_BODY`\. Content inheritance does not apply to any entity of the `API`, `AUTHORIZER`, `METHOD`, `MODEL`, `REQUEST_BODY`, or `RESOURCE` type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `API | AUTHORIZER | METHOD | MODEL | PATH_PARAMETER | QUERY_PARAMETER | REQUEST_BODY | REQUEST_HEADER | RESOURCE | RESPONSE | RESPONSE_BODY | RESPONSE_HEADER`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-apigateway-documentationpart-location--seealso"></a>
+ [DocumentationPart](https://docs.aws.amazon.com/apigateway/latest/api/API_DocumentationPartLocation.html) in the *Amazon API Gateway REST API Reference*

