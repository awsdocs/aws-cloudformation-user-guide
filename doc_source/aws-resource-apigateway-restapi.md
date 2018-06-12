# AWS::ApiGateway::RestApi<a name="aws-resource-apigateway-restapi"></a>

The `AWS::ApiGateway::RestApi` resource contains a collection of Amazon API Gateway resources and methods that can be invoked through HTTPS endpoints\. For more information, see [restapi:create](http://docs.aws.amazon.com//apigateway/api-reference/link-relation/restapi-create/) in the *Amazon API Gateway REST API Reference*\.

**Note**  
On January 1, 2016, the Swagger Specification was donated to the [OpenAPI initiative](https://www.openapis.org/), becoming the foundation of the OpenAPI Specification\.

**Topics**
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
    "[ApiKeySourceType](#cfn-apigateway-restapi-apikeysourcetype)" : String,
    "[BinaryMediaTypes](#cfn-apigateway-restapi-binarymediatypes)" : [ String, ... ],
    "[Body](#cfn-apigateway-restapi-body)" : JSON object,
    "[BodyS3Location](#cfn-apigateway-restapi-bodys3location)" : [*S3Location*](aws-properties-apitgateway-restapi-bodys3location.md),
    "[CloneFrom](#cfn-apigateway-restapi-clonefrom)" : String,
    "[Description](#cfn-apigateway-restapi-description)" : String,      
    "[EndpointConfiguration](#cfn-apigateway-restapi-endpointconfiguration)" : [*EndpointConfiguration*](aws-properties-apigateway-restapi-endpointconfiguration.md),
    "[FailOnWarnings](#cfn-apigateway-restapi-failonwarning)" : Boolean,
    "[MinimumCompressionSize](#cfn-apigateway-restapi-minimumcompressionsize)" : Integer,
    "[Name](#cfn-apigateway-restapi-name)" : String,
    "[Parameters](#cfn-apigateway-restapi-parameters)" : { String:String, ... },
    "[Policy](#cfn-apigateway-restapi-policy)" : JSON object,
  }
}
```

### YAML<a name="aws-resource-apigateway-restapi-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::RestApi"
Properties:
  [ApiKeySourceType](#cfn-apigateway-restapi-apikeysourcetype): String
  [BinaryMediaTypes](#cfn-apigateway-restapi-binarymediatypes):
    - String
  [Body](#cfn-apigateway-restapi-body): JSON object
  [BodyS3Location](#cfn-apigateway-restapi-bodys3location):
    [*S3Location*](aws-properties-apitgateway-restapi-bodys3location.md)
  [CloneFrom](#cfn-apigateway-restapi-clonefrom): String
  [Description](#cfn-apigateway-restapi-description): String
  [EndpointConfiguration](#cfn-apigateway-restapi-endpointconfiguration): [*EndpointConfiguration*](aws-properties-apigateway-restapi-endpointconfiguration.md)
  [FailOnWarnings](#cfn-apigateway-restapi-failonwarning): Boolean
  [MinimumCompressionSize](#cfn-apigateway-restapi-minimumcompressionsize): Integer
  [Name](#cfn-apigateway-restapi-name): String
  [Parameters](#cfn-apigateway-restapi-parameters):
    String: String
 [Policy](#cfn-apigateway-restapi-policy): JSON object
```

## Properties<a name="w3ab2c21c10c76c11"></a>

`ApiKeySourceType`  <a name="cfn-apigateway-restapi-apikeysourcetype"></a>
The source of the API key for metering requests according to a usage plan\. Valid values are:  
+ `HEADER` to read the API key from the `X-API-Key` header of a request\.
+ `AUTHORIZER` to read the API key from the `UsageIdentifierKey` from a custom authorizer\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`BinaryMediaTypes`  <a name="cfn-apigateway-restapi-binarymediatypes"></a>
The list of binary media types that are supported by the `RestApi` resource, such as `image/png` or `application/octet-stream`\. By default, `RestApi` supports only UTF\-8\-encoded text payloads\. For more information, see [Enable Support for Binary Payloads in API Gateway](http://docs.aws.amazon.com//apigateway/latest/developerguide/api-gateway-payload-encodings.html) in the *API Gateway Developer Guide*\. Duplicates are not allowed\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Body`  <a name="cfn-apigateway-restapi-body"></a>
An OpenAPI specification that defines a set of RESTful APIs in the JSON format\. For YAML templates, you can also provide the specification in the YAML format\.  
*Required*: No  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`BodyS3Location`  <a name="cfn-apigateway-restapi-bodys3location"></a>
The Amazon Simple Storage Service \(Amazon S3\) location that points to an OpenAPI file, which defines a set of RESTful APIs in JSON or YAML format\.  
*Required*: No  
*Type*: [Amazon API Gateway RestApi S3Location](aws-properties-apitgateway-restapi-bodys3location.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CloneFrom`  <a name="cfn-apigateway-restapi-clonefrom"></a>
The ID of the API Gateway `RestApi` resource that you want to clone\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-apigateway-restapi-description"></a>
A description of the purpose of this API Gateway `RestApi` resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EndpointConfiguration`  <a name="cfn-apigateway-restapi-endpointconfiguration"></a>
A list of the endpoint types of the API\. Use this property when creating an API\. When importing an existing API, specify the endpoint configuration types using the `Parameters` property\.  
 *Required*: No  
 *Type*: [API Gateway RestApi EndpointConfiguration](aws-properties-apigateway-restapi-endpointconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`FailOnWarnings`  <a name="cfn-apigateway-restapi-failonwarning"></a>
Indicates whether to roll back the resource if a warning occurs while API Gateway is creating the `RestApi` resource\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MinimumCompressionSize`  <a name="cfn-apigateway-restapi-minimumcompressionsize"></a>
A nullable integer that is used to enable compression \(with non\-negative between 0 and 10485760 \(10M\) bytes, inclusive\) or disable compression \(with a null value\) on an API\. When compression is enabled, compression or decompression is not applied on the payload if the payload size is smaller than this value\. Setting it to zero allows compression for any payload size\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-apigateway-restapi-name"></a>
A name for the API Gateway `RestApi` resource\.  
*Required*: Conditional\. Required if you don't specify a OpenAPI definition\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Parameters`  <a name="cfn-apigateway-restapi-parameters"></a>
Custom header parameters for the request\.  
For more information on specifying parameters when importing an API, see [import\-rest\-api](http://docs.aws.amazon.com/cli/latest/reference/apigateway/import-rest-api.html) operation in the *AWS CLI Command Reference*\.  
*Required*: No  
*Type*: String to String map  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Policy`  <a name="cfn-apigateway-restapi-policy"></a>
A policy document that contains the permissions for this `RestApi` resource, in JSON format\.  
*Required*: No  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-apigateway-restapi-returnvalues"></a>

### Ref<a name="aws-resource-apigateway-restapi-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the `RestApi` ID, such as `a1bcdef2gh`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-apigateway-restapi-examplegetatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. This section lists the available attribute and a sample return value\.

`RootResourceId`  
The root resource ID for a `RestApi` resource, such as `a0bc123d4e`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

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

#### YAML<a name="aws-resource-apigateway-restapi-example.yaml"></a>

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

### <a name="aws-resource-apigateway-restapi-example3"></a>

The following example imports an API Gateway `RestApi` resource with an endpoint type of REGIONAL\.

#### JSON<a name="aws-resource-apigateway-restapi-example3.json"></a>

```
{
    "Resources": {
        "RestApi": {
            "Type": "AWS::ApiGateway::RestApi",
            "Properties": {
                "Body": {
                    "swagger": 2,
                    "info": {
                        "version": "0.0.1",
                        "title": "test"
                    },
                    "basePath": "/pete",
                    "schemes": [
                        "https"
                    ],
                    "definitions": {
                        "Empty": {
                            "type": "object"
                        }
                    }
                },
                "Name": "myApi",
                "Parameters": {
                    "endpointConfigurationTypes": "REGIONAL"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-restapi-example3.yaml"></a>

```
Resources :
    RestApi :
        Type : AWS::ApiGateway::RestApi
        Properties :
            Body :
                swagger : 2.0
                info :
                    version : 0.0.1
                    title : test
                basePath : /pete
                schemes :
                    - https
                definitions:
                    Empty :
                        type : object
            Name : myApi
            Parameters:
                endpointConfigurationTypes: REGIONAL
```

### <a name="aws-resource-apigateway-restapi-example4"></a>

The following example creates an API Gateway `RestApi` resource with ApiKeySourceType, BinaryMediaTypes and MinimumCompressionSize\.

#### JSON<a name="aws-resource-apigateway-restapi-example4.json"></a>

```
{
    "Parameters": {
        "apiKeySourceType": {
            "Type": "String"
        },
        "apiName": {
            "Type": "String"
        },
        "binaryMediaType1": {
            "Type": "String"
        },
        "binaryMediaType2": {
            "Type": "String"
        },
        "minimumCompressionSize": {
            "Type": "String"
        }
    },
    "Resources": {
        "MyRestApi": {
            "Type": "AWS::ApiGateway::RestApi",
            "Properties": {
                "ApiKeySourceType": {
                    "Ref": "apiKeySourceType"
                },
                "BinaryMediaTypes": [
                    {
                        "Ref": "binaryMediaType1"
                    },
                    {
                        "Ref": "binaryMediaType2"
                    }
                ],
                "MinimumCompressionSize": {
                    "Ref": "minimumCompressionSize"
                },
                "Name": {
                    "Ref": "apiName"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-restapi-example4.yaml"></a>

```
Parameters:
    apiKeySourceType:
        Type: String
    apiName:
        Type: String
    binaryMediaType1:
        Type: String
    binaryMediaType2:
        Type: String
    minimumCompressionSize:
        Type: String
Resources:
    MyRestApi:
        Type: AWS::ApiGateway::RestApi
        Properties:
            ApiKeySourceType: !Ref apiKeySourceType
            BinaryMediaTypes:
                - !Ref binaryMediaType1
                - !Ref binaryMediaType2
            MinimumCompressionSize: !Ref minimumCompressionSize
            Name: !Ref apiName
```

## See Also<a name="aws-resource-apigateway-restapi-seealso"></a>
+ [restapi:create](http://docs.aws.amazon.com/apigateway/api-reference/link-relation/restapi-create/) operation in the *Amazon API Gateway REST API Reference*
+ [import\-rest\-api](http://docs.aws.amazon.com/cli/latest/reference/apigateway/import-rest-api.html) operation in the *AWS CLI Command Reference*