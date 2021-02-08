# AWS::CloudFront::Distribution CustomOriginConfig<a name="aws-properties-cloudfront-distribution-customoriginconfig"></a>

A custom origin\. A custom origin is any origin that is *not* an Amazon S3 bucket, with one exception\. An Amazon S3 bucket that is [configured with static website hosting](https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html) *is* a custom origin\.

## Syntax<a name="aws-properties-cloudfront-distribution-customoriginconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-cloudfront-distribution-customoriginconfig-properties"></a>

`HTTPPort`  <a name="cfn-cloudfront-distribution-customoriginconfig-httpport"></a>
The HTTP port that CloudFront uses to connect to the origin\. Specify the HTTP port that the origin listens on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HTTPSPort`  <a name="cfn-cloudfront-distribution-customoriginconfig-httpsport"></a>
The HTTPS port that CloudFront uses to connect to the origin\. Specify the HTTPS port that the origin listens on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginKeepaliveTimeout`  <a name="cfn-cloudfront-distribution-customoriginconfig-originkeepalivetimeout"></a>
Specifies how long, in seconds, CloudFront persists its connection to the origin\. The minimum timeout is 1 second, the maximum is 60 seconds, and the default \(if you don’t specify otherwise\) is 5 seconds\.  
For more information, see [Origin Keep\-alive Timeout](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#DownloadDistValuesOriginKeepaliveTimeout) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginProtocolPolicy`  <a name="cfn-cloudfront-distribution-customoriginconfig-originprotocolpolicy"></a>
Specifies the protocol \(HTTP or HTTPS\) that CloudFront uses to connect to the origin\. Valid values are:  
+  `http-only` – CloudFront always uses HTTP to connect to the origin\.
+  `match-viewer` – CloudFront connects to the origin using the same protocol that the viewer used to connect to CloudFront\.
+  `https-only` – CloudFront always uses HTTPS to connect to the origin\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `http-only | https-only | match-viewer`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginReadTimeout`  <a name="cfn-cloudfront-distribution-customoriginconfig-originreadtimeout"></a>
Specifies how long, in seconds, CloudFront waits for a response from the origin\. This is also known as the *origin response timeout*\. The minimum timeout is 1 second, the maximum is 60 seconds, and the default \(if you don’t specify otherwise\) is 30 seconds\.  
For more information, see [Origin Response Timeout](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#DownloadDistValuesOriginResponseTimeout) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginSSLProtocols`  <a name="cfn-cloudfront-distribution-customoriginconfig-originsslprotocols"></a>
Specifies the minimum SSL/TLS protocol that CloudFront uses when connecting to your origin over HTTPS\. Valid values include `SSLv3`, `TLSv1`, `TLSv1.1`, and `TLSv1.2`\.  
For more information, see [Minimum Origin SSL Protocol](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#DownloadDistValuesOriginSSLProtocols) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-distribution-customoriginconfig--seealso"></a>
+  [CustomOriginConfig](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CustomOriginConfig.html) in the *Amazon CloudFront API Reference* 

