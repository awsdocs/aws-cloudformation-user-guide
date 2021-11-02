# AWS::MediaConnect::Flow<a name="aws-resource-mediaconnect-flow"></a>

The AWS::MediaConnect::Flow resource defines a connection between one or more video sources and one or more outputs\. For each flow, you specify the transport protocol to use, encryption information, and details for any outputs or entitlements that you want\. AWS Elemental MediaConnect returns an ingest endpoint where you can send your live video as a single unicast stream\. The service replicates and distributes the video to every output that you specify, whether inside or outside the AWS Cloud\. You can also set up entitlements on a flow to allow other AWS accounts to access your content\. 

## Syntax<a name="aws-resource-mediaconnect-flow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconnect-flow-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConnect::Flow",
  "Properties" : {
      "[AvailabilityZone](#cfn-mediaconnect-flow-availabilityzone)" : String,
      "[Name](#cfn-mediaconnect-flow-name)" : String,
      "[Source](#cfn-mediaconnect-flow-source)" : Source,
      "[SourceFailoverConfig](#cfn-mediaconnect-flow-sourcefailoverconfig)" : FailoverConfig
    }
}
```

### YAML<a name="aws-resource-mediaconnect-flow-syntax.yaml"></a>

```
Type: AWS::MediaConnect::Flow
Properties: 
  [AvailabilityZone](#cfn-mediaconnect-flow-availabilityzone): String
  [Name](#cfn-mediaconnect-flow-name): String
  [Source](#cfn-mediaconnect-flow-source): 
    Source
  [SourceFailoverConfig](#cfn-mediaconnect-flow-sourcefailoverconfig): 
    FailoverConfig
```

## Properties<a name="aws-resource-mediaconnect-flow-properties"></a>

`AvailabilityZone`  <a name="cfn-mediaconnect-flow-availabilityzone"></a>
The Availability Zone that you want to create the flow in\. These options are limited to the Availability Zones within the current AWS Region\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-mediaconnect-flow-name"></a>
The name of the flow\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Source`  <a name="cfn-mediaconnect-flow-source"></a>
The settings for the source that you want to use for the new flow\.  
*Required*: Yes  
*Type*: [Source](aws-properties-mediaconnect-flow-source.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFailoverConfig`  <a name="cfn-mediaconnect-flow-sourcefailoverconfig"></a>
The settings for source failover\.  
*Required*: No  
*Type*: [FailoverConfig](aws-properties-mediaconnect-flow-failoverconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediaconnect-flow-return-values"></a>

### Ref<a name="aws-resource-mediaconnect-flow-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the flow ARN\. For example:

`{ "Ref": "arn:aws:mediaconnect:us-east-1:111122223333:flow:1-23aBC45dEF67hiJ8-12AbC34DE5fG:BasketballGame" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediaconnect-flow-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-mediaconnect-flow-return-values-fn--getatt-fn--getatt"></a>

`FlowArn`  <a name="FlowArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the flow\.

`FlowAvailabilityZone`  <a name="FlowAvailabilityZone-fn::getatt"></a>
The Availability Zone that the flow was created in\. These options are limited to the Availability Zones within the current AWS Region\.

`Source.IngestIp`  <a name="Source.IngestIp-fn::getatt"></a>
The IP address that the flow listens on for incoming content\.

`Source.SourceArn`  <a name="Source.SourceArn-fn::getatt"></a>
The ARN of the source\.

`Source.SourceIngestPort`  <a name="Source.SourceIngestPort-fn::getatt"></a>
The port that the flow will be listening on for incoming content\.