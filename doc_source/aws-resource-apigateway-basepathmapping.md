# AWS::ApiGateway::BasePathMapping<a name="aws-resource-apigateway-basepathmapping"></a>

The `AWS::ApiGateway::BasePathMapping` resource creates a base path that clients who call your Amazon API Gateway API must use in the invocation URL\.


+ [Syntax](#aws-resource-apigateway-basepathmapping-syntax)
+ [Properties](#w3ab2c21c10c27b9)

## Syntax<a name="aws-resource-apigateway-basepathmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-basepathmapping-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::BasePathMapping",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-basepathmapping-basepath)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-basepathmapping-domainname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-basepathmapping-restapiid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-basepathmapping-stage)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-basepathmapping-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::BasePathMapping"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-basepathmapping-basepath): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-basepathmapping-domainname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-basepathmapping-restapiid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-basepathmapping-stage): String
```

## Properties<a name="w3ab2c21c10c27b9"></a>

`BasePath`  
The base path name that callers of the API must provide in the URL after the domain name\. If you specify this property, it can't be an empty string\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`DomainName`  
The domain name of a `DomainName` resource\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`RestApiId`  
The name of the API\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`Stage`  
The name of the API's stage\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption