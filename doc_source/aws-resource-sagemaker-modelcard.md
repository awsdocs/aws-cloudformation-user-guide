# AWS::SageMaker::ModelCard<a name="aws-resource-sagemaker-modelcard"></a>

Creates an Amazon SageMaker Model Card\.

For information about how to use model cards, see [Amazon SageMaker Model Card](https://docs.aws.amazon.com/sagemaker/latest/dg/model-cards.html)\.

## Syntax<a name="aws-resource-sagemaker-modelcard-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-modelcard-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::ModelCard",
  "Properties" : {
      "[Content](#cfn-sagemaker-modelcard-content)" : Content,
      "[CreatedBy](#cfn-sagemaker-modelcard-createdby)" : UserContext,
      "[LastModifiedBy](#cfn-sagemaker-modelcard-lastmodifiedby)" : UserContext,
      "[ModelCardName](#cfn-sagemaker-modelcard-modelcardname)" : String,
      "[ModelCardStatus](#cfn-sagemaker-modelcard-modelcardstatus)" : String,
      "[SecurityConfig](#cfn-sagemaker-modelcard-securityconfig)" : SecurityConfig,
      "[Tags](#cfn-sagemaker-modelcard-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-modelcard-syntax.yaml"></a>

```
Type: AWS::SageMaker::ModelCard
Properties: 
  [Content](#cfn-sagemaker-modelcard-content): 
    Content
  [CreatedBy](#cfn-sagemaker-modelcard-createdby): 
    UserContext
  [LastModifiedBy](#cfn-sagemaker-modelcard-lastmodifiedby): 
    UserContext
  [ModelCardName](#cfn-sagemaker-modelcard-modelcardname): String
  [ModelCardStatus](#cfn-sagemaker-modelcard-modelcardstatus): String
  [SecurityConfig](#cfn-sagemaker-modelcard-securityconfig): 
    SecurityConfig
  [Tags](#cfn-sagemaker-modelcard-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-modelcard-properties"></a>

`Content`  <a name="cfn-sagemaker-modelcard-content"></a>
The content of the model card\. Content uses the [model card JSON schema](https://docs.aws.amazon.com/sagemaker/latest/dg/model-cards.html#model-cards-json-schema)\.  
*Required*: Yes  
*Type*: [Content](aws-properties-sagemaker-modelcard-content.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreatedBy`  <a name="cfn-sagemaker-modelcard-createdby"></a>
Information about the user who created or modified one or more of the following:  
+ Experiment
+ Trial
+ Trial component
+ Lineage group
+ Project
+ Model Card
*Required*: No  
*Type*: [UserContext](aws-properties-sagemaker-modelcard-usercontext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastModifiedBy`  <a name="cfn-sagemaker-modelcard-lastmodifiedby"></a>
Property description not available\.  
*Required*: No  
*Type*: [UserContext](aws-properties-sagemaker-modelcard-usercontext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelCardName`  <a name="cfn-sagemaker-modelcard-modelcardname"></a>
The unique name of the model card\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelCardStatus`  <a name="cfn-sagemaker-modelcard-modelcardstatus"></a>
The approval status of the model card within your organization\. Different organizations might have different criteria for model card review and approval\.  
+  `Draft`: The model card is a work in progress\.
+  `PendingReview`: The model card is pending review\.
+  `Approved`: The model card is approved\.
+  `Archived`: The model card is archived\. No more updates should be made to the model card, but it can still be exported\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `Approved | Archived | Draft | PendingReview`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityConfig`  <a name="cfn-sagemaker-modelcard-securityconfig"></a>
The security configuration used to protect model card data\.  
*Required*: No  
*Type*: [SecurityConfig](aws-properties-sagemaker-modelcard-securityconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-modelcard-tags"></a>
Key\-value pairs used to manage metadata for the model card\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sagemaker-modelcard-return-values"></a>

### Ref<a name="aws-resource-sagemaker-modelcard-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the model card name\.

For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-modelcard-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. For more information about using the Fn::GetAtt intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-sagemaker-modelcard-return-values-fn--getatt-fn--getatt"></a>

`CreatedBy.DomainId`  <a name="CreatedBy.DomainId-fn::getatt"></a>
Property description not available\.

`CreatedBy.UserProfileArn`  <a name="CreatedBy.UserProfileArn-fn::getatt"></a>
Property description not available\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
Property description not available\.

`LastModifiedBy.DomainId`  <a name="LastModifiedBy.DomainId-fn::getatt"></a>
Property description not available\.

`LastModifiedBy.UserProfileArn`  <a name="LastModifiedBy.UserProfileArn-fn::getatt"></a>
Property description not available\.

`ModelCardArn`  <a name="ModelCardArn-fn::getatt"></a>
The Amazon Resource Number \(ARN\) of the model card\. For example, `arn:aws:sagemaker:us-west-2:012345678901:modelcard/examplemodelcard`\.

`ModelCardProcessingStatus`  <a name="ModelCardProcessingStatus-fn::getatt"></a>
Property description not available\.