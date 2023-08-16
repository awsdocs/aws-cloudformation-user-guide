# AWS::Omics::VariantStore SseConfig<a name="aws-properties-omics-variantstore-sseconfig"></a>

Server\-side encryption \(SSE\) settings for a store\.

## Syntax<a name="aws-properties-omics-variantstore-sseconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-omics-variantstore-sseconfig-syntax.json"></a>

```
{
  "[KeyArn](#cfn-omics-variantstore-sseconfig-keyarn)" : String,
  "[Type](#cfn-omics-variantstore-sseconfig-type)" : String
}
```

### YAML<a name="aws-properties-omics-variantstore-sseconfig-syntax.yaml"></a>

```
  [KeyArn](#cfn-omics-variantstore-sseconfig-keyarn): String
  [Type](#cfn-omics-variantstore-sseconfig-type): String
```

## Properties<a name="aws-properties-omics-variantstore-sseconfig-properties"></a>

`KeyArn`  <a name="cfn-omics-variantstore-sseconfig-keyarn"></a>
An encryption key ARN\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*arn:([^: ]*):([^: ]*):([^: ]*):([0-9]{12}):([^: ]*).*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-omics-variantstore-sseconfig-type"></a>
The encryption type\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `KMS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)