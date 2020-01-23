# AWS::WAFv2::WebACL SingleQueryArgument<a name="aws-properties-wafv2-webacl-singlequeryargument"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

One query argument in a web request, identified by name, for example *UserName* or *SalesRegion*\. The name can be up to 30 characters long and isn't case sensitive\. 

This is used only to indicate the web request component for AWS WAF to inspect, in the `FieldToMatch` setting of a rule statement\. 

## Syntax<a name="aws-properties-wafv2-webacl-singlequeryargument-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-singlequeryargument-syntax.json"></a>

```
{
  "[Name](#cfn-wafv2-webacl-singlequeryargument-name)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-singlequeryargument-syntax.yaml"></a>

```
  [Name](#cfn-wafv2-webacl-singlequeryargument-name): String
```

## Properties<a name="aws-properties-wafv2-webacl-singlequeryargument-properties"></a>

`Name`  <a name="cfn-wafv2-webacl-singlequeryargument-name"></a>
The name of the query argument to inspect\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)