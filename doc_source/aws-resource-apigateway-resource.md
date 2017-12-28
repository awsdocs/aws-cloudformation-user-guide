# AWS::ApiGateway::Resource<a name="aws-resource-apigateway-resource"></a>

The `AWS::ApiGateway::Resource` resource creates a resource in an Amazon API Gateway \(API Gateway\) API\.


+ [Syntax](#aws-resource-apigateway-resource-syntax)
+ [Properties](#w3ab2c21c10c72b9)
+ [Return Value](#w3ab2c21c10c72c11)
+ [Example](#w3ab2c21c10c72c13)

## Syntax<a name="aws-resource-apigateway-resource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-resource-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Resource",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-resource-parentid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-resource-pathpart)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-resource-resapiid)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-resource-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::Resource"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-resource-parentid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-resource-pathpart): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-resource-resapiid): String
```

## Properties<a name="w3ab2c21c10c72b9"></a>

`ParentId`  
If you want to create a child resource, the ID of the parent resource\. For resources without a parent, specify the RestApi root resource ID, such as `{ "Fn::GetAtt": ["MyRestApi", "RootResourceId"] }`\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`PathPart`  
A path name for the resource\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`RestApiId`  
The ID of the `RestApi` resource in which you want to create this resource\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

## Return Value<a name="w3ab2c21c10c72c11"></a>

### Ref<a name="w3ab2c21c10c72c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource ID, such as `abc123`\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10c72c13"></a>

The following example creates a `stack` resource for the `MyApi` API\.

### JSON<a name="aws-resource-apigateway-resource-example.json"></a>

```
"Stack": {
  "Type": "AWS::ApiGateway::Resource",
  "Properties": {
    "RestApiId": { "Ref": "MyApi" },
    "ParentId": { "Fn::GetAtt": ["MyApi", "RootResourceId"] },
    "PathPart": "stack"
  }
}
```

### YAML<a name="aws-resource-apigateway-resource-example.yaml"></a>

```
Stack: 
  Type: "AWS::ApiGateway::Resource"
  Properties: 
    RestApiId: 
      Ref: "MyApi"
    ParentId: 
      Fn::GetAtt: 
        - "MyApi"
        - "RootResourceId"
    PathPart: "stack"
```