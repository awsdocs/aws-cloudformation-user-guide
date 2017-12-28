# Amazon API Gateway DocumentationPart Location<a name="aws-properties-apigateway-documentationpart-location"></a>

The `Location` property specifies the location of the Amazon API Gateway API entity that the documentation applies to\. `Location` is a property of the [AWS::ApiGateway::DocumentationPart](aws-resource-apigateway-documentationpart.md) resource\.

## Syntax<a name="aws-properties-apigateway-documentationpart-location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-documentationpart-location-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-documentationpart-location-method)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-documentationpart-location-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-documentationpart-location-path)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-documentationpart-location-statuscode)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-documentationpart-location-type)" : String
}
```

### YAML<a name="aws-properties-apigateway-documentationpart-location-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-documentationpart-location-method): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-documentationpart-location-name): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-documentationpart-location-path): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-documentationpart-location-statuscode): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-documentationpart-location-type): String
```

## Properties<a name="aws-properties-apigateway-documentationpart-location-properties"></a>

**Note**  
For more information about each property, including constraints and valid values, see [ DocumentationPart](http://docs.aws.amazon.com/apigateway/api-reference/resource/documentation-part/#location) in the *Amazon API Gateway REST API Reference*\.

`Method`  
The HTTP verb of a method\.  
 *Required*: No  
*Type*: String  
 *Update requires*: Replacement 

`Name`  
The name of the targeted API entity\.  
 *Required*: No  
*Type*: String  
 *Update requires*: Replacement 

`Path`  
The URL path of the target\.  
 *Required*: No  
*Type*: String  
 *Update requires*: Replacement 

`StatusCode`  
The HTTP status code of a response\.  
 *Required*: No  
*Type*: String  
 *Update requires*: Replacement 

`Type`  
The type of API entity that the documentation content applies to\.  
 *Required*: No  
*Type*: String  
 *Update requires*: Replacement 