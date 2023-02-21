# AWS::Omics::SequenceStore<a name="aws-resource-omics-sequencestore"></a>

Creates a sequence store\.

## Syntax<a name="aws-resource-omics-sequencestore-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-omics-sequencestore-syntax.json"></a>

```
{
  "Type" : "AWS::Omics::SequenceStore",
  "Properties" : {
      "[Description](#cfn-omics-sequencestore-description)" : String,
      "[Name](#cfn-omics-sequencestore-name)" : String,
      "[SseConfig](#cfn-omics-sequencestore-sseconfig)" : SseConfig,
      "[Tags](#cfn-omics-sequencestore-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-omics-sequencestore-syntax.yaml"></a>

```
Type: AWS::Omics::SequenceStore
Properties: 
  [Description](#cfn-omics-sequencestore-description): String
  [Name](#cfn-omics-sequencestore-name): String
  [SseConfig](#cfn-omics-sequencestore-sseconfig): 
    SseConfig
  [Tags](#cfn-omics-sequencestore-tags): 
    Key : Value
```

## Properties<a name="aws-resource-omics-sequencestore-properties"></a>

`Description`  <a name="cfn-omics-sequencestore-description"></a>
A description for the store\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-omics-sequencestore-name"></a>
A name for the store\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SseConfig`  <a name="cfn-omics-sequencestore-sseconfig"></a>
Server\-side encryption \(SSE\) settings for the store\.  
*Required*: No  
*Type*: [SseConfig](aws-properties-omics-sequencestore-sseconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-omics-sequencestore-tags"></a>
Tags for the store\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-omics-sequencestore-return-values"></a>

### Ref<a name="aws-resource-omics-sequencestore-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the details of this resource\. For example:

 `{ "Ref": "SequenceStore.CreationTime" }` `Ref` returns the timestamp for when the sequence store was created\. 

### Fn::GetAtt<a name="aws-resource-omics-sequencestore-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-omics-sequencestore-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The store's ARN\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
When the store was created\.

`SequenceStoreId`  <a name="SequenceStoreId-fn::getatt"></a>
The store's ID\.