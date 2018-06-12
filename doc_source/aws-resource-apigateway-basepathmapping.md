# AWS::ApiGateway::BasePathMapping<a name="aws-resource-apigateway-basepathmapping"></a>

The `AWS::ApiGateway::BasePathMapping` resource creates a base path that clients who call your Amazon API Gateway API must use in the invocation URL\.

**Topics**
+ [Syntax](#aws-resource-apigateway-basepathmapping-syntax)
+ [Properties](#w3ab2c21c10c27b9)

## Syntax<a name="aws-resource-apigateway-basepathmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-basepathmapping-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::BasePathMapping",
  "Properties" : {
    "[BasePath](#cfn-apigateway-basepathmapping-basepath)" : String,
    "[DomainName](#cfn-apigateway-basepathmapping-domainname)" : String,
    "[RestApiId](#cfn-apigateway-basepathmapping-restapiid)" : String,
    "[Stage](#cfn-apigateway-basepathmapping-stage)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-basepathmapping-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::BasePathMapping"
Properties:
  [BasePath](#cfn-apigateway-basepathmapping-basepath): String
  [DomainName](#cfn-apigateway-basepathmapping-domainname): String
  [RestApiId](#cfn-apigateway-basepathmapping-restapiid): String
  [Stage](#cfn-apigateway-basepathmapping-stage): String
```

## Properties<a name="w3ab2c21c10c27b9"></a>

`BasePath`  <a name="cfn-apigateway-basepathmapping-basepath"></a>
The base path name that callers of the API must provide in the URL after the domain name\. If you specify this property, it can't be an empty string\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DomainName`  <a name="cfn-apigateway-basepathmapping-domainname"></a>
The domain name of a `DomainName` resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RestApiId`  <a name="cfn-apigateway-basepathmapping-restapiid"></a>
The name of the API\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Stage`  <a name="cfn-apigateway-basepathmapping-stage"></a>
The name of the API's stage\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)