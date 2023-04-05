# AWS::QuickSight::Template ShortFormatText<a name="aws-properties-quicksight-template-shortformattext"></a>

The text format for the title\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-shortformattext-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-shortformattext-syntax.json"></a>

```
{
  "[PlainText](#cfn-quicksight-template-shortformattext-plaintext)" : String,
  "[RichText](#cfn-quicksight-template-shortformattext-richtext)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-shortformattext-syntax.yaml"></a>

```
  [PlainText](#cfn-quicksight-template-shortformattext-plaintext): String
  [RichText](#cfn-quicksight-template-shortformattext-richtext): String
```

## Properties<a name="aws-properties-quicksight-template-shortformattext-properties"></a>

`PlainText`  <a name="cfn-quicksight-template-shortformattext-plaintext"></a>
Plain text format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RichText`  <a name="cfn-quicksight-template-shortformattext-richtext"></a>
Rich text\. Examples of rich text include bold, underline, and italics\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)