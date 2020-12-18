# AWS::ApiGateway::DocumentationPart Location<a name="aws-properties-apigateway-documentationpart-location"></a>

The `Location` property specifies the location of the Amazon API Gateway API entity that the documentation applies to\. `Location` is a property of the [AWS::ApiGateway::DocumentationPart](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-documentationpart.html) resource\.

**Note**  
For more information about each property, including constraints and valid values, see [DocumentationPart](https://docs.aws.amazon.com/apigateway/api-reference/resource/documentation-part/#location) in the *Amazon API Gateway REST API Reference*\.

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
The HTTP verb of a method\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-apigateway-documentationpart-location-name"></a>
The name of the targeted API entity\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Path`  <a name="cfn-apigateway-documentationpart-location-path"></a>
The URL path of the target\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StatusCode`  <a name="cfn-apigateway-documentationpart-location-statuscode"></a>
The HTTP status code of a response\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-apigateway-documentationpart-location-type"></a>
The type of API entity that the documentation content applies to\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-apigateway-documentationpart-location--seealso"></a>
+ [DocumentationPart](https://docs.aws.amazon.com/apigateway/api-reference/resource/documentation-part/) in the *Amazon API Gateway REST API Reference*

