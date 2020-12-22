# AWS::Kendra::Index<a name="aws-resource-kendra-index"></a>

Specifies a new Amazon Kendra index\. And index is a collection of documents and associated metadata that you want to search for relevant documents\.

Once the index is active you can add documents to your index using the [BatchPutDocument](https://docs.aws.amazon.com/kendra/latest/dg/BatchPutDocument.html) operation or using one of the supported data sources\. 

## Syntax<a name="aws-resource-kendra-index-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kendra-index-syntax.json"></a>

```
{
  "Type" : "AWS::Kendra::Index",
  "Properties" : {
      "[CapacityUnits](#cfn-kendra-index-capacityunits)" : CapacityUnitsConfiguration,
      "[Description](#cfn-kendra-index-description)" : String,
      "[DocumentMetadataConfigurations](#cfn-kendra-index-documentmetadataconfigurations)" : DocumentMetadataConfigurationList,
      "[Edition](#cfn-kendra-index-edition)" : String,
      "[Name](#cfn-kendra-index-name)" : String,
      "[RoleArn](#cfn-kendra-index-rolearn)" : String,
      "[ServerSideEncryptionConfiguration](#cfn-kendra-index-serversideencryptionconfiguration)" : ServerSideEncryptionConfiguration,
      "[Tags](#cfn-kendra-index-tags)" : TagList,
      "[UserContextPolicy](#cfn-kendra-index-usercontextpolicy)" : String,
      "[UserTokenConfigurations](#cfn-kendra-index-usertokenconfigurations)" : UserTokenConfigurationList
    }
}
```

### YAML<a name="aws-resource-kendra-index-syntax.yaml"></a>

```
Type: AWS::Kendra::Index
Properties: 
  [CapacityUnits](#cfn-kendra-index-capacityunits): 
    CapacityUnitsConfiguration
  [Description](#cfn-kendra-index-description): String
  [DocumentMetadataConfigurations](#cfn-kendra-index-documentmetadataconfigurations): 
    DocumentMetadataConfigurationList
  [Edition](#cfn-kendra-index-edition): String
  [Name](#cfn-kendra-index-name): String
  [RoleArn](#cfn-kendra-index-rolearn): String
  [ServerSideEncryptionConfiguration](#cfn-kendra-index-serversideencryptionconfiguration): 
    ServerSideEncryptionConfiguration
  [Tags](#cfn-kendra-index-tags): 
    TagList
  [UserContextPolicy](#cfn-kendra-index-usercontextpolicy): String
  [UserTokenConfigurations](#cfn-kendra-index-usertokenconfigurations): 
    UserTokenConfigurationList
```

## Properties<a name="aws-resource-kendra-index-properties"></a>

`CapacityUnits`  <a name="cfn-kendra-index-capacityunits"></a>
Specifies capacity units configured for your index\. You can add and remove capacity units to tune an index to your requirements\. You can set capacity units only for Enterprise edition indexes\.  
*Required*: No  
*Type*: [CapacityUnitsConfiguration](aws-properties-kendra-index-capacityunitsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-kendra-index-description"></a>
A description of the index\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentMetadataConfigurations`  <a name="cfn-kendra-index-documentmetadataconfigurations"></a>
Specifies the properties of an index field\. You can add either a custom or a built\-in field\. You can add and remove built\-in fields at any time\. When a built\-in field is removed it's configuration reverts to the default for the field\. Custom fields can't be removed from an index after they are added\.  
*Required*: No  
*Type*: [DocumentMetadataConfigurationList](aws-properties-kendra-index-documentmetadataconfigurationlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Edition`  <a name="cfn-kendra-index-edition"></a>
Indicates whether the index is a enterprise edition index or a developer edition index\. Valid values are `DEVELOPER_EDITION` and `ENTERPRISE_EDITION`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DEVELOPER_EDITION | ENTERPRISE_EDITION`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-kendra-index-name"></a>
The name of the index\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Pattern*: `[a-zA-Z0-9][a-zA-Z0-9_-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-kendra-index-rolearn"></a>
An IAM role that gives Amazon Kendra permissions to access your Amazon CloudWatch logs and metrics\. This is also the role used when you use the [BatchPutDocument](https://docs.aws.amazon.com/kendra/latest/dg/BatchPutDocument.html) operation to index documents from an Amazon S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerSideEncryptionConfiguration`  <a name="cfn-kendra-index-serversideencryptionconfiguration"></a>
The identifier of the AWS KMS customer managed key \(CMK\) to use to encrypt data indexed by Amazon Kendra\. Amazon Kendra doesn't support asymmetric CMKs\.  
*Required*: No  
*Type*: [ServerSideEncryptionConfiguration](aws-properties-kendra-index-serversideencryptionconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-kendra-index-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: [TagList](aws-properties-kendra-index-taglist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserContextPolicy`  <a name="cfn-kendra-index-usercontextpolicy"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserTokenConfigurations`  <a name="cfn-kendra-index-usertokenconfigurations"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [UserTokenConfigurationList](aws-properties-kendra-index-usertokenconfigurationlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-kendra-index-return-values"></a>

### Ref<a name="aws-resource-kendra-index-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the index ID\. For example:

 `{"Ref": "index-id"}` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-kendra-index-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-kendra-index-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the index\. For example: `arn:aws:kendra:us-west-2:111122223333:index/0123456789abcdef`\.

`Id`  <a name="Id-fn::getatt"></a>
The identifier for the index\. For example: `f4aeaa10-8056-4b2c-a343-522ca0f41234`\.