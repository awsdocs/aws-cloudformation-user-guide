# AWS::MediaConnect::FlowSource<a name="aws-resource-mediaconnect-flowsource"></a>

The AWS::MediaConnect::FlowSource resource is used to add additional sources to an existing flow\. Adding an additional source requires Failover to be enabled\. When you enable Failover, the additional source must use the same protocol as the existing source\. A source is the external video content that includes configuration information \(encryption and source type\) and a network address\. Each flow has at least one source\. A standard source comes from a source other than another AWS Elemental MediaConnect flow, such as an on\-premises encoder\.

## Syntax<a name="aws-resource-mediaconnect-flowsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconnect-flowsource-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConnect::FlowSource",
  "Properties" : {
      "[Decryption](#cfn-mediaconnect-flowsource-decryption)" : Encryption,
      "[Description](#cfn-mediaconnect-flowsource-description)" : String,
      "[EntitlementArn](#cfn-mediaconnect-flowsource-entitlementarn)" : String,
      "[FlowArn](#cfn-mediaconnect-flowsource-flowarn)" : String,
      "[IngestPort](#cfn-mediaconnect-flowsource-ingestport)" : Integer,
      "[MaxBitrate](#cfn-mediaconnect-flowsource-maxbitrate)" : Integer,
      "[MaxLatency](#cfn-mediaconnect-flowsource-maxlatency)" : Integer,
      "[Name](#cfn-mediaconnect-flowsource-name)" : String,
      "[Protocol](#cfn-mediaconnect-flowsource-protocol)" : String,
      "[StreamId](#cfn-mediaconnect-flowsource-streamid)" : String,
      "[VpcInterfaceName](#cfn-mediaconnect-flowsource-vpcinterfacename)" : String,
      "[WhitelistCidr](#cfn-mediaconnect-flowsource-whitelistcidr)" : String
    }
}
```

### YAML<a name="aws-resource-mediaconnect-flowsource-syntax.yaml"></a>

```
Type: AWS::MediaConnect::FlowSource
Properties: 
  [Decryption](#cfn-mediaconnect-flowsource-decryption): 
    Encryption
  [Description](#cfn-mediaconnect-flowsource-description): String
  [EntitlementArn](#cfn-mediaconnect-flowsource-entitlementarn): String
  [FlowArn](#cfn-mediaconnect-flowsource-flowarn): String
  [IngestPort](#cfn-mediaconnect-flowsource-ingestport): Integer
  [MaxBitrate](#cfn-mediaconnect-flowsource-maxbitrate): Integer
  [MaxLatency](#cfn-mediaconnect-flowsource-maxlatency): Integer
  [Name](#cfn-mediaconnect-flowsource-name): String
  [Protocol](#cfn-mediaconnect-flowsource-protocol): String
  [StreamId](#cfn-mediaconnect-flowsource-streamid): String
  [VpcInterfaceName](#cfn-mediaconnect-flowsource-vpcinterfacename): String
  [WhitelistCidr](#cfn-mediaconnect-flowsource-whitelistcidr): String
```

## Properties<a name="aws-resource-mediaconnect-flowsource-properties"></a>

`Decryption`  <a name="cfn-mediaconnect-flowsource-decryption"></a>
The type of encryption that is used on the content ingested from the source\.  
*Required*: No  
*Type*: [Encryption](aws-properties-mediaconnect-flowsource-encryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-mediaconnect-flowsource-description"></a>
A description of the source\. This description is not visible outside of the current AWS account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntitlementArn`  <a name="cfn-mediaconnect-flowsource-entitlementarn"></a>
The ARN of the entitlement that allows you to subscribe to the flow\. The entitlement is set by the content originator, and the ARN is generated as part of the originator's flow\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlowArn`  <a name="cfn-mediaconnect-flowsource-flowarn"></a>
The Amazon Resource Name \(ARN\) of the flow this source is connected to\. The flow must have Failover enabled to add an additional source\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngestPort`  <a name="cfn-mediaconnect-flowsource-ingestport"></a>
The port that the flow listens on for incoming content\. If the protocol of the source is Zixi, the port must be set to 2088\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxBitrate`  <a name="cfn-mediaconnect-flowsource-maxbitrate"></a>
The maximum bitrate for RIST, RTP, and RTP\-FEC streams\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxLatency`  <a name="cfn-mediaconnect-flowsource-maxlatency"></a>
The maximum latency in milliseconds\. This parameter applies only to RIST\-based, Zixi\-based, and Fujitsu\-based streams\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconnect-flowsource-name"></a>
The name of the source\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-mediaconnect-flowsource-protocol"></a>
The protocol that the source uses to deliver the content to MediaConnect\. Adding additional sources to an existing flow requires Failover to be enabled\. When you enable Failover, the additional source must use the same protocol as the existing source\. Only the following protocols support failover: Zixi\-push, RTP\-FEC, RTP, and RIST\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamId`  <a name="cfn-mediaconnect-flowsource-streamid"></a>
The stream ID that you want to use for this transport\. This parameter applies only to Zixi and SRT caller\-based streams\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcInterfaceName`  <a name="cfn-mediaconnect-flowsource-vpcinterfacename"></a>
The name of the VPC interface that you want to send your output to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WhitelistCidr`  <a name="cfn-mediaconnect-flowsource-whitelistcidr"></a>
The range of IP addresses that are allowed to contribute content to your source\. Format the IP addresses as a Classless Inter\-Domain Routing \(CIDR\) block; for example, 10\.0\.0\.0/16\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediaconnect-flowsource-return-values"></a>

### Ref<a name="aws-resource-mediaconnect-flowsource-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the source ARN\. For example:

`{ "Ref": "arn:aws:mediaconnect:us-east-1:111122223333:source:2-3aBC45dEF67hiJ89-c34de5fG678h:AwardsShowSource" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediaconnect-flowsource-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-mediaconnect-flowsource-return-values-fn--getatt-fn--getatt"></a>

`IngestIp`  <a name="IngestIp-fn::getatt"></a>
The IP address that the flow listens on for incoming content\.

`SourceArn`  <a name="SourceArn-fn::getatt"></a>
The ARN of the source\.

`SourceIngestPort`  <a name="SourceIngestPort-fn::getatt"></a>
Property description not available\.