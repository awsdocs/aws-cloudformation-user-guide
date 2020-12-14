# AWS::Kendra::Index TagList<a name="aws-properties-kendra-index-taglist"></a>

A list of key\-value pairs that identify the index\. You can use tags to identify and organize your resources and to control access to resources\.

## Syntax<a name="aws-properties-kendra-index-taglist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-index-taglist-syntax.json"></a>

```
{
  "[TagList](#cfn-kendra-index-taglist-taglist)" : [ Tag, ... ]
}
```

### YAML<a name="aws-properties-kendra-index-taglist-syntax.yaml"></a>

```
  [TagList](#cfn-kendra-index-taglist-taglist): 
    - Tag
```

## Properties<a name="aws-properties-kendra-index-taglist-properties"></a>

`TagList`  <a name="cfn-kendra-index-taglist-taglist"></a>
A key\-value pair attached to the data source\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-index-taglist) of [Tag](#aws-properties-kendra-index-taglist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)