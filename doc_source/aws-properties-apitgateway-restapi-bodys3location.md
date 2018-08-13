# Amazon API Gateway RestApi S3Location<a name="aws-properties-apitgateway-restapi-bodys3location"></a>

`S3Location` is a property of the [AWS::ApiGateway::RestApi](aws-resource-apigateway-restapi.md) resource that specifies the Amazon Simple Storage Service \(Amazon S3\) location of a OpenAPI \(formerly Swagger\) file that defines a set of RESTful APIs in JSON or YAML for an Amazon API Gateway \(API Gateway\) RestApi\.

**Note**  
On January 1, 2016, the Swagger Specification was donated to the [OpenAPI initiative](https://www.openapis.org/), becoming the foundation of the OpenAPI Specification\.

## Syntax<a name="w3ab2c21c14c33b7"></a>

### JSON<a name="aws-properties-apitgateway-restapi-bodys3location-syntax.json"></a>

```
{
  "[Bucket](#cfn-apigateway-restapi-s3location-bucket)" : String,
  "[ETag](#cfn-apigateway-restapi-s3location-etag)" : String,
  "[Key](#cfn-apigateway-restapi-s3location-key)" : String,
  "[Version](#cfn-apigateway-restapi-s3location-version)" : String
}
```

### YAML<a name="aws-properties-apitgateway-restapi-bodys3location-syntax.yaml"></a>

```
[Bucket](#cfn-apigateway-restapi-s3location-bucket): String
[ETag](#cfn-apigateway-restapi-s3location-etag): String
[Key](#cfn-apigateway-restapi-s3location-key): String
[Version](#cfn-apigateway-restapi-s3location-version): String
```

## Properties<a name="w3ab2c21c14c33b9"></a>

`Bucket`  <a name="cfn-apigateway-restapi-s3location-bucket"></a>
The name of the S3 bucket where the OpenAPI file is stored\.  
*Required*: No  
*Type*: String

`ETag`  <a name="cfn-apigateway-restapi-s3location-etag"></a>
The Amazon S3 ETag \(a file checksum\) of the OpenAPI file\. If you don't specify a value, API Gateway skips ETag validation of your OpenAPI file\.  
*Required*: No  
*Type*: String

`Key`  <a name="cfn-apigateway-restapi-s3location-key"></a>
The file name of the OpenAPI file \(Amazon S3 object name\)\.  
*Required*: No  
*Type*: String

`Version`  <a name="cfn-apigateway-restapi-s3location-version"></a>
For versioning\-enabled buckets, a specific version of the OpenAPI file\.  
*Required*: No  
*Type*: String