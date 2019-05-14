# AWS::CloudFront::Distribution CustomOriginConfig<a name="aws-properties-cloudfront-distribution-customoriginconfig"></a>

A custom origin or an Amazon S3 bucket configured as a website endpoint\.

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
﻿  [HTTPPort](#cfn-cloudfront-distribution-customoriginconfig-httpport) : Integer
﻿  [HTTPSPort](#cfn-cloudfront-distribution-customoriginconfig-httpsport) : Integer
﻿  [OriginKeepaliveTimeout](#cfn-cloudfront-distribution-customoriginconfig-originkeepalivetimeout) : Integer
﻿  [OriginProtocolPolicy](#cfn-cloudfront-distribution-customoriginconfig-originprotocolpolicy) : String
﻿  [OriginReadTimeout](#cfn-cloudfront-distribution-customoriginconfig-originreadtimeout) : Integer
﻿  [OriginSSLProtocols](#cfn-cloudfront-distribution-customoriginconfig-originsslprotocols) : 
    - String
```

## Properties<a name="aws-properties-cloudfront-distribution-customoriginconfig-properties"></a>

`HTTPPort`  <a name="cfn-cloudfront-distribution-customoriginconfig-httpport"></a>
The HTTP port the custom origin listens on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HTTPSPort`  <a name="cfn-cloudfront-distribution-customoriginconfig-httpsport"></a>
The HTTPS port the custom origin listens on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginKeepaliveTimeout`  <a name="cfn-cloudfront-distribution-customoriginconfig-originkeepalivetimeout"></a>
You can create a custom keep\-alive timeout\. All timeout units are in seconds\. The default keep\-alive timeout is 5 seconds, but you can configure custom timeout lengths using the CloudFront API\. The minimum timeout length is 1 second; the maximum is 60 seconds\.  
If you need to increase the maximum time limit, contact the [AWS Support Center](https://console.aws.amazon.com/support/home#/)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginProtocolPolicy`  <a name="cfn-cloudfront-distribution-customoriginconfig-originprotocolpolicy"></a>
The origin protocol policy to apply to your origin\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `http-only | https-only | match-viewer`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginReadTimeout`  <a name="cfn-cloudfront-distribution-customoriginconfig-originreadtimeout"></a>
You can create a custom origin read timeout\. All timeout units are in seconds\. The default origin read timeout is 30 seconds, but you can configure custom timeout lengths using the CloudFront API\. The minimum timeout length is 4 seconds; the maximum is 60 seconds\.  
If you need to increase the maximum time limit, contact the [AWS Support Center](https://console.aws.amazon.com/support/home#/)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginSSLProtocols`  <a name="cfn-cloudfront-distribution-customoriginconfig-originsslprotocols"></a>
The SSL/TLS protocols that you want CloudFront to use when communicating with your origin over HTTPS\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-cloudfront-distribution-customoriginconfig--seealso"></a>
+  [CustomOriginConfig](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CustomOriginConfig.html) in the *Amazon CloudFront API Reference* 