# AWS::IoT::TopicRule HttpAuthorization<a name="aws-properties-iot-topicrule-httpauthorization"></a>

The authorization method used to send messages\.

## Syntax<a name="aws-properties-iot-topicrule-httpauthorization-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-httpauthorization-syntax.json"></a>

```
{
  "[Sigv4](#cfn-iot-topicrule-httpauthorization-sigv4)" : SigV4Authorization
}
```

### YAML<a name="aws-properties-iot-topicrule-httpauthorization-syntax.yaml"></a>

```
  [Sigv4](#cfn-iot-topicrule-httpauthorization-sigv4): 
    SigV4Authorization
```

## Properties<a name="aws-properties-iot-topicrule-httpauthorization-properties"></a>

`Sigv4`  <a name="cfn-iot-topicrule-httpauthorization-sigv4"></a>
Use Sig V4 authorization\. For more information, see [Signature Version 4 Signing Process](https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html)\.  
*Required*: No  
*Type*: [SigV4Authorization](aws-properties-iot-topicrule-sigv4authorization.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)