# AWS::QuickSight::Dashboard LongFormatText<a name="aws-properties-quicksight-dashboard-longformattext"></a>

The text format for a subtitle\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-longformattext-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-longformattext-syntax.json"></a>

```
{
  "[PlainText](#cfn-quicksight-dashboard-longformattext-plaintext)" : String,
  "[RichText](#cfn-quicksight-dashboard-longformattext-richtext)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-longformattext-syntax.yaml"></a>

```
  [PlainText](#cfn-quicksight-dashboard-longformattext-plaintext): String
  [RichText](#cfn-quicksight-dashboard-longformattext-richtext): String
```

## Properties<a name="aws-properties-quicksight-dashboard-longformattext-properties"></a>

`PlainText`  <a name="cfn-quicksight-dashboard-longformattext-plaintext"></a>
Plain text format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RichText`  <a name="cfn-quicksight-dashboard-longformattext-richtext"></a>
Rich text\. Examples of rich text include bold, underline, and italics\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)