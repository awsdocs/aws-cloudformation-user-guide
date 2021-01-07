# AWS::WAFv2::RegexPatternSet<a name="aws-resource-wafv2-regexpatternset"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Use an [AWS::WAFv2::RegexPatternSet](#aws-resource-wafv2-regexpatternset) to have AWS WAF inspect a web request component for a specific set of regex patterns\. 

You use a regex pattern set by providing its Amazon Resource Name \(ARN\) to the rule statement `RegexPatternSetReferenceStatement`, when you add a rule to a rule group or web ACL\. 

## Syntax<a name="aws-resource-wafv2-regexpatternset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafv2-regexpatternset-syntax.json"></a>

```
{
  "Type" : "AWS::WAFv2::RegexPatternSet",
  "Properties" : {
      "[Description](#cfn-wafv2-regexpatternset-description)" : String,
      "[Name](#cfn-wafv2-regexpatternset-name)" : String,
      "[RegularExpressionList](#cfn-wafv2-regexpatternset-regularexpressionlist)" : [ String, ... ],
      "[Scope](#cfn-wafv2-regexpatternset-scope)" : String,
      "[Tags](#cfn-wafv2-regexpatternset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-wafv2-regexpatternset-syntax.yaml"></a>

```
Type: AWS::WAFv2::RegexPatternSet
Properties: 
  [Description](#cfn-wafv2-regexpatternset-description): String
  [Name](#cfn-wafv2-regexpatternset-name): String
  [RegularExpressionList](#cfn-wafv2-regexpatternset-regularexpressionlist): 
    - String
  [Scope](#cfn-wafv2-regexpatternset-scope): String
  [Tags](#cfn-wafv2-regexpatternset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-wafv2-regexpatternset-properties"></a>

`Description`  <a name="cfn-wafv2-regexpatternset-description"></a>
A friendly description of the set\. You cannot change the description of a set after you create it\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[\w+=:#@/\-,\.][\w+=:#@/\-,\.\s]+[\w+=:#@/\-,\.]$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-wafv2-regexpatternset-name"></a>
A friendly name of the set\. You cannot change the name after you create the set\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegularExpressionList`  <a name="cfn-wafv2-regexpatternset-regularexpressionlist"></a>
The regular expression patterns in the set\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-wafv2-regexpatternset-scope"></a>
Specifies whether this is for an AWS CloudFront distribution or for a regional application\. A regional application can be an Application Load Balancer \(ALB\), an Amazon API Gateway REST API, or an AWS AppSync GraphQL API\. Valid Values are `CLOUDFRONT` and `REGIONAL`\.  
For `CLOUDFRONT`, you must create your WAFv2 resources in the US East \(N\. Virginia\) Region, `us-east-1`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-wafv2-regexpatternset-tags"></a>
Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.  
To modify tags on existing resources, use the AWS WAF console or the APIs\. With AWS CloudFormation, you can only add tags to AWS WAF resources during resource creation\. 
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafv2-regexpatternset-return-values"></a>

### Ref<a name="aws-resource-wafv2-regexpatternset-return-values-ref"></a>

The `Ref` for the resource, containing the resource name, physical ID, and scope, formatted as follows: `name|id|scope`\.

For example: `my-webacl-name|1234a1a-a1b1-12a1-abcd-a123b123456|REGIONAL`

### Fn::GetAtt<a name="aws-resource-wafv2-regexpatternset-return-values-fn--getatt"></a>

#### <a name="aws-resource-wafv2-regexpatternset-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the regex pattern set\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the regex pattern set\.

## Examples<a name="aws-resource-wafv2-regexpatternset--examples"></a>



### Create a regex pattern set<a name="aws-resource-wafv2-regexpatternset--examples--Create_a_regex_pattern_set"></a>

The following shows an example regex pattern set specification\. 

#### JSON<a name="aws-resource-wafv2-regexpatternset--examples--Create_a_regex_pattern_set--json"></a>

```
"Description": "Create RegexPatternSet example",
  "Resources": {
    "ExampleRegexPatternSet": {
      "Type": "AWS::WAFv2::RegexPatternSet",
      "Properties": {
        "Name": "ExampleRegexPatternSet1",
        "Scope": "REGIONAL",
        "Description": "This is an example RegexPatternSet",
        "RegularExpressionList": [
          "^foobar$",
          "^example$"
        ]
      }
    }
  }
```

#### YAML<a name="aws-resource-wafv2-regexpatternset--examples--Create_a_regex_pattern_set--yaml"></a>

```
Description: Create RegexPatternSet example
Resources:
  ExampleRegexPatternSet:
    Type: AWS::WAFv2::RegexPatternSet
    Properties:
      Name: ExampleRegexPatternSet
      Scope: REGIONAL
      Description: This is an example RegexPatternSet
      RegularExpressionList:
        - ^foobar$
        - ^example$
```