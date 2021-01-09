# AWS::WAFv2::RuleGroup<a name="aws-resource-wafv2-rulegroup"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Use an [AWS::WAFv2::RuleGroup](#aws-resource-wafv2-rulegroup) to define a collection of rules for inspecting and controlling web requests\. You use a rule group in an [AWS::WAFv2::WebACL](aws-resource-wafv2-webacl.md) by providing its Amazon Resource Name \(ARN\) to the rule statement `RuleGroupReferenceStatement`, when you add rules to the web ACL\. 

When you create a rule group, you define an immutable capacity limit\. If you update a rule group, you must stay within the capacity\. This allows others to reuse the rule group with confidence in its capacity requirements\. 

**Note**  
You can only use up to 3 levels of nested rule statements when you manage your web ACLs and rule groups using AWS CloudFormation\. This limitation doesn't exist when you use the API and SDKs\. 

## Syntax<a name="aws-resource-wafv2-rulegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafv2-rulegroup-syntax.json"></a>

```
{
  "Type" : "AWS::WAFv2::RuleGroup",
  "Properties" : {
      "[Capacity](#cfn-wafv2-rulegroup-capacity)" : Integer,
      "[Description](#cfn-wafv2-rulegroup-description)" : String,
      "[Name](#cfn-wafv2-rulegroup-name)" : String,
      "[Rules](#cfn-wafv2-rulegroup-rules)" : [ Rule, ... ],
      "[Scope](#cfn-wafv2-rulegroup-scope)" : String,
      "[Tags](#cfn-wafv2-rulegroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VisibilityConfig](#cfn-wafv2-rulegroup-visibilityconfig)" : VisibilityConfig
    }
}
```

### YAML<a name="aws-resource-wafv2-rulegroup-syntax.yaml"></a>

```
Type: AWS::WAFv2::RuleGroup
Properties: 
  [Capacity](#cfn-wafv2-rulegroup-capacity): Integer
  [Description](#cfn-wafv2-rulegroup-description): String
  [Name](#cfn-wafv2-rulegroup-name): String
  [Rules](#cfn-wafv2-rulegroup-rules): 
    - Rule
  [Scope](#cfn-wafv2-rulegroup-scope): String
  [Tags](#cfn-wafv2-rulegroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VisibilityConfig](#cfn-wafv2-rulegroup-visibilityconfig): 
    VisibilityConfig
```

## Properties<a name="aws-resource-wafv2-rulegroup-properties"></a>

`Capacity`  <a name="cfn-wafv2-rulegroup-capacity"></a>
The web ACL capacity units \(WCUs\) required for this rule group\.  
When you create your own rule group, you define this, and you cannot change it after creation\. When you add or modify the rules in a rule group, AWS WAF enforces this limit\. You can check the capacity for a set of rules using CheckCapacity\.  
AWS WAF uses WCUs to calculate and control the operating resources that are used to run your rules, rule groups, and web ACLs\. AWS WAF calculates capacity differently for each rule type, to reflect the relative cost of each rule\. Simple rules that cost little to run use fewer WCUs than more complex rules that use more processing power\. Rule group capacity is fixed at creation, which helps users plan their web ACL WCU usage when they use a rule group\. The WCU limit for web ACLs is 1,500\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-wafv2-rulegroup-description"></a>
A friendly description of the rule group\. You cannot change the description of a rule group after you create it\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[\w+=:#@/\-,\.][\w+=:#@/\-,\.\s]+[\w+=:#@/\-,\.]$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-wafv2-rulegroup-name"></a>
A friendly name of the rule group\. You cannot change the name of a rule group after you create it\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rules`  <a name="cfn-wafv2-rulegroup-rules"></a>
The Rule statements used to identify the web requests that you want to allow, block, or count\. Each rule includes one top\-level statement that AWS WAF uses to identify matching web requests, and parameters that govern how AWS WAF handles them\.   
*Required*: No  
*Type*: List of [Rule](aws-properties-wafv2-rulegroup-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-wafv2-rulegroup-scope"></a>
Specifies whether this is for an AWS CloudFront distribution or for a regional application\. A regional application can be an Application Load Balancer \(ALB\), an Amazon API Gateway REST API, or an AWS AppSync GraphQL API\. Valid Values are `CLOUDFRONT` and `REGIONAL`\.  
For `CLOUDFRONT`, you must create your WAFv2 resources in the US East \(N\. Virginia\) Region, `us-east-1`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-wafv2-rulegroup-tags"></a>
Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.  
To modify tags on existing resources, use the AWS WAF console or the APIs\. With AWS CloudFormation, you can only add tags to AWS WAF resources during resource creation\. 
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisibilityConfig`  <a name="cfn-wafv2-rulegroup-visibilityconfig"></a>
Defines and enables Amazon CloudWatch metrics and web request sample collection\.   
*Required*: Yes  
*Type*: [VisibilityConfig](aws-properties-wafv2-rulegroup-visibilityconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafv2-rulegroup-return-values"></a>

### Ref<a name="aws-resource-wafv2-rulegroup-return-values-ref"></a>

The `Ref` for the resource, containing the resource name, physical ID, and scope, formatted as follows: `name|id|scope`\.

For example: `my-webacl-name|1234a1a-a1b1-12a1-abcd-a123b123456|REGIONAL`

### Fn::GetAtt<a name="aws-resource-wafv2-rulegroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-wafv2-rulegroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the rule group\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the rule group\.

## Examples<a name="aws-resource-wafv2-rulegroup--examples"></a>



### Create a rule group<a name="aws-resource-wafv2-rulegroup--examples--Create_a_rule_group"></a>

The following shows an example rule group specification\. 

#### JSON<a name="aws-resource-wafv2-rulegroup--examples--Create_a_rule_group--json"></a>

```
"Description": "Create RuleGroups",
  "Resources": {
      "SampleRuleGroup": {
          "Type": "AWS::WAFv2::RuleGroup",
          "Properties": {
              "Name": "SampleRuleGroup",
              "Scope": "REGIONAL",
              "Description": "SampleRuleGroup",
              "VisibilityConfig": {
                  "SampledRequestsEnabled": true,
                  "CloudWatchMetricsEnabled": true,
                  "MetricName": "SampleRuleGroupMetrics"
              },
              "Capacity": 1000,
              "Rules": [
                  {
                      "Name": "RuleOne",
                      "Priority": 1,
                      "Action": {
                          "Allow": {}
                      },
                      "VisibilityConfig": {
                          "SampledRequestsEnabled": true,
                          "CloudWatchMetricsEnabled": true,
                          "MetricName": "RuleOneMetric"
                      },
                      "Statement": {
                          "ByteMatchStatement": {
                              "FieldToMatch": {
                                  "AllQueryArguments": {}
                              },
                              "PositionalConstraint": "CONTAINS",
                              "SearchString": "testagent",
                              "TextTransformations": [
                                  {
                                      "Priority": 1,
                                      "Type": "HTML_ENTITY_DECODE"
                                  }
                              ]
                          }
                      }
                  },
                  {
                      "Name": "RuleTwo",
                      "Priority": 2,
                      "Action": {
                          "Block": {}
                      },
                      "VisibilityConfig": {
                          "SampledRequestsEnabled": true,
                          "CloudWatchMetricsEnabled": true,
                          "MetricName": "RuleTwoMetric"
                      },
                      "Statement": {
                          "ByteMatchStatement": {
                              "FieldToMatch": {
                                  "SingleHeader": {
                                      "Name": "haystack"
                                  }
                              },
                              "PositionalConstraint": "CONTAINS",
                              "SearchString": "badbot",
                              "TextTransformations": [
                                  {
                                      "Priority": 0,
                                      "Type": "NONE"
                                  }
                              ]
                          }
                      }
                  },
                  {
                      "Name": "RuleThree",
                      "Priority": 3,
                      "Action": {
                          "Count": {}
                      },
                      "VisibilityConfig": {
                          "SampledRequestsEnabled": true,
                          "CloudWatchMetricsEnabled": true,
                          "MetricName": "RuleThreeMetric"
                      },
                      "Statement": {
                          "ByteMatchStatement": {
                              "FieldToMatch": {
                                  "Body": {}
                              },
                              "PositionalConstraint": "CONTAINS",
                              "SearchString": "RegionOne",
                              "TextTransformations": [
                                  {
                                      "Priority": 0,
                                      "Type": "HTML_ENTITY_DECODE"
                                  }
                              ]
                          }
                      }
                  },
                  {
                      "Name": "RuleFour",
                      "Priority": 4,
                      "Action": {
                          "Allow": {}
                      },
                      "VisibilityConfig": {
                          "SampledRequestsEnabled": true,
                          "CloudWatchMetricsEnabled": true,
                          "MetricName": "RuleFourMetric"
                      },
                      "Statement": {
                          "SizeConstraintStatement": {
                              "ComparisonOperator": "GT",
                              "Size": 1000,
                              "FieldToMatch": {
                                  "UriPath": {}
                              },
                              "TextTransformations": [
                                  {
                                      "Priority": 0,
                                      "Type": "NONE"
                                  }
                              ]
                          }
                      }
                  }
              ]
          }
      }
  }
```

#### YAML<a name="aws-resource-wafv2-rulegroup--examples--Create_a_rule_group--yaml"></a>

```
Description: Create RuleGroups
  Resources:
    SampleRuleGroup:
      Type: 'AWS::WAFv2::RuleGroup'
      Properties:
        Name: SampleRuleGroup
        Scope: REGIONAL
        Description: SampleRuleGroup
        VisibilityConfig:
          SampledRequestsEnabled: true
          CloudWatchMetricsEnabled: true
          MetricName: SampleRuleGroupMetrics
        Capacity: 1000
        Rules:
          - Name: RuleOne
            Priority: 1
            Action:
              Allow: {}
            VisibilityConfig:
              SampledRequestsEnabled: true
              CloudWatchMetricsEnabled: true
              MetricName: RuleOneMetric
            Statement:
              ByteMatchStatement:
                FieldToMatch:
                  AllQueryArguments:
                    {}
                PositionalConstraint: CONTAINS
                SearchString: testagent
                TextTransformations:
                  - Priority: 1
                    Type: HTML_ENTITY_DECODE
          - Name: RuleTwo
            Priority: 2
            Action:
              Block: {}
            VisibilityConfig:
              SampledRequestsEnabled: true
              CloudWatchMetricsEnabled: true
              MetricName: RuleTwoMetric
            Statement:
              ByteMatchStatement:
                FieldToMatch:
                  SingleHeader:
                    Name: haystack
                PositionalConstraint: CONTAINS
                SearchString: badbot
                TextTransformations:
                  - Priority: 0
                    Type: NONE
          - Name: RuleThree
            Priority: 3
            Action:
              Count: {}
            VisibilityConfig:
              SampledRequestsEnabled: true
              CloudWatchMetricsEnabled: true
              MetricName: RuleThreeMetric
            Statement:
              ByteMatchStatement:
                FieldToMatch:
                  Body: {}
                PositionalConstraint: CONTAINS
                SearchString: RegionOne
                TextTransformations:
                  - Priority: 0
                    Type: HTML_ENTITY_DECODE
          - Name: RuleFour
            Priority: 4
            Action:
              Allow: {}
            VisibilityConfig:
              SampledRequestsEnabled: true
              CloudWatchMetricsEnabled: true
              MetricName: RuleFourMetric
            Statement:
              SizeConstraintStatement:
                ComparisonOperator: GT
                Size: 1000
                FieldToMatch:
                  UriPath: {}
                TextTransformations:
                  - Priority: 0
                    Type: NONE
```