# AWS::Comprehend::DocumentClassifier<a name="aws-resource-comprehend-documentclassifier"></a>

This resource creates and trains a document classifier to categorize documents\. You provide a set of training documents that are labeled with the categories that you want to identify\. After the classifier is trained you can use it to categorize a set of labeled documents into the categories\. For more information, see [Document Classification](https://docs.aws.amazon.com/comprehend/latest/dg/how-document-classification.html) in the Comprehend Developer Guide\.

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
The Amazon Resource Name \(ARN\) of the IAM role that grants Amazon Comprehend read access to your input data\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:aws(-[^:]+)?:iam::[0-9]{12}:role/.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DocumentClassifierName`  <a name="cfn-comprehend-documentclassifier-documentclassifiername"></a>
The name of the document classifier\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9])*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InputDataConfig`  <a name="cfn-comprehend-documentclassifier-inputdataconfig"></a>
Specifies the format and location of the input data for the job\.  
*Required*: Yes  
*Type*: [DocumentClassifierInputDataConfig](aws-properties-comprehend-documentclassifier-documentclassifierinputdataconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LanguageCode`  <a name="cfn-comprehend-documentclassifier-languagecode"></a>
The language of the input documents\. You can specify any of the languages supported by Amazon Comprehend\. All documents must be in the same language\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `de | en | es | fr | it | pt`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Mode`  <a name="cfn-comprehend-documentclassifier-mode"></a>
Indicates the mode in which the classifier will be trained\. The classifier can be trained in multi\-class mode, which identifies one and only one class for each document, or multi\-label mode, which identifies one or more labels for each document\. In multi\-label mode, multiple labels for an individual document are separated by a delimiter\. The default delimiter between labels is a pipe \(\|\)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `MULTI_CLASS | MULTI_LABEL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelKmsKeyId`  <a name="cfn-comprehend-documentclassifier-modelkmskeyid"></a>
ID for the AWS KMS key that Amazon Comprehend uses to encrypt trained custom models\. The ModelKmsKeyId can be either of the following formats:  
+ KMS Key ID: `"1234abcd-12ab-34cd-56ef-1234567890ab"` 
+ Amazon Resource Name \(ARN\) of a KMS Key: `"arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab"` 
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `^\p{ASCII}+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelPolicy`  <a name="cfn-comprehend-documentclassifier-modelpolicy"></a>
The resource\-based policy to attach to your custom document classifier model\. You can use this policy to allow another AWS account to import your custom model\.  
Provide your policy as a JSON body that you enter as a UTF\-8 encoded string without line breaks\. To provide valid JSON, enclose the attribute names and values in double quotes\. If the JSON body is also enclosed in double quotes, then you must escape the double quotes that are inside the policy:  
`"{\"attribute\": \"value\", \"attribute\": [\"value\"]}"`  
To avoid escaping quotes, you can use single quotes to enclose the policy and double quotes to enclose the JSON names and values:  
`'{"attribute": "value", "attribute": ["value"]}'`  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `20000`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u00FF]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputDataConfig`  <a name="cfn-comprehend-documentclassifier-outputdataconfig"></a>
 Provides output results configuration parameters for custom classifier jobs\.  
*Required*: No  
*Type*: [DocumentClassifierOutputDataConfig](aws-properties-comprehend-documentclassifier-documentclassifieroutputdataconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-comprehend-documentclassifier-tags"></a>
Tags to associate with the document classifier\. A tag is a key\-value pair that adds as a metadata to a resource used by Amazon Comprehend\. For example, a tag with "Sales" as the key might be added to a resource to indicate its use by the sales department\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionName`  <a name="cfn-comprehend-documentclassifier-versionname"></a>
The version name given to the newly created classifier\. Version names can have a maximum of 256 characters\. Alphanumeric characters, hyphens \(\-\) and underscores \(\_\) are allowed\. The version name must be unique among all models with the same classifier name in the AWS account/AWS Region\.  
*Required*: No  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9])*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeKmsKeyId`  <a name="cfn-comprehend-documentclassifier-volumekmskeyid"></a>
ID for the AWS Key Management Service \(KMS\) key that Amazon Comprehend uses to encrypt data on the storage volume attached to the ML compute instance\(s\) that process the analysis job\. The VolumeKmsKeyId can be either of the following formats:  
+ KMS Key ID: `"1234abcd-12ab-34cd-56ef-1234567890ab"` 
+ Amazon Resource Name \(ARN\) of a KMS Key: `"arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab"` 
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `^\p{ASCII}+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcConfig`  <a name="cfn-comprehend-documentclassifier-vpcconfig"></a>
 Configuration parameters for a private Virtual Private Cloud \(VPC\) containing the resources you are using for your custom classifier\. For more information, see [Amazon VPC](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)\.   
*Required*: No  
*Type*: [VpcConfig](aws-properties-comprehend-documentclassifier-vpcconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-comprehend-documentclassifier-return-values"></a>

### Ref<a name="aws-resource-comprehend-documentclassifier-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the Amazon Resource Name \(ARN\) of the document classifier\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-comprehend-documentclassifier-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-comprehend-documentclassifier-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the document classifier\.