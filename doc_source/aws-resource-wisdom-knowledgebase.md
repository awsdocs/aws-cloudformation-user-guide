# AWS::Wisdom::KnowledgeBase<a name="aws-resource-wisdom-knowledgebase"></a>

Specifies a knowledge base\.

## Syntax<a name="aws-resource-wisdom-knowledgebase-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wisdom-knowledgebase-syntax.json"></a>

```
{
  "Type" : "AWS::Wisdom::KnowledgeBase",
  "Properties" : {
      "[Description](#cfn-wisdom-knowledgebase-description)" : String,
      "[KnowledgeBaseType](#cfn-wisdom-knowledgebase-knowledgebasetype)" : String,
      "[Name](#cfn-wisdom-knowledgebase-name)" : String,
      "[RenderingConfiguration](#cfn-wisdom-knowledgebase-renderingconfiguration)" : RenderingConfiguration,
      "[ServerSideEncryptionConfiguration](#cfn-wisdom-knowledgebase-serversideencryptionconfiguration)" : ServerSideEncryptionConfiguration,
      "[SourceConfiguration](#cfn-wisdom-knowledgebase-sourceconfiguration)" : SourceConfiguration,
      "[Tags](#cfn-wisdom-knowledgebase-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-wisdom-knowledgebase-syntax.yaml"></a>

```
Type: AWS::Wisdom::KnowledgeBase
Properties: 
  [Description](#cfn-wisdom-knowledgebase-description): String
  [KnowledgeBaseType](#cfn-wisdom-knowledgebase-knowledgebasetype): String
  [Name](#cfn-wisdom-knowledgebase-name): String
  [RenderingConfiguration](#cfn-wisdom-knowledgebase-renderingconfiguration): 
    RenderingConfiguration
  [ServerSideEncryptionConfiguration](#cfn-wisdom-knowledgebase-serversideencryptionconfiguration): 
    ServerSideEncryptionConfiguration
  [SourceConfiguration](#cfn-wisdom-knowledgebase-sourceconfiguration): 
    SourceConfiguration
  [Tags](#cfn-wisdom-knowledgebase-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-wisdom-knowledgebase-properties"></a>

`Description`  <a name="cfn-wisdom-knowledgebase-description"></a>
The description\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[a-zA-Z0-9\s_.,-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KnowledgeBaseType`  <a name="cfn-wisdom-knowledgebase-knowledgebasetype"></a>
The type of knowledge base\. Only CUSTOM knowledge bases allow you to upload your own content\. EXTERNAL knowledge bases support integrations with third\-party systems whose content is synchronized automatically\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `CUSTOM | EXTERNAL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-wisdom-knowledgebase-name"></a>
The name of the knowledge base\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[a-zA-Z0-9\s_.,-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RenderingConfiguration`  <a name="cfn-wisdom-knowledgebase-renderingconfiguration"></a>
Information about how to render the content\.  
*Required*: No  
*Type*: [RenderingConfiguration](aws-properties-wisdom-knowledgebase-renderingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerSideEncryptionConfiguration`  <a name="cfn-wisdom-knowledgebase-serversideencryptionconfiguration"></a>
The KMS key used for encryption\.  
*Required*: No  
*Type*: [ServerSideEncryptionConfiguration](aws-properties-wisdom-knowledgebase-serversideencryptionconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceConfiguration`  <a name="cfn-wisdom-knowledgebase-sourceconfiguration"></a>
The source of the knowledge base content\. Only set this argument for EXTERNAL knowledge bases\.  
*Required*: No  
*Type*: [SourceConfiguration](aws-properties-wisdom-knowledgebase-sourceconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-wisdom-knowledgebase-tags"></a>
The tags used to organize, track, or control access for this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-wisdom-knowledgebase-return-values"></a>

### Ref<a name="aws-resource-wisdom-knowledgebase-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the knowledge base ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-wisdom-knowledgebase-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-wisdom-knowledgebase-return-values-fn--getatt-fn--getatt"></a>

`KnowledgeBaseArn`  <a name="KnowledgeBaseArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the knowledge base\.

`KnowledgeBaseId`  <a name="KnowledgeBaseId-fn::getatt"></a>
The ID of the knowledge base\.