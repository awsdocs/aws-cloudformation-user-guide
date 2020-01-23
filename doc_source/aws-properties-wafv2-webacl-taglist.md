# AWS::WAFv2::WebACL TagList<a name="aws-properties-wafv2-webacl-taglist"></a>

Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.

## Syntax<a name="aws-properties-wafv2-webacl-taglist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-taglist-syntax.json"></a>

```
{
  "[TagList](#cfn-wafv2-webacl-taglist-taglist)" : [ [Tag](#aws-properties-wafv2-webacl-taglist), ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-taglist-syntax.yaml"></a>

```
  [TagList](#cfn-wafv2-webacl-taglist-taglist): 
    - [Tag](#aws-properties-wafv2-webacl-taglist)
```

## Properties<a name="aws-properties-wafv2-webacl-taglist-properties"></a>

`TagList`  <a name="cfn-wafv2-webacl-taglist-taglist"></a>
Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.  
*Required*: No  
*Type*: [List](#aws-properties-wafv2-webacl-taglist) of [Tag](#aws-properties-wafv2-webacl-taglist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)