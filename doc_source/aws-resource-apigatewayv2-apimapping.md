# AWS::ApiGatewayV2::ApiMapping<a name="aws-resource-apigatewayv2-apimapping"></a>

The `AWS::ApiGatewayV2::ApiMapping` resource contains an API mapping\. An API mapping relates a path of your custom domain name to a stage of your API\. A custom domain name can have multiple API mappings, but the paths can't overlap\. A custom domain can map only to APIs of the same protocol type\. For more information, see [CreateApiMapping](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/domainnames-domainname-apimappings.html#CreateApiMapping) in the *Amazon API Gateway V2 API Reference*\.

## Syntax<a name="aws-resource-apigatewayv2-apimapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-apimapping-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::ApiMapping",
  "Properties" : {
      "[ApiId](#cfn-apigatewayv2-apimapping-apiid)" : String,
      "[ApiMappingKey](#cfn-apigatewayv2-apimapping-apimappingkey)" : String,
      "[DomainName](#cfn-apigatewayv2-apimapping-domainname)" : String,
      "[Stage](#cfn-apigatewayv2-apimapping-stage)" : String
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-apimapping-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::ApiMapping
Properties: 
  [ApiId](#cfn-apigatewayv2-apimapping-apiid): String
  [ApiMappingKey](#cfn-apigatewayv2-apimapping-apimappingkey): String
  [DomainName](#cfn-apigatewayv2-apimapping-domainname): String
  [Stage](#cfn-apigatewayv2-apimapping-stage): String
```

## Properties<a name="aws-resource-apigatewayv2-apimapping-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-apimapping-apiid"></a>
The identifier of the API\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ApiMappingKey`  <a name="cfn-apigatewayv2-apimapping-apimappingkey"></a>
The API mapping key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-apigatewayv2-apimapping-domainname"></a>
The domain name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Stage`  <a name="cfn-apigatewayv2-apimapping-stage"></a>
The API stage\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-apimapping-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-apimapping-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the API mapping resource ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigatewayv2-apimapping--examples"></a>



### API mapping creation example<a name="aws-resource-apigatewayv2-apimapping--examples--API_mapping_creation_example"></a>

The following example creates an `ApiMapping` resource called `MyApiMapping`\.

#### JSON<a name="aws-resource-apigatewayv2-apimapping--examples--API_mapping_creation_example--json"></a>

```
{
    "MyApiMapping": {
        "Type": "AWS::ApiGatewayV2::ApiMapping",
        "Properties": {
            "DomainName": "mydomainame.us-east-1.com",
            "ApiId": {
                "Ref": "MyApi"
            },
            "Stage": {
                "Ref": "MyStage"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigatewayv2-apimapping--examples--API_mapping_creation_example--yaml"></a>

```
MyApiMapping:
  Type: 'AWS::ApiGatewayV2::ApiMapping'
  Properties:
    DomainName: mydomainame.us-east-1.com
    ApiId: !Ref MyApi
    Stage: !Ref MyStage
```

## See also<a name="aws-resource-apigatewayv2-apimapping--seealso"></a>
+ [CreateApiMapping](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/domainnames-domainname-apimappings.html#CreateApiMapping) in the *Amazon API Gateway Version 2 API Reference*

