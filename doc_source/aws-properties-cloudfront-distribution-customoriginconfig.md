# CloudFront Distribution CustomOriginConfig<a name="aws-properties-cloudfront-distribution-customoriginconfig"></a>

`CustomOriginConfig` is a property of the [Amazon CloudFront Origin](aws-properties-cloudfront-distribution-origin.md) property that describes an HTTP server\.

## Syntax<a name="w3ab2c21c14d257b5"></a>

### JSON<a name="aws-properties-cloudfront-distribution-customoriginconfig-syntax.json"></a>

```
{
  "[HTTPPort](#cfn-cloudfront-distribution-customoriginconfig-httpport)" : Integer,
  "[HTTPSPort](#cfn-cloudfront-distribution-customoriginconfig-httpsport)" : Integer,
  "[OriginKeepaliveTimeout](#cfn-cloudfront-distribution-customoriginconfig-originkeepalivetimeout)" : Integer,
  "[OriginProtocolPolicy](#cfn-cloudfront-distribution-customoriginconfig-originprotocolpolicy)" : String,
  "[OriginReadTimeout](#cfn-cloudfront-distribution-customoriginconfig-originreadtimeout)" : Integer,
  "[OriginSSLProtocols](#cfn-cloudfront-distribution-customoriginconfig-originsslprotocols)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-distribution-customoriginconfig-syntax.yaml"></a>

```
[HTTPPort](#cfn-cloudfront-distribution-customoriginconfig-httpport): Integer
[HTTPSPort](#cfn-cloudfront-distribution-customoriginconfig-httpsport): Integer
[OriginKeepaliveTimeout](#cfn-cloudfront-distribution-customoriginconfig-originkeepalivetimeout): Integer
[OriginProtocolPolicy](#cfn-cloudfront-distribution-customoriginconfig-originprotocolpolicy): String
[OriginReadTimeout](#cfn-cloudfront-distribution-customoriginconfig-originreadtimeout): Integer
[OriginSSLProtocols](#cfn-cloudfront-distribution-customoriginconfig-originsslprotocols):
  - String
```

## Properties<a name="w3ab2c21c14d257b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [CustomOriginConfig](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CustomOriginConfig.html) data type in the *Amazon CloudFront API Reference*\.

`HTTPPort`  <a name="cfn-cloudfront-distribution-customoriginconfig-httpport"></a>
The HTTP port the custom origin listens on\.  
*Required*: No  
*Type*: Integer

`HTTPSPort`  <a name="cfn-cloudfront-distribution-customoriginconfig-httpsport"></a>
The HTTPS port the custom origin listens on\.  
*Required*: No  
*Type*: Integer

`OriginKeepaliveTimeout`  <a name="cfn-cloudfront-distribution-customoriginconfig-originkeepalivetimeout"></a>
You can create a custom keep\-alive timeout\. All timeout units are in seconds\. The default keep\-alive timeout is 5 seconds, but you can configure custom timeout lengths\. The minimum timeout length is 1 second; the maximum is 60 seconds\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OriginProtocolPolicy`  <a name="cfn-cloudfront-distribution-customoriginconfig-originprotocolpolicy"></a>
The origin protocol policy to apply to your origin\.  
*Required*: Yes  
*Type*: String  
*Valid Values*: `http-only`, ` match-viewer`, `https-only`

`OriginReadTimeout`  <a name="cfn-cloudfront-distribution-customoriginconfig-originreadtimeout"></a>
You can create a custom origin read timeout\. All timeout units are in seconds\. The default origin read timeout is 30 seconds, but you can configure custom timeout lengths\. The minimum timeout length is 4 seconds; the maximum is 60 seconds\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OriginSSLProtocols`  <a name="cfn-cloudfront-distribution-customoriginconfig-originsslprotocols"></a>
The SSL protocols that CloudFront can use when establishing an HTTPS connection with your origin\. By default, AWS CloudFormation specifies the `TLSv1` and `SSLv3` protocols\.  
*Required*: No  
*Type*: List of String values