# AWS::Comprehend::DocumentClassifier<a name="aws-resource-comprehend-documentclassifier"></a>

<a name="aws-resource-comprehend-documentclassifier-description"></a>The `AWS::Comprehend::DocumentClassifier` resource Property description not available\. for Comprehend\.

## Syntax<a name="aws-resource-comprehend-documentclassifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-comprehend-documentclassifier-syntax.json"></a>

```
{
  "Type" : "AWS::Comprehend::DocumentClassifier",
  "Properties" : {
      "[DataAccessRoleArn](#cfn-comprehend-documentclassifier-dataaccessrolearn)" : String,
      "[DocumentClassifierName](#cfn-comprehend-documentclassifier-documentclassifiername)" : String,
      "[InputDataConfig](#cfn-comprehend-documentclassifier-inputdataconfig)" : DocumentClassifierInputDataConfig,
      "[LanguageCode](#cfn-comprehend-documentclassifier-languagecode)" : String,
      "[Mode](#cfn-comprehend-documentclassifier-mode)" : String,
      "[ModelKmsKeyId](#cfn-comprehend-documentclassifier-modelkmskeyid)" : String,
      "[ModelPolicy](#cfn-comprehend-documentclassifier-modelpolicy)" : String,
      "[OutputDataConfig](#cfn-comprehend-documentclassifier-outputdataconfig)" : DocumentClassifierOutputDataConfig,
      "[Tags](#cfn-comprehend-documentclassifier-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VersionName](#cfn-comprehend-documentclassifier-versionname)" : String,
      "[VolumeKmsKeyId](#cfn-comprehend-documentclassifier-volumekmskeyid)" : String,
      "[VpcConfig](#cfn-comprehend-documentclassifier-vpcconfig)" : VpcConfig
    }
}
```

### YAML<a name="aws-resource-comprehend-documentclassifier-syntax.yaml"></a>

```
Type: AWS::Comprehend::DocumentClassifier
Properties: 
  [DataAccessRoleArn](#cfn-comprehend-documentclassifier-dataaccessrolearn): String
  [DocumentClassifierName](#cfn-comprehend-documentclassifier-documentclassifiername): String
  [InputDataConfig](#cfn-comprehend-documentclassifier-inputdataconfig): 
    DocumentClassifierInputDataConfig
  [LanguageCode](#cfn-comprehend-documentclassifier-languagecode): String
  [Mode](#cfn-comprehend-documentclassifier-mode): String
  [ModelKmsKeyId](#cfn-comprehend-documentclassifier-modelkmskeyid): String
  [ModelPolicy](#cfn-comprehend-documentclassifier-modelpolicy): String
  [OutputDataConfig](#cfn-comprehend-documentclassifier-outputdataconfig): 
    DocumentClassifierOutputDataConfig
  [Tags](#cfn-comprehend-documentclassifier-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VersionName](#cfn-comprehend-documentclassifier-versionname): String
  [VolumeKmsKeyId](#cfn-comprehend-documentclassifier-volumekmskeyid): String
  [VpcConfig](#cfn-comprehend-documentclassifier-vpcconfig): 
    VpcConfig
```

## Properties<a name="aws-resource-comprehend-documentclassifier-properties"></a>

`DataAccessRoleArn`  <a name="cfn-comprehend-documentclassifier-dataaccessrolearn"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DocumentClassifierName`  <a name="cfn-comprehend-documentclassifier-documentclassifiername"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InputDataConfig`  <a name="cfn-comprehend-documentclassifier-inputdataconfig"></a>
Property description not available\.  
*Required*: Yes  
*Type*: [DocumentClassifierInputDataConfig](aws-properties-comprehend-documentclassifier-documentclassifierinputdataconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LanguageCode`  <a name="cfn-comprehend-documentclassifier-languagecode"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Mode`  <a name="cfn-comprehend-documentclassifier-mode"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelKmsKeyId`  <a name="cfn-comprehend-documentclassifier-modelkmskeyid"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelPolicy`  <a name="cfn-comprehend-documentclassifier-modelpolicy"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputDataConfig`  <a name="cfn-comprehend-documentclassifier-outputdataconfig"></a>
Property description not available\.  
*Required*: No  
*Type*: [DocumentClassifierOutputDataConfig](aws-properties-comprehend-documentclassifier-documentclassifieroutputdataconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-comprehend-documentclassifier-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionName`  <a name="cfn-comprehend-documentclassifier-versionname"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeKmsKeyId`  <a name="cfn-comprehend-documentclassifier-volumekmskeyid"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcConfig`  <a name="cfn-comprehend-documentclassifier-vpcconfig"></a>
Property description not available\.  
*Required*: No  
*Type*: [VpcConfig](aws-properties-comprehend-documentclassifier-vpcconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-comprehend-documentclassifier-return-values"></a>

### Ref<a name="aws-resource-comprehend-documentclassifier-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-comprehend-documentclassifier-return-values-fn--getatt"></a>

#### <a name="aws-resource-comprehend-documentclassifier-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.