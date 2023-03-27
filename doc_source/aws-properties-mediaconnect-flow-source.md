# AWS::MediaConnect::Flow Source<a name="aws-properties-mediaconnect-flow-source"></a>

The details of the sources of the flow\.

If you are creating a flow with a VPC source, you must first create the flow with a temporary standard source by doing the following:

1. Use CloudFormation to create a flow with a standard source that uses the flow’s public IP address\.

1. Use CloudFormation to create the VPC interface to add to this flow\. This can also be done as part of the previous step\.

1. After CloudFormation has created the flow and the VPC interface, update the source to point to the VPC interface that you created\.

## Syntax<a name="aws-properties-mediaconnect-flow-source-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-flow-source-syntax.json"></a>

```
{
  "[Decryption](#cfn-mediaconnect-flow-source-decryption)" : Encryption,
  "[Description](#cfn-mediaconnect-flow-source-description)" : String,
  "[EntitlementArn](#cfn-mediaconnect-flow-source-entitlementarn)" : String,
  "[IngestIp](#cfn-mediaconnect-flow-source-ingestip)" : String,
  "[IngestPort](#cfn-mediaconnect-flow-source-ingestport)" : Integer,
  "[MaxBitrate](#cfn-mediaconnect-flow-source-maxbitrate)" : Integer,
  "[MaxLatency](#cfn-mediaconnect-flow-source-maxlatency)" : Integer,
  "[MinLatency](#cfn-mediaconnect-flow-source-minlatency)" : Integer,
  "[Name](#cfn-mediaconnect-flow-source-name)" : String,
  "[Protocol](#cfn-mediaconnect-flow-source-protocol)" : String,
  "[SenderControlPort](#cfn-mediaconnect-flow-source-sendercontrolport)" : Integer,
  "[SenderIpAddress](#cfn-mediaconnect-flow-source-senderipaddress)" : String,
  "[SourceArn](#cfn-mediaconnect-flow-source-sourcearn)" : String,
  "[SourceIngestPort](#cfn-mediaconnect-flow-source-sourceingestport)" : String,
  "[SourceListenerAddress](#cfn-mediaconnect-flow-source-sourcelisteneraddress)" : String,
  "[SourceListenerPort](#cfn-mediaconnect-flow-source-sourcelistenerport)" : Integer,
  "[StreamId](#cfn-mediaconnect-flow-source-streamid)" : String,
  "[VpcInterfaceName](#cfn-mediaconnect-flow-source-vpcinterfacename)" : String,
  "[WhitelistCidr](#cfn-mediaconnect-flow-source-whitelistcidr)" : String
}
```

### YAML<a name="aws-properties-mediaconnect-flow-source-syntax.yaml"></a>

```
  [Decryption](#cfn-mediaconnect-flow-source-decryption): 
    Encryption
  [Description](#cfn-mediaconnect-flow-source-description): String
  [EntitlementArn](#cfn-mediaconnect-flow-source-entitlementarn): String
  [IngestIp](#cfn-mediaconnect-flow-source-ingestip): String
  [IngestPort](#cfn-mediaconnect-flow-source-ingestport): Integer
  [MaxBitrate](#cfn-mediaconnect-flow-source-maxbitrate): Integer
  [MaxLatency](#cfn-mediaconnect-flow-source-maxlatency): Integer
  [MinLatency](#cfn-mediaconnect-flow-source-minlatency): Integer
  [Name](#cfn-mediaconnect-flow-source-name): String
  [Protocol](#cfn-mediaconnect-flow-source-protocol): String
  [SenderControlPort](#cfn-mediaconnect-flow-source-sendercontrolport): Integer
  [SenderIpAddress](#cfn-mediaconnect-flow-source-senderipaddress): String
  [SourceArn](#cfn-mediaconnect-flow-source-sourcearn): String
  [SourceIngestPort](#cfn-mediaconnect-flow-source-sourceingestport): String
  [SourceListenerAddress](#cfn-mediaconnect-flow-source-sourcelisteneraddress): String
  [SourceListenerPort](#cfn-mediaconnect-flow-source-sourcelistenerport): Integer
  [StreamId](#cfn-mediaconnect-flow-source-streamid): String
  [VpcInterfaceName](#cfn-mediaconnect-flow-source-vpcinterfacename): String
  [WhitelistCidr](#cfn-mediaconnect-flow-source-whitelistcidr): String
```

## Properties<a name="aws-properties-mediaconnect-flow-source-properties"></a>

`Decryption`  <a name="cfn-mediaconnect-flow-source-decryption"></a>
The type of encryption that is used on the content ingested from the source\.  
*Required*: No  
*Type*: [Encryption](aws-properties-mediaconnect-flow-encryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-mediaconnect-flow-source-description"></a>
A description of the source\. This description is not visible outside of the current AWS account\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntitlementArn`  <a name="cfn-mediaconnect-flow-source-entitlementarn"></a>
The ARN of the entitlement that allows you to subscribe to content that comes from another AWS account\. The entitlement is set by the content originator and the ARN is generated as part of the originator’s flow\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngestIp`  <a name="cfn-mediaconnect-flow-source-ingestip"></a>
The IP address that the flow listens on for incoming content\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngestPort`  <a name="cfn-mediaconnect-flow-source-ingestport"></a>
The port that the flow listens on for incoming content\. If the protocol of the source is Zixi, the port must be set to 2088\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxBitrate`  <a name="cfn-mediaconnect-flow-source-maxbitrate"></a>
The maximum bitrate for RIST, RTP, and RTP\-FEC streams\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxLatency`  <a name="cfn-mediaconnect-flow-source-maxlatency"></a>
The maximum latency in milliseconds for a RIST or Zixi\-based source\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinLatency`  <a name="cfn-mediaconnect-flow-source-minlatency"></a>
The minimum latency in milliseconds for SRT\-based streams\. In streams that use the SRT protocol, this value that you set on your MediaConnect source or output represents the minimal potential latency of that connection\. The latency of the stream is set to the highest number between the sender’s minimum latency and the receiver’s minimum latency\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconnect-flow-source-name"></a>
The name of the source\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-mediaconnect-flow-source-protocol"></a>
The protocol that is used by the source\. AWS CloudFormation does not currently support CDI or ST 2110 JPEG XS source protocols\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SenderControlPort`  <a name="cfn-mediaconnect-flow-source-sendercontrolport"></a>
The port that the flow uses to send outbound requests to initiate connection with the sender\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SenderIpAddress`  <a name="cfn-mediaconnect-flow-source-senderipaddress"></a>
The IP address that the flow communicates with to initiate connection with the sender\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceArn`  <a name="cfn-mediaconnect-flow-source-sourcearn"></a>
The ARN of the source\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceIngestPort`  <a name="cfn-mediaconnect-flow-source-sourceingestport"></a>
The port that the flow will be listening on for incoming content\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceListenerAddress`  <a name="cfn-mediaconnect-flow-source-sourcelisteneraddress"></a>
Source IP or domain name for SRT\-caller protocol\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceListenerPort`  <a name="cfn-mediaconnect-flow-source-sourcelistenerport"></a>
Source port for SRT\-caller protocol\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamId`  <a name="cfn-mediaconnect-flow-source-streamid"></a>
The stream ID that you want to use for the transport\. This parameter applies only to Zixi\-based streams\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcInterfaceName`  <a name="cfn-mediaconnect-flow-source-vpcinterfacename"></a>
The name of the VPC interface that the source content comes from\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WhitelistCidr`  <a name="cfn-mediaconnect-flow-source-whitelistcidr"></a>
The range of IP addresses that are allowed to contribute content to your source\. Format the IP addresses as a Classless Inter\-Domain Routing \(CIDR\) block; for example, 10\.0\.0\.0/16\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)