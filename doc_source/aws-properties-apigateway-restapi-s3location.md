# AWS::ApiGateway::RestApi S3Location<a name="aws-properties-apigateway-restapi-s3location"></a>

`S3Location` is a property of the [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html) resource that specifies the Amazon S3 location of a OpenAPI \(formerly Swagger\) file that defines a set of RESTful APIs in JSON or YAML\.

**Note**  
On January 1, 2016, the Swagger Specification was donated to the [OpenAPI initiative](https://www.openapis.org/), becoming the foundation of the OpenAPI Specification\.

## Syntax<a name="aws-properties-apigateway-restapi-s3location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-restapi-s3location-syntax.json"></a>

```
{
  "[Bucket](#cfn-apigateway-restapi-s3location-bucket)" : String,
  "[ETag](#cfn-apigateway-restapi-s3location-etag)" : String,
  "[Key](#cfn-apigateway-restapi-s3location-key)" : String,
  "[Version](#cfn-apigateway-restapi-s3location-version)" : String
}
```

### YAML<a name="aws-properties-apigateway-restapi-s3location-syntax.yaml"></a>

```
  [Bucket](#cfn-apigateway-restapi-s3location-bucket): String
  [ETag](#cfn-apigateway-restapi-s3location-etag): String
  [Key](#cfn-apigateway-restapi-s3location-key): String
  [Version](#cfn-apigateway-restapi-s3location-version): String
```

## Properties<a name="aws-properties-apigateway-restapi-s3location-properties"></a>

`Bucket`  <a name="cfn-apigateway-restapi-s3location-bucket"></a>
The name of the S3 bucket where the OpenAPI file is stored\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ETag`  <a name="cfn-apigateway-restapi-s3location-etag"></a>
The Amazon S3 ETag \(a file checksum\) of the OpenAPI file\. If you don't specify a value, API Gateway skips ETag validation of your OpenAPI file\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-apigateway-restapi-s3location-key"></a>
The file name of the OpenAPI file \(Amazon S3 object name\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-apigateway-restapi-s3location-version"></a>
For versioning\-enabled buckets, a specific version of the OpenAPI file\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-restapi-s3location--seealso"></a>
+ [RestApi](https://docs.aws.amazon.com/apigateway/api-reference/resource/rest-api/) in the *Amazon API Gateway REST API Reference*

