# AWS::Kendra::Faq S3Path<a name="aws-properties-kendra-faq-s3path"></a>

Information required to find a specific file in an Amazon S3 bucket\.

## Syntax<a name="aws-properties-kendra-faq-s3path-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-faq-s3path-syntax.json"></a>

```
{
  "[Bucket](#cfn-kendra-faq-s3path-bucket)" : String,
  "[Key](#cfn-kendra-faq-s3path-key)" : String
}
```

### YAML<a name="aws-properties-kendra-faq-s3path-syntax.yaml"></a>

```
  [Bucket](#cfn-kendra-faq-s3path-bucket): String
  [Key](#cfn-kendra-faq-s3path-key): String
```

## Properties<a name="aws-properties-kendra-faq-s3path-properties"></a>

`Bucket`  <a name="cfn-kendra-faq-s3path-bucket"></a>
The name of the S3 bucket that contains the file\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `[a-z0-9][\.\-a-z0-9]{1,61}[a-z0-9]`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Key`  <a name="cfn-kendra-faq-s3path-key"></a>
The name of the file\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)