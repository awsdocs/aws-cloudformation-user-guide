# AWS::QuickSight::Analysis LongFormatText<a name="aws-properties-quicksight-analysis-longformattext"></a>

The text format for a subtitle\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-longformattext-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-longformattext-syntax.json"></a>

```
{
  "[PlainText](#cfn-quicksight-analysis-longformattext-plaintext)" : String,
  "[RichText](#cfn-quicksight-analysis-longformattext-richtext)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-longformattext-syntax.yaml"></a>

```
  [PlainText](#cfn-quicksight-analysis-longformattext-plaintext): String
  [RichText](#cfn-quicksight-analysis-longformattext-richtext): String
```

## Properties<a name="aws-properties-quicksight-analysis-longformattext-properties"></a>

`PlainText`  <a name="cfn-quicksight-analysis-longformattext-plaintext"></a>
Plain text format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RichText`  <a name="cfn-quicksight-analysis-longformattext-richtext"></a>
Rich text\. Examples of rich text include bold, underline, and italics\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)