# AWS::Omics::ReferenceStore<a name="aws-resource-omics-referencestore"></a>

Creates a reference store\.

## Syntax<a name="aws-resource-omics-referencestore-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-omics-referencestore-syntax.json"></a>

```
{
  "Type" : "AWS::Omics::ReferenceStore",
  "Properties" : {
      "[Description](#cfn-omics-referencestore-description)" : String,
      "[Name](#cfn-omics-referencestore-name)" : String,
      "[SseConfig](#cfn-omics-referencestore-sseconfig)" : SseConfig,
      "[Tags](#cfn-omics-referencestore-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-omics-referencestore-syntax.yaml"></a>

```
Type: AWS::Omics::ReferenceStore
Properties: 
  [Description](#cfn-omics-referencestore-description): String
  [Name](#cfn-omics-referencestore-name): String
  [SseConfig](#cfn-omics-referencestore-sseconfig): 
    SseConfig
  [Tags](#cfn-omics-referencestore-tags): 
    Key : Value
```

## Properties<a name="aws-resource-omics-referencestore-properties"></a>

`Description`  <a name="cfn-omics-referencestore-description"></a>
A description for the store\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-omics-referencestore-name"></a>
A name for the store\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SseConfig`  <a name="cfn-omics-referencestore-sseconfig"></a>
Server\-side encryption \(SSE\) settings for the store\.  
*Required*: No  
*Type*: [SseConfig](aws-properties-omics-referencestore-sseconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-omics-referencestore-tags"></a>
Tags for the store\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-omics-referencestore-return-values"></a>

### Ref<a name="aws-resource-omics-referencestore-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the details of this resource\. For example:

 `{ "Ref": "ReferenceStore.Arn" }` `Ref` returns the arn for the reference store\. 

### Fn::GetAtt<a name="aws-resource-omics-referencestore-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-omics-referencestore-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
When the store was created\.

`ReferenceStoreId`  <a name="ReferenceStoreId-fn::getatt"></a>
The store's ID\.