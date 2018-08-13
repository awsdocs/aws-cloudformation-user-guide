# CloudFront Distribution CustomErrorResponse<a name="aws-properties-cloudfront-distribution-customerrorresponse"></a>

`CustomErrorResponse` is a property of the [CloudFront Distribution DistributionConfig](aws-properties-cloudfront-distribution-distributionconfig.md) resource that defines custom error messages for certain HTTP status codes\.

## Syntax<a name="w3ab2c21c14d252b5"></a>

### JSON<a name="aws-properties-cloudfront-distribution-customerrorresponse-syntax.json"></a>

```
{
  "[ErrorCachingMinTTL](#cfn-cloudfront-distribution-customerrorresponse-errorcachingminttl)" : Integer,
  "[ErrorCode](#cfn-cloudfront-distribution-customerrorresponse-errorcode)" : Integer,
  "[ResponseCode](#cfn-cloudfront-distribution-customerrorresponse-responsecode)" : Integer,
  "[ResponsePagePath](#cfn-cloudfront-distribution-customerrorresponse-responsepagepath)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-customerrorresponse-syntax.yaml"></a>

```
[ErrorCachingMinTTL](#cfn-cloudfront-distribution-customerrorresponse-errorcachingminttl): Integer
[ErrorCode](#cfn-cloudfront-distribution-customerrorresponse-errorcode): Integer
[ResponseCode](#cfn-cloudfront-distribution-customerrorresponse-responsecode): Integer
[ResponsePagePath](#cfn-cloudfront-distribution-customerrorresponse-responsepagepath): String
```

## Properties<a name="w3ab2c21c14d252b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [CustomErrorResponse](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CustomErrorResponse.html) data type in the *Amazon CloudFront API Reference*\.

`ErrorCachingMinTTL`  <a name="cfn-cloudfront-distribution-customerrorresponse-errorcachingminttl"></a>
The minimum amount of time, in seconds, that Amazon CloudFront caches the HTTP status code that you specified in the `ErrorCode` property\. The default value is `300`\.  
*Required*: No  
*Type*: Integer

`ErrorCode`  <a name="cfn-cloudfront-distribution-customerrorresponse-errorcode"></a>
An HTTP status code for which you want to specify a custom error page\. You can specify `400`, `403`, `404`, `405`, `414`, `500`, `501`, `502`, `503`, or `504`\.  
*Required*: Yes  
*Type*: Integer

`ResponseCode`  <a name="cfn-cloudfront-distribution-customerrorresponse-responsecode"></a>
The HTTP status code that CloudFront returns to viewer along with the custom error page\. You can specify `200`, `400`, `403`, `404`, `405`, `414`, `500`, `501`, `502`, `503`, or `504`\.  
*Required*: Conditional\. Required if you specified the `ResponsePagePath` property\.  
*Type*: Integer

`ResponsePagePath`  <a name="cfn-cloudfront-distribution-customerrorresponse-responsepagepath"></a>
The path to the custom error page that CloudFront returns to a viewer when your origin returns the HTTP status code that you specified in the `ErrorCode` property\. For example, you can specify `/404-errors/403-forbidden.html`\.  
*Required*: Conditional\. Required if you specified the `ResponseCode` property\.  
*Type*: String