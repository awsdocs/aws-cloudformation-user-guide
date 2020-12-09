# AWS::Kendra::Faq TagList<a name="aws-properties-kendra-faq-taglist"></a>

A list of key\-value pairs that identify the FAQ\. You can use tags to identify and organize your resources and to control access to resources\.

## Syntax<a name="aws-properties-kendra-faq-taglist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-faq-taglist-syntax.json"></a>

```
{
  "[TagList](#cfn-kendra-faq-taglist-taglist)" : [ Tag, ... ]
}
```

### YAML<a name="aws-properties-kendra-faq-taglist-syntax.yaml"></a>

```
  [TagList](#cfn-kendra-faq-taglist-taglist): 
    - Tag
```

## Properties<a name="aws-properties-kendra-faq-taglist-properties"></a>

`TagList`  <a name="cfn-kendra-faq-taglist-taglist"></a>
A key\-value pair attached to the FAQ\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-faq-taglist) of [Tag](#aws-properties-kendra-faq-taglist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)