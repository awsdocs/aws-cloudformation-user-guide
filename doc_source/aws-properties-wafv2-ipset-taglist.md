# AWS::WAFv2::IPSet TagList<a name="aws-properties-wafv2-ipset-taglist"></a>

Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.

## Syntax<a name="aws-properties-wafv2-ipset-taglist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-ipset-taglist-syntax.json"></a>

```
{
  "[TagList](#cfn-wafv2-ipset-taglist-taglist)" : [ [Tag](#aws-properties-wafv2-ipset-taglist), ... ]
}
```

### YAML<a name="aws-properties-wafv2-ipset-taglist-syntax.yaml"></a>

```
  [TagList](#cfn-wafv2-ipset-taglist-taglist): 
    - [Tag](#aws-properties-wafv2-ipset-taglist)
```

## Properties<a name="aws-properties-wafv2-ipset-taglist-properties"></a>

`TagList`  <a name="cfn-wafv2-ipset-taglist-taglist"></a>
Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.  
*Required*: No  
*Type*: [List](#aws-properties-wafv2-ipset-taglist) of [Tag](#aws-properties-wafv2-ipset-taglist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)