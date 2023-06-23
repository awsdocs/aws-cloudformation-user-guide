# AWS::MediaConnect::Bridge EgressGatewayBridge<a name="aws-properties-mediaconnect-bridge-egressgatewaybridge"></a>

Create a bridge with the egress bridge type\. An egress bridge is a cloud\-to\-ground bridge\. The content comes from an existing MediaConnect flow and is delivered to your premises\.

## Syntax<a name="aws-properties-mediaconnect-bridge-egressgatewaybridge-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-bridge-egressgatewaybridge-syntax.json"></a>

```
{
  "[MaxBitrate](#cfn-mediaconnect-bridge-egressgatewaybridge-maxbitrate)" : Integer
}
```

### YAML<a name="aws-properties-mediaconnect-bridge-egressgatewaybridge-syntax.yaml"></a>

```
  [MaxBitrate](#cfn-mediaconnect-bridge-egressgatewaybridge-maxbitrate): Integer
```

## Properties<a name="aws-properties-mediaconnect-bridge-egressgatewaybridge-properties"></a>

`MaxBitrate`  <a name="cfn-mediaconnect-bridge-egressgatewaybridge-maxbitrate"></a>
The maximum expected bitrate \(in bps\) of the egress bridge\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)