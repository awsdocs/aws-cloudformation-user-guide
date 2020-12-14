# AWS::ApiGatewayV2::Api BodyS3Location<a name="aws-properties-apigatewayv2-api-bodys3location"></a>

The `BodyS3Location` property specifies an S3 location from which to import an OpenAPI definition\. Supported only for HTTP APIs\.

## Syntax<a name="aws-properties-apigatewayv2-api-bodys3location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-api-bodys3location-syntax.json"></a>

```
{
  "[Bucket](#cfn-apigatewayv2-api-bodys3location-bucket)" : String,
  "[Etag](#cfn-apigatewayv2-api-bodys3location-etag)" : String,
  "[Key](#cfn-apigatewayv2-api-bodys3location-key)" : String,
  "[Version](#cfn-apigatewayv2-api-bodys3location-version)" : String
}
```

### YAML<a name="aws-properties-apigatewayv2-api-bodys3location-syntax.yaml"></a>

```
  [Bucket](#cfn-apigatewayv2-api-bodys3location-bucket): String
  [Etag](#cfn-apigatewayv2-api-bodys3location-etag): String
  [Key](#cfn-apigatewayv2-api-bodys3location-key): String
  [Version](#cfn-apigatewayv2-api-bodys3location-version): String
```

## Properties<a name="aws-properties-apigatewayv2-api-bodys3location-properties"></a>

`Bucket`  <a name="cfn-apigatewayv2-api-bodys3location-bucket"></a>
The S3 bucket that contains the OpenAPI definition to import\. Required if you specify a `BodyS3Location` for an API\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Etag`  <a name="cfn-apigatewayv2-api-bodys3location-etag"></a>
The Etag of the S3 object\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-apigatewayv2-api-bodys3location-key"></a>
The key of the S3 object\. Required if you specify a `BodyS3Location` for an API\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-apigatewayv2-api-bodys3location-version"></a>
The version of the S3 object\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)