# AWS::MediaConnect::FlowOutput<a name="aws-resource-mediaconnect-flowoutput"></a>

The AWS::MediaConnect::FlowOutput resource defines the destination address, protocol, and port that AWS Elemental MediaConnect sends the ingested video to\. Each flow can have up to 50 outputs\. An output can have the same protocol or a different protocol from the source\. The following protocols are supported: RIST, RTP, RTP\-FEC, SRT\-listener, SRT\-caller, Zixi pull, Zixi push, and Fujitsu\-QoS\. CDI and ST 2110 JPEG XS protocols are not currently supported by AWS CloudFormation\. 

## Syntax<a name="aws-resource-mediaconnect-flowoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconnect-flowoutput-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConnect::FlowOutput",
  "Properties" : {
      "[CidrAllowList](#cfn-mediaconnect-flowoutput-cidrallowlist)" : [ String, ... ],
      "[Description](#cfn-mediaconnect-flowoutput-description)" : String,
      "[Destination](#cfn-mediaconnect-flowoutput-destination)" : String,
      "[Encryption](#cfn-mediaconnect-flowoutput-encryption)" : Encryption,
      "[FlowArn](#cfn-mediaconnect-flowoutput-flowarn)" : String,
      "[MaxLatency](#cfn-mediaconnect-flowoutput-maxlatency)" : Integer,
      "[MinLatency](#cfn-mediaconnect-flowoutput-minlatency)" : Integer,
      "[Name](#cfn-mediaconnect-flowoutput-name)" : String,
      "[Port](#cfn-mediaconnect-flowoutput-port)" : Integer,
      "[Protocol](#cfn-mediaconnect-flowoutput-protocol)" : String,
      "[RemoteId](#cfn-mediaconnect-flowoutput-remoteid)" : String,
      "[SmoothingLatency](#cfn-mediaconnect-flowoutput-smoothinglatency)" : Integer,
      "[StreamId](#cfn-mediaconnect-flowoutput-streamid)" : String,
      "[VpcInterfaceAttachment](#cfn-mediaconnect-flowoutput-vpcinterfaceattachment)" : VpcInterfaceAttachment
    }
}
```

### YAML<a name="aws-resource-mediaconnect-flowoutput-syntax.yaml"></a>

```
Type: AWS::MediaConnect::FlowOutput
Properties: 
  [CidrAllowList](#cfn-mediaconnect-flowoutput-cidrallowlist): 
    - String
  [Description](#cfn-mediaconnect-flowoutput-description): String
  [Destination](#cfn-mediaconnect-flowoutput-destination): String
  [Encryption](#cfn-mediaconnect-flowoutput-encryption): 
    Encryption
  [FlowArn](#cfn-mediaconnect-flowoutput-flowarn): String
  [MaxLatency](#cfn-mediaconnect-flowoutput-maxlatency): Integer
  [MinLatency](#cfn-mediaconnect-flowoutput-minlatency): Integer
  [Name](#cfn-mediaconnect-flowoutput-name): String
  [Port](#cfn-mediaconnect-flowoutput-port): Integer
  [Protocol](#cfn-mediaconnect-flowoutput-protocol): String
  [RemoteId](#cfn-mediaconnect-flowoutput-remoteid): String
  [SmoothingLatency](#cfn-mediaconnect-flowoutput-smoothinglatency): Integer
  [StreamId](#cfn-mediaconnect-flowoutput-streamid): String
  [VpcInterfaceAttachment](#cfn-mediaconnect-flowoutput-vpcinterfaceattachment): 
    VpcInterfaceAttachment
```

## Properties<a name="aws-resource-mediaconnect-flowoutput-properties"></a>

`CidrAllowList`  <a name="cfn-mediaconnect-flowoutput-cidrallowlist"></a>
The range of IP addresses that are allowed to initiate output requests to this flow\. Format the IP addresses as a Classless Inter\-Domain Routing \(CIDR\) block; for example, 10\.0\.0\.0/16\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-mediaconnect-flowoutput-description"></a>
A description of the output\. This description is not visible outside of the current AWS account even if the account grants entitlements to other accounts\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destination`  <a name="cfn-mediaconnect-flowoutput-destination"></a>
The IP address where you want to send the output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encryption`  <a name="cfn-mediaconnect-flowoutput-encryption"></a>
The encryption credentials that you want to use for the output\.  
*Required*: No  
*Type*: [Encryption](aws-properties-mediaconnect-flowoutput-encryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlowArn`  <a name="cfn-mediaconnect-flowoutput-flowarn"></a>
The Amazon Resource Name \(ARN\) of the flow this output is attached to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxLatency`  <a name="cfn-mediaconnect-flowoutput-maxlatency"></a>
The maximum latency in milliseconds\. This parameter applies only to RIST\-based, Zixi\-based, and Fujitsu\-based streams\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinLatency`  <a name="cfn-mediaconnect-flowoutput-minlatency"></a>
The minimum latency in milliseconds for SRT\-based streams\. In streams that use the SRT protocol, this value that you set on your MediaConnect source or output represents the minimal potential latency of that connection\. The latency of the stream is set to the highest number between the sender’s minimum latency and the receiver’s minimum latency\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconnect-flowoutput-name"></a>
The name of the VPC interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-mediaconnect-flowoutput-port"></a>
The port to use when MediaConnect distributes content to the output\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-mediaconnect-flowoutput-protocol"></a>
The protocol to use for the output\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoteId`  <a name="cfn-mediaconnect-flowoutput-remoteid"></a>
The identifier that is assigned to the Zixi receiver\. This parameter applies only to outputs that use Zixi pull\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmoothingLatency`  <a name="cfn-mediaconnect-flowoutput-smoothinglatency"></a>
The smoothing latency in milliseconds for RIST, RTP, and RTP\-FEC streams\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamId`  <a name="cfn-mediaconnect-flowoutput-streamid"></a>
The stream ID that you want to use for this transport\. This parameter applies only to Zixi and SRT caller\-based streams\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcInterfaceAttachment`  <a name="cfn-mediaconnect-flowoutput-vpcinterfaceattachment"></a>
The VPC interface that you want to send your output to\.  
*Required*: No  
*Type*: [VpcInterfaceAttachment](aws-properties-mediaconnect-flowoutput-vpcinterfaceattachment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediaconnect-flowoutput-return-values"></a>

### Ref<a name="aws-resource-mediaconnect-flowoutput-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the output ARN\. For example:

`{ "Ref": "arn:aws:mediaconnect:us-east-1:111122223333:output:2-3aBC45dEF67hiJ89-c34de5fG678h:NYCOutput" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediaconnect-flowoutput-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-mediaconnect-flowoutput-return-values-fn--getatt-fn--getatt"></a>

`OutputArn`  <a name="OutputArn-fn::getatt"></a>
The ARN of the output\.