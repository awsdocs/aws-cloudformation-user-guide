# AWS::SageMaker::ModelPackageGroup<a name="aws-resource-sagemaker-modelpackagegroup"></a>

A group of versioned models in the model registry\.

## Syntax<a name="aws-resource-sagemaker-modelpackagegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-modelpackagegroup-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::ModelPackageGroup",
  "Properties" : {
      "[ModelPackageGroupDescription](#cfn-sagemaker-modelpackagegroup-modelpackagegroupdescription)" : String,
      "[ModelPackageGroupName](#cfn-sagemaker-modelpackagegroup-modelpackagegroupname)" : String,
      "[ModelPackageGroupPolicy](#cfn-sagemaker-modelpackagegroup-modelpackagegrouppolicy)" : ,
      "[Tags](#cfn-sagemaker-modelpackagegroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-modelpackagegroup-syntax.yaml"></a>

```
Type: AWS::SageMaker::ModelPackageGroup
Properties: 
  [ModelPackageGroupDescription](#cfn-sagemaker-modelpackagegroup-modelpackagegroupdescription): String
  [ModelPackageGroupName](#cfn-sagemaker-modelpackagegroup-modelpackagegroupname): String
  [ModelPackageGroupPolicy](#cfn-sagemaker-modelpackagegroup-modelpackagegrouppolicy): 
  [Tags](#cfn-sagemaker-modelpackagegroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-modelpackagegroup-properties"></a>

`ModelPackageGroupDescription`  <a name="cfn-sagemaker-modelpackagegroup-modelpackagegroupdescription"></a>
The description for the model group\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `[\p{L}\p{M}\p{Z}\p{S}\p{N}\p{P}]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelPackageGroupName`  <a name="cfn-sagemaker-modelpackagegroup-modelpackagegroupname"></a>
The name of the model group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelPackageGroupPolicy`  <a name="cfn-sagemaker-modelpackagegroup-modelpackagegrouppolicy"></a>
A resouce policy to control access to a model group\. For information about resoure policies, see [Identity\-based policies and resource\-based policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_identity-vs-resource.html) in the *AWS Identity and Access Management User Guide\.*\.  
*Required*: No  
*Type*:   
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sagemaker-modelpackagegroup-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sagemaker-modelpackagegroup-return-values"></a>

### Ref<a name="aws-resource-sagemaker-modelpackagegroup-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-sagemaker-modelpackagegroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-sagemaker-modelpackagegroup-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time when the model group was created\.

`ModelPackageGroupArn`  <a name="ModelPackageGroupArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the model group\.

`ModelPackageGroupStatus`  <a name="ModelPackageGroupStatus-fn::getatt"></a>
The status of the model group\.