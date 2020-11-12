# AWS::Kendra::Faq<a name="aws-resource-kendra-faq"></a>

Specifies an new set of frequently asked question \(FAQ\) questions and answers\.

## Syntax<a name="aws-resource-kendra-faq-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kendra-faq-syntax.json"></a>

```
{
  "Type" : "AWS::Kendra::Faq",
  "Properties" : {
      "[Description](#cfn-kendra-faq-description)" : String,
      "[FileFormat](#cfn-kendra-faq-fileformat)" : String,
      "[IndexId](#cfn-kendra-faq-indexid)" : String,
      "[Name](#cfn-kendra-faq-name)" : String,
      "[RoleArn](#cfn-kendra-faq-rolearn)" : String,
      "[S3Path](#cfn-kendra-faq-s3path)" : S3Path,
      "[Tags](#cfn-kendra-faq-tags)" : TagList
    }
}
```

### YAML<a name="aws-resource-kendra-faq-syntax.yaml"></a>

```
Type: AWS::Kendra::Faq
Properties: 
  [Description](#cfn-kendra-faq-description): String
  [FileFormat](#cfn-kendra-faq-fileformat): String
  [IndexId](#cfn-kendra-faq-indexid): String
  [Name](#cfn-kendra-faq-name): String
  [RoleArn](#cfn-kendra-faq-rolearn): String
  [S3Path](#cfn-kendra-faq-s3path): 
    S3Path
  [Tags](#cfn-kendra-faq-tags): 
    TagList
```

## Properties<a name="aws-resource-kendra-faq-properties"></a>

`Description`  <a name="cfn-kendra-faq-description"></a>
A description of the FAQ\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileFormat`  <a name="cfn-kendra-faq-fileformat"></a>
The format of the input file\. You can choose between a basic CSV format, a CSV format that includes customs attributes in a header, and a JSON format that includes custom attributes\.   
 The format must match the format of the file stored in the S3 bucket identified in the S3Path parameter\.   
Valid values are:  
+ `CSV`
+ `CSV_WITH_HEADER`
+ `JSON`
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IndexId`  <a name="cfn-kendra-faq-indexid"></a>
The identifier of the index that contains the FAQ\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-kendra-faq-name"></a>
The name that you assigned the FAQ when you created or updated the FAQ\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[a-zA-Z0-9][a-zA-Z0-9_-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-kendra-faq-rolearn"></a>
The Amazon Resource Name \(ARN\) of a role with permission to access the S3 bucket that contains the FAQ\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Path`  <a name="cfn-kendra-faq-s3path"></a>
The Amazon Simple Storage Service \(Amazon S3\) location of the FAQ input data\.  
*Required*: Yes  
*Type*: [S3Path](aws-properties-kendra-faq-s3path.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-kendra-faq-tags"></a>
An array of key\-value pairs to apply to this resource  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: [TagList](aws-properties-kendra-faq-taglist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-kendra-faq-return-values"></a>

### Ref<a name="aws-resource-kendra-faq-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the FAQ identifier\. For example:

`{ "Ref": "<faq-id>|<index-id>" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-kendra-faq-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-kendra-faq-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
`arn:aws:kendra:us-west-2:111122223333:index/335c3741-41df-46a6-b5d3-61f85b787884/faq/f61995a6-cd5c-4e99-9cfc-58816d8bfaa7`

`Id`  <a name="Id-fn::getatt"></a>
The identifier for the FAQ\. For example:  
`f61995a6-cd5c-4e99-9cfc-58816d8bfaa7`