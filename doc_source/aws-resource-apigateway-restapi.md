# AWS::ApiGateway::RestApi<a name="aws-resource-apigateway-restapi"></a>

The `AWS::ApiGateway::RestApi` resource creates a REST API\. For more information, see [restapi:create](https://docs.aws.amazon.com/apigateway/latest/api/API_CreateRestApi.html) in the *Amazon API Gateway REST API Reference*\.

**Note**  
On January 1, 2016, the Swagger Specification was donated to the [OpenAPI initiative](https://www.openapis.org/), becoming the foundation of the OpenAPI Specification\.

## Syntax<a name="aws-resource-apigateway-restapi-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-restapi-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::RestApi",
  "Properties" : {
      "[ApiKeySourceType](#cfn-apigateway-restapi-apikeysourcetype)" : String,
      "[BinaryMediaTypes](#cfn-apigateway-restapi-binarymediatypes)" : [ String, ... ],
      "[Body](#cfn-apigateway-restapi-body)" : Json,
      "[BodyS3Location](#cfn-apigateway-restapi-bodys3location)" : S3Location,
      "[CloneFrom](#cfn-apigateway-restapi-clonefrom)" : String,
      "[Description](#cfn-apigateway-restapi-description)" : String,
      "[DisableExecuteApiEndpoint](#cfn-apigateway-restapi-disableexecuteapiendpoint)" : Boolean,
      "[EndpointConfiguration](#cfn-apigateway-restapi-endpointconfiguration)" : EndpointConfiguration,
      "[FailOnWarnings](#cfn-apigateway-restapi-failonwarnings)" : Boolean,
      "[MinimumCompressionSize](#cfn-apigateway-restapi-minimumcompressionsize)" : Integer,
      "[Mode](#cfn-apigateway-restapi-mode)" : String,
      "[Name](#cfn-apigateway-restapi-name)" : String,
      "[Parameters](#cfn-apigateway-restapi-parameters)" : {Key : Value, ...},
      "[Policy](#cfn-apigateway-restapi-policy)" : Json,
      "[Tags](#cfn-apigateway-restapi-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-apigateway-restapi-syntax.yaml"></a>

```
Type: AWS::ApiGateway::RestApi
Properties: 
  [ApiKeySourceType](#cfn-apigateway-restapi-apikeysourcetype): String
  [BinaryMediaTypes](#cfn-apigateway-restapi-binarymediatypes): 
    - String
  [Body](#cfn-apigateway-restapi-body): Json
  [BodyS3Location](#cfn-apigateway-restapi-bodys3location): 
    S3Location
  [CloneFrom](#cfn-apigateway-restapi-clonefrom): String
  [Description](#cfn-apigateway-restapi-description): String
  [DisableExecuteApiEndpoint](#cfn-apigateway-restapi-disableexecuteapiendpoint): Boolean
  [EndpointConfiguration](#cfn-apigateway-restapi-endpointconfiguration): 
    EndpointConfiguration
  [FailOnWarnings](#cfn-apigateway-restapi-failonwarnings): Boolean
  [MinimumCompressionSize](#cfn-apigateway-restapi-minimumcompressionsize): Integer
  [Mode](#cfn-apigateway-restapi-mode): String
  [Name](#cfn-apigateway-restapi-name): String
  [Parameters](#cfn-apigateway-restapi-parameters): 
    Key : Value
  [Policy](#cfn-apigateway-restapi-policy): Json
  [Tags](#cfn-apigateway-restapi-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-apigateway-restapi-properties"></a>

`ApiKeySourceType`  <a name="cfn-apigateway-restapi-apikeysourcetype"></a>
The source of the API key for metering requests according to a usage plan\. Valid values are: `HEADER` to read the API key from the `X-API-Key` header of a request\. `AUTHORIZER` to read the API key from the `UsageIdentifierKey` from a custom authorizer\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BinaryMediaTypes`  <a name="cfn-apigateway-restapi-binarymediatypes"></a>
The list of binary media types supported by the RestApi\. By default, the RestApi supports only UTF\-8\-encoded text payloads\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Body`  <a name="cfn-apigateway-restapi-body"></a>
An OpenAPI specification that defines a set of RESTful APIs in JSON format\. For YAML templates, you can also provide the specification in YAML format\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BodyS3Location`  <a name="cfn-apigateway-restapi-bodys3location"></a>
The Amazon Simple Storage Service \(Amazon S3\) location that points to an OpenAPI file, which defines a set of RESTful APIs in JSON or YAML format\.  
*Required*: No  
*Type*: [S3Location](aws-properties-apigateway-restapi-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloneFrom`  <a name="cfn-apigateway-restapi-clonefrom"></a>
The ID of the RestApi that you want to clone from\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigateway-restapi-description"></a>
The description of the RestApi\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableExecuteApiEndpoint`  <a name="cfn-apigateway-restapi-disableexecuteapiendpoint"></a>
Specifies whether clients can invoke your API by using the default `execute-api` endpoint\. By default, clients can invoke your API with the default `https://{api_id}.execute-api.{region}.amazonaws.com` endpoint\. To require that clients use a custom domain name to invoke your API, disable the default endpoint  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointConfiguration`  <a name="cfn-apigateway-restapi-endpointconfiguration"></a>
A list of the endpoint types of the API\. Use this property when creating an API\. When importing an existing API, specify the endpoint configuration types using the `Parameters` property\.  
*Required*: No  
*Type*: [EndpointConfiguration](aws-properties-apigateway-restapi-endpointconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailOnWarnings`  <a name="cfn-apigateway-restapi-failonwarnings"></a>
A query parameter to indicate whether to rollback the API update \(`true`\) or not \(`false`\) when a warning is encountered\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumCompressionSize`  <a name="cfn-apigateway-restapi-minimumcompressionsize"></a>
A nullable integer that is used to enable compression \(with non\-negative between 0 and 10485760 \(10M\) bytes, inclusive\) or disable compression \(with a null value\) on an API\. When compression is enabled, compression or decompression is not applied on the payload if the payload size is smaller than this value\. Setting it to zero allows compression for any payload size\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-apigateway-restapi-mode"></a>
This property applies only when you use OpenAPI to define your REST API\. The `Mode` determines how API Gateway handles resource updates\.  
Valid values are `overwrite` or `merge`\.   
For `overwrite`, the new API definition replaces the existing one\. The existing API identifier remains unchanged\.  
 For `merge`, the new API definition takes precedence, but any container types such as endpoint configurations and binary media types are merged with the existing API\. Use `merge` to define top\-level `RestApi` properties in addition to using OpenAPI\. Generally, it's preferred to use API Gateway's OpenAPI extensions to model these properties\.  
If you don't specify this property, a default value is chosen\. For REST APIs created before March 29, 2021, the default is `overwrite`\. Otherwise, the default value is `merge`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-apigateway-restapi-name"></a>
The name of the RestApi\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-apigateway-restapi-parameters"></a>
Custom header parameters as part of the request\. For example, to exclude DocumentationParts from an imported API, set `ignore=documentation` as a `parameters` value, as in the AWS CLI command of `aws apigateway import-rest-api --parameters ignore=documentation --body 'file:///path/to/imported-api-body.json'`\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policy`  <a name="cfn-apigateway-restapi-policy"></a>
A policy document that contains the permissions for the `RestApi` resource\. To set the ARN for the policy, use the `!Join` intrinsic function with `""` as delimiter and values of `"execute-api:/"` and `"*"`\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-apigateway-restapi-tags"></a>
The key\-value map of strings\. The valid character set is \[a\-zA\-Z\+\-=\.\_:/\]\. The tag key can be up to 128 characters and must not start with `aws:`\. The tag value can be up to 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-restapi-return-values"></a>

### Ref<a name="aws-resource-apigateway-restapi-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `RestApi` ID, such as `a1bcdef2gh`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apigateway-restapi-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apigateway-restapi-return-values-fn--getatt-fn--getatt"></a>

`RestApiId`  <a name="RestApiId-fn::getatt"></a>
The string identifier of the associated RestApi\.

`RootResourceId`  <a name="RootResourceId-fn::getatt"></a>
The root resource ID for a `RestApi` resource, such as `a0bc123d4e`\.

## Examples<a name="aws-resource-apigateway-restapi--examples"></a>



### Based on OpenAPI specification<a name="aws-resource-apigateway-restapi--examples--Based_on_OpenAPI_specification"></a>

The following example creates an API Gateway RestApi resource based on an OpenAPI specification\.

#### JSON<a name="aws-resource-apigateway-restapi--examples--Based_on_OpenAPI_specification--json"></a>

```
{
    "MyRestApi": {
        "Type": "AWS::ApiGateway::RestApi",
        "Properties": {
            "Body": {
                "OpenAPI specification": null
            },
            "Description": "A test API",
            "Name": "MyRestAPI"
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-restapi--examples--Based_on_OpenAPI_specification--yaml"></a>

```
MyRestApi:
  Type: 'AWS::ApiGateway::RestApi'
  Properties:
    Body:
      OpenAPI specification: null
    Description: A test API
    Name: MyRestAPI
```

### With endpoint type<a name="aws-resource-apigateway-restapi--examples--With_endpoint_type"></a>

The following example creates an API Gateway RestApi resource with an endpoint type\.

#### JSON<a name="aws-resource-apigateway-restapi--examples--With_endpoint_type--json"></a>

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

#### YAML<a name="aws-resource-apigateway-restapi--examples--With_endpoint_type--yaml"></a>

```
Parameters:
  apiName:
    Type: String
  type:
    Type: String
Resources:
  MyRestApi:
    Type: AWS::ApiGateway::RestApi
    Properties:
      EndpointConfiguration:
        Types:
          - !Ref type
      Name: !Ref apiName
```

### With REGIONAL endpoint type<a name="aws-resource-apigateway-restapi--examples--With_REGIONAL_endpoint_type"></a>

The following example imports an API Gateway RestApi resource with an endpoint type of REGIONAL\.

#### JSON<a name="aws-resource-apigateway-restapi--examples--With_REGIONAL_endpoint_type--json"></a>

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

#### YAML<a name="aws-resource-apigateway-restapi--examples--With_REGIONAL_endpoint_type--yaml"></a>

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

### With ApiKeySourceType<a name="aws-resource-apigateway-restapi--examples--With_ApiKeySourceType"></a>

The following example creates an API Gateway RestApi resource with ApiKeySourceType, BinaryMediaTypes and MinimumCompressionSize\.

#### JSON<a name="aws-resource-apigateway-restapi--examples--With_ApiKeySourceType--json"></a>

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

#### YAML<a name="aws-resource-apigateway-restapi--examples--With_ApiKeySourceType--yaml"></a>

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

## See also<a name="aws-resource-apigateway-restapi--seealso"></a>
+ [restapi:create](https://docs.aws.amazon.com/apigateway/latest/api/API_CreateRestApi.html) in the *Amazon API Gateway REST API Reference*
+ [Tutorial: Building a private REST API](https://docs.aws.amazon.com/apigateway/latest/developerguide/private-api-tutorial.html) in the *API Gateway Developer Guide*

