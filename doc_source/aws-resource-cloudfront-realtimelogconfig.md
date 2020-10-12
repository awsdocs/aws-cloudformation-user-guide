# AWS::CloudFront::RealtimeLogConfig<a name="aws-resource-cloudfront-realtimelogconfig"></a>

A real\-time log configuration\.

## Syntax<a name="aws-resource-cloudfront-realtimelogconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-realtimelogconfig-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::RealtimeLogConfig",
  "Properties" : {
      "[EndPoints](#cfn-cloudfront-realtimelogconfig-endpoints)" : [ EndPoint, ... ],
      "[Fields](#cfn-cloudfront-realtimelogconfig-fields)" : [ String, ... ],
      "[Name](#cfn-cloudfront-realtimelogconfig-name)" : String,
      "[SamplingRate](#cfn-cloudfront-realtimelogconfig-samplingrate)" : Double
    }
}
```

### YAML<a name="aws-resource-cloudfront-realtimelogconfig-syntax.yaml"></a>

```
Type: AWS::CloudFront::RealtimeLogConfig
Properties: 
  [EndPoints](#cfn-cloudfront-realtimelogconfig-endpoints): 
    - EndPoint
  [Fields](#cfn-cloudfront-realtimelogconfig-fields): 
    - String
  [Name](#cfn-cloudfront-realtimelogconfig-name): String
  [SamplingRate](#cfn-cloudfront-realtimelogconfig-samplingrate): Double
```

## Properties<a name="aws-resource-cloudfront-realtimelogconfig-properties"></a>

`EndPoints`  <a name="cfn-cloudfront-realtimelogconfig-endpoints"></a>
Contains information about the Amazon Kinesis data stream where you are sending real\-time log data for this real\-time log configuration\.  
*Required*: Yes  
*Type*: List of [EndPoint](aws-properties-cloudfront-realtimelogconfig-endpoint.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Fields`  <a name="cfn-cloudfront-realtimelogconfig-fields"></a>
A list of fields that are included in each real\-time log record\. In an API response, the fields are provided in the same order in which they are sent to the Amazon Kinesis data stream\.  
For more information about fields, see [Real\-time log configuration fields](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/real-time-logs.html#understand-real-time-log-config-fields) in the *Amazon CloudFront Developer Guide*\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudfront-realtimelogconfig-name"></a>
The unique name of this real\-time log configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SamplingRate`  <a name="cfn-cloudfront-realtimelogconfig-samplingrate"></a>
The sampling rate for this real\-time log configuration\. The sampling rate determines the percentage of viewer requests that are represented in the real\-time log data\. The sampling rate is an integer between 1 and 100, inclusive\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudfront-realtimelogconfig-return-values"></a>

### Ref<a name="aws-resource-cloudfront-realtimelogconfig-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the real\-time log configuration\. For example: `arn:aws:cloudfront::111122223333:realtime-log-config/ExampleNameForRealtimeLogConfig`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudfront-realtimelogconfig-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudfront-realtimelogconfig-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 The Amazon Resource Name \(ARN\) of the real\-time log configuration\. For example: `arn:aws:cloudfront::111122223333:realtime-log-config/ExampleNameForRealtimeLogConfig`\.