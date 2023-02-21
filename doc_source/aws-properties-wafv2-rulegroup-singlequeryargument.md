# AWS::WAFv2::RuleGroup SingleQueryArgument<a name="aws-properties-wafv2-rulegroup-singlequeryargument"></a>

Inspect one query argument in the web request, identified by name, for example *UserName* or *SalesRegion*\. The name isn't case sensitive\. 

This is used to indicate the web request component to inspect, in the [FieldToMatch](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-xssmatchstatement.html#cfn-wafv2-rulegroup-xssmatchstatement-fieldtomatch) specification\. 

Example JSON: `"SingleQueryArgument": { "Name": "myArgument" }` 

## Syntax<a name="aws-properties-wafv2-rulegroup-singlequeryargument-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-singlequeryargument-syntax.json"></a>

```
{
  "[Name](#cfn-wafv2-rulegroup-singlequeryargument-name)" : String
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-singlequeryargument-syntax.yaml"></a>

```
  [Name](#cfn-wafv2-rulegroup-singlequeryargument-name): String
```

## Properties<a name="aws-properties-wafv2-rulegroup-singlequeryargument-properties"></a>

`Name`  <a name="cfn-wafv2-rulegroup-singlequeryargument-name"></a>
The name of the query argument to inspect\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)