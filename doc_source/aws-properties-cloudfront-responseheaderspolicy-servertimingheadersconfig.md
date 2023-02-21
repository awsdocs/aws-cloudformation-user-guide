# AWS::CloudFront::ResponseHeadersPolicy ServerTimingHeadersConfig<a name="aws-properties-cloudfront-responseheaderspolicy-servertimingheadersconfig"></a>

A configuration for enabling the `Server-Timing` header in HTTP responses sent from CloudFront\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-servertimingheadersconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-servertimingheadersconfig-syntax.json"></a>

```
{
  "[Enabled](#cfn-cloudfront-responseheaderspolicy-servertimingheadersconfig-enabled)" : Boolean,
  "[SamplingRate](#cfn-cloudfront-responseheaderspolicy-servertimingheadersconfig-samplingrate)" : Double
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-servertimingheadersconfig-syntax.yaml"></a>

```
  [Enabled](#cfn-cloudfront-responseheaderspolicy-servertimingheadersconfig-enabled): Boolean
  [SamplingRate](#cfn-cloudfront-responseheaderspolicy-servertimingheadersconfig-samplingrate): Double
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-servertimingheadersconfig-properties"></a>

`Enabled`  <a name="cfn-cloudfront-responseheaderspolicy-servertimingheadersconfig-enabled"></a>
A Boolean that determines whether CloudFront adds the `Server-Timing` header to HTTP responses that it sends in response to requests that match a cache behavior that's associated with this response headers policy\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SamplingRate`  <a name="cfn-cloudfront-responseheaderspolicy-servertimingheadersconfig-samplingrate"></a>
A number 0–100 \(inclusive\) that specifies the percentage of responses that you want CloudFront to add the `Server-Timing` header to\. When you set the sampling rate to 100, CloudFront adds the `Server-Timing` header to the HTTP response for every request that matches the cache behavior that this response headers policy is attached to\. When you set it to 50, CloudFront adds the header to 50% of the responses for requests that match the cache behavior\. You can set the sampling rate to any number 0–100 with up to four decimal places\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)