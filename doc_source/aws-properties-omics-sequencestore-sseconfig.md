# AWS::Omics::SequenceStore SseConfig<a name="aws-properties-omics-sequencestore-sseconfig"></a>

Server\-side encryption \(SSE\) settings for a store\.

## Syntax<a name="aws-properties-omics-sequencestore-sseconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-omics-sequencestore-sseconfig-syntax.json"></a>

```
{
  "[KeyArn](#cfn-omics-sequencestore-sseconfig-keyarn)" : String,
  "[Type](#cfn-omics-sequencestore-sseconfig-type)" : String
}
```

### YAML<a name="aws-properties-omics-sequencestore-sseconfig-syntax.yaml"></a>

```
  [KeyArn](#cfn-omics-sequencestore-sseconfig-keyarn): String
  [Type](#cfn-omics-sequencestore-sseconfig-type): String
```

## Properties<a name="aws-properties-omics-sequencestore-sseconfig-properties"></a>

`KeyArn`  <a name="cfn-omics-sequencestore-sseconfig-keyarn"></a>
An encryption key ARN\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*arn:([^: ]*):([^: ]*):([^: ]*):([0-9]{12}):([^: ]*).*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-omics-sequencestore-sseconfig-type"></a>
The encryption type\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `KMS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)