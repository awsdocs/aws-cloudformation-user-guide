# AWS::ApiGateway::RestApi<a name="aws-resource-apigateway-restapi"></a>

The `AWS::ApiGateway::RestApi` resource contains a collection of Amazon API Gateway resources and methods that can be invoked through HTTPS endpoints\. For more information, see [restapi:create](http://docs.aws.amazon.com//apigateway/api-reference/link-relation/restapi-create/) in the *Amazon API Gateway REST API Reference*\.

**Note**  
On January 1, 2016, the Swagger Specification was donated to the [OpenAPI initiative](https://www.openapis.org/), becoming the foundation of the OpenAPI Specification\.


+ [Syntax](#aws-resource-apigateway-restapi-syntax)
+ [Properties](#w3ab2c21c10c76c11)
+ [Return Values](#aws-resource-apigateway-restapi-returnvalues)
+ [Examples](#aws-resource-apigateway-restapi-examples)
+ [See Also](#aws-resource-apigateway-restapi-seealso)

## Syntax<a name="aws-resource-apigateway-restapi-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-restapi-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::RestApi",
  "Properties" : {  
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-binarymediatypes)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-body)" : JSON object,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-bodys3location)" : S3Location,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-clonefrom)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-description)" : String,      
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-endpointconfiguration)" : EndpointConfiguration,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-failonwarning)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-parameters)" : { String:String, ... }
  }
}
```

### YAML<a name="aws-resource-apigateway-restapi-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::RestApi"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-binarymediatypes):
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-body): JSON object
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-bodys3location):
    S3Location
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-clonefrom): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-endpointconfiguration): EndpointConfiguration
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-failonwarning): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-restapi-parameters):
    String: String
```

## Properties<a name="w3ab2c21c10c76c11"></a>

`BinaryMediaTypes`  
The list of binary media types that are supported by the `RestApi` resource, such as `image/png` or `application/octet-stream`\. By default, `RestApi` supports only UTF\-8\-encoded text payloads\. For more information, see [Enable Support for Binary Payloads in API Gateway](http://docs.aws.amazon.com//apigateway/latest/developerguide/api-gateway-payload-encodings.html) in the *API Gateway Developer Guide*\. Duplicates are not allowed\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`Body`  
An OpenAPI specification that defines a set of RESTful APIs in the JSON format\. For YAML templates, you can also provide the specification in the YAML format\.  
*Required: *No  
*Type*: JSON object  
*Update requires*: No interruption

`BodyS3Location`  
The Amazon Simple Storage Service \(Amazon S3\) location that points to an OpenAPI file, which defines a set of RESTful APIs in JSON or YAML format\.  
*Required: *No  
*Type*: [Amazon API Gateway RestApi S3Location](aws-properties-apitgateway-restapi-bodys3location.md)  
*Update requires*: No interruption

`CloneFrom`  
The ID of the API Gateway `RestApi` resource that you want to clone\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Description`  
A description of the purpose of this API Gateway `RestApi` resource\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`EndpointConfiguration`  
A list of the endpoint types of the API\.  
 *Required*: No  
 *Type*: [API Gateway RestApi EndpointConfiguration](aws-properties-apigateway-restapi-endpointconfiguration.md)  
 *Update requires*: No interruption 

`FailOnWarnings`  
Indicates whether to roll back the resource if a warning occurs while API Gateway is creating the `RestApi` resource\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`Name`  
A name for the API Gateway `RestApi` resource\.  
*Required: *Conditional\. Required if you don't specify a OpenAPI definition\.  
*Type*: String  
*Update requires*: No interruption

`Parameters`  
Custom header parameters for the request\.  
*Required: *No  
*Type*: String to String map  
*Update requires*: No interruption

## Return Values<a name="aws-resource-apigateway-restapi-returnvalues"></a>

### Ref<a name="aws-resource-apigateway-restapi-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the `RestApi` ID, such as `a1bcdef2gh`\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="aws-resource-apigateway-restapi-examplegetatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. This section lists the available attribute and a sample return value\.

`RootResourceId`  
The root resource ID for a `RestApi` resource, such as `a0bc123d4e`\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Examples<a name="aws-resource-apigateway-restapi-examples"></a>

### <a name="aws-resource-apigateway-restapi-example1"></a>

The following example creates an API Gateway `RestApi` resource based on an OpenAPI specification\.

#### JSON<a name="aws-resource-apigateway-restapi-example1.json"></a>

```
"MyRestApi": {
  "Type": "AWS::ApiGateway::RestApi",
  "Properties": {
    "Body": {
      OpenAPI specification
    }
    "Description": "A test API",
    "Name": "MyRestAPI"
  }
}
```

#### YAML<a name="aws-resource-apigateway-restapi-example1.yaml"></a>

```
MyRestApi: 
  Type: "AWS::ApiGateway::RestApi"
  Properties:
    Body:
      OpenAPI specification    
    Description: "A test API"
    Name: "MyRestAPI"
```

### <a name="aws-resource-apigateway-restapi-example2"></a>

The following example creates an API Gateway `RestApi` resource with an endpoint type\.

#### JSON<a name="aws-resource-apigateway-restapi-example2.json"></a>

```
{
  "Parameters": {
    "apiName": {
      "Type": "String"
    },
    "type": {
      "Type": "String"
    }
  },
  "Resources": {
    "MyRestApi": {
      "Type": "AWS::ApiGateway::RestApi",
      "Properties": {
        "EndpointConfiguration": {
          "Types": [
            {
              "Ref": "type"
            }
          ]
        },
        "Name": {
          "Ref": "apiName"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-apigateway-restapi-exampl2e.yaml"></a>

```
Parameters:
  apiName:
    Type: String
  type:
    Type: String
Resources:
  MyRestApi:
    Type: 'AWS::ApiGateway::RestApi'
    Properties:
      EndpointConfiguration:
        Types:
          - !Ref type
      Name: !Ref apiName
```

## See Also<a name="aws-resource-apigateway-restapi-seealso"></a>

+ [restapi:create](http://docs.aws.amazon.com/apigateway/api-reference/link-relation/restapi-create/) operation in the *Amazon API Gateway REST API Reference*