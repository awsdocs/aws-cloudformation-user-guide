# AWS::WAFv2::RuleGroup<a name="aws-resource-wafv2-rulegroup"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Use an [AWS::WAFv2::RuleGroup](#aws-resource-wafv2-rulegroup) to define a collection of rules for inspecting and controlling web requests\. You use a rule group in an [AWS::WAFv2::WebACL](aws-resource-wafv2-webacl.md) by providing its Amazon Resource Name \(ARN\) to the rule statement `RuleGroupReferenceStatement`, when you add rules to the web ACL\. 

When you create a rule group, you define an immutable capacity limit\. If you update a rule group, you must stay within the capacity\. This allows others to reuse the rule group with confidence in its capacity requirements\. 

## Syntax<a name="aws-resource-wafv2-rulegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafv2-rulegroup-syntax.json"></a>

```
{
  "Type" : "AWS::WAFv2::RuleGroup",
  "Properties" : {
      "[AvailableLabels](#cfn-wafv2-rulegroup-availablelabels)" : [ LabelSummary, ... ],
      "[Capacity](#cfn-wafv2-rulegroup-capacity)" : Integer,
      "[ConsumedLabels](#cfn-wafv2-rulegroup-consumedlabels)" : [ LabelSummary, ... ],
      "[CustomResponseBodies](#cfn-wafv2-rulegroup-customresponsebodies)" : {Key : Value, ...},
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
  [AvailableLabels](#cfn-wafv2-rulegroup-availablelabels): 
    - LabelSummary
  [Capacity](#cfn-wafv2-rulegroup-capacity): Integer
  [ConsumedLabels](#cfn-wafv2-rulegroup-consumedlabels): 
    - LabelSummary
  [CustomResponseBodies](#cfn-wafv2-rulegroup-customresponsebodies): 
    Key : Value
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

`AvailableLabels`  <a name="cfn-wafv2-rulegroup-availablelabels"></a>
The labels that one or more rules in this rule group add to matching web requests\. These labels are defined in the `RuleLabels` for a `Rule`\.  
*Required*: No  
*Type*: List of [LabelSummary](aws-properties-wafv2-rulegroup-labelsummary.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Capacity`  <a name="cfn-wafv2-rulegroup-capacity"></a>
The web ACL capacity units \(WCUs\) required for this rule group\.  
When you create your own rule group, you define this, and you cannot change it after creation\. When you add or modify the rules in a rule group, AWS WAF enforces this limit\.   
 AWS WAF uses WCUs to calculate and control the operating resources that are used to run your rules, rule groups, and web ACLs\. AWS WAF calculates capacity differently for each rule type, to reflect the relative cost of each rule\. Simple rules that cost little to run use fewer WCUs than more complex rules that use more processing power\. Rule group capacity is fixed at creation, which helps users plan their web ACL WCU usage when they use a rule group\. The WCU limit for web ACLs is 1,500\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConsumedLabels`  <a name="cfn-wafv2-rulegroup-consumedlabels"></a>
The labels that one or more rules in this rule group match against in label match statements\. These labels are defined in a `LabelMatchStatement` specification, in the [Statement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-webacl-notstatement.html#cfn-wafv2-webacl-notstatement-statement) definition of a rule\.   
*Required*: No  
*Type*: List of [LabelSummary](aws-properties-wafv2-rulegroup-labelsummary.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomResponseBodies`  <a name="cfn-wafv2-rulegroup-customresponsebodies"></a>
A map of custom response keys and content bodies\. When you create a rule with a block action, you can send a custom response to the web request\. You define these for the rule group, and then use them in the rules that you define in the rule group\.   
For information about customizing web requests and responses, see [Customizing web requests and responses in AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-custom-request-response.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
For information about the limits on count and size for custom request and response settings, see [AWS WAF quotas](https://docs.aws.amazon.com/waf/latest/developerguide/limits.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: Map of [CustomResponseBody](aws-properties-wafv2-rulegroup-customresponsebody.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-wafv2-rulegroup-description"></a>
A description of the rule group that helps with identification\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[\w+=:#@/\-,\.][\w+=:#@/\-,\.\s]+[\w+=:#@/\-,\.]$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-wafv2-rulegroup-name"></a>
The name of the rule group\. You cannot change the name of a rule group after you create it\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Rules`  <a name="cfn-wafv2-rulegroup-rules"></a>
The rule statements used to identify the web requests that you want to allow, block, or count\. Each rule includes one top\-level statement that AWS WAF uses to identify matching web requests, and parameters that govern how AWS WAF handles them\.   
*Required*: No  
*Type*: List of [Rule](aws-properties-wafv2-rulegroup-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-wafv2-rulegroup-scope"></a>
Specifies whether this is for an Amazon CloudFront distribution or for a regional application\. A regional application can be an Application Load Balancer \(ALB\), an Amazon API Gateway REST API, an AWS AppSync GraphQL API, or an Amazon Cognito user pool\. Valid Values are `CLOUDFRONT` and `REGIONAL`\.  
For `CLOUDFRONT`, you must create your WAFv2 resources in the US East \(N\. Virginia\) Region, `us-east-1`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-wafv2-rulegroup-tags"></a>
Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.  
To modify tags on existing resources, use the AWS WAF APIs or command line interface\. With AWS CloudFormation, you can only add tags to AWS WAF resources during resource creation\. 
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

For example: `my-webacl-name|1234a1a-a1b1-12a1-abcd-a123b123456|REGIONAL`\.

### Fn::GetAtt<a name="aws-resource-wafv2-rulegroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-wafv2-rulegroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the rule group\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the rule group\.

`LabelNamespace`  <a name="LabelNamespace-fn::getatt"></a>
The label namespace prefix for this rule group\. All labels added by rules in this rule group have this prefix\.  
The syntax for the label namespace prefix for a rule group is the following: `awswaf:<account ID>:rule group:<rule group name>:`  
When a rule with a label matches a web request, AWS WAF adds the fully qualified label to the request\. A fully qualified label is made up of the label namespace from the rule group or web ACL where the rule is defined and the label from the rule, separated by a colon\.

## Examples<a name="aws-resource-wafv2-rulegroup--examples"></a>



### Create a rule group<a name="aws-resource-wafv2-rulegroup--examples--Create_a_rule_group_"></a>

The following shows an example rule group specification\. 

#### YAML<a name="aws-resource-wafv2-rulegroup--examples--Create_a_rule_group_--yaml"></a>

```
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
        CustomResponseBodies:
          CustomResponseBodyKey1:
            ContentType: TEXT_PLAIN
            Content: this is a plain text
          CustomResponseBodyKey2:
            ContentType: APPLICATION_JSON
            Content: '{"jsonfieldname": "jsonfieldvalue"}'
          CustomResponseBodyKey3:
            ContentType: TEXT_HTML
            Content: <html>HTML text content</html>
        Capacity: 1000
        Rules:
          - Name: RuleOne
            Priority: 1
            Action:
              Allow:
                CustomRequestHandling:
                  InsertHeaders:
                    - Name: AllowActionHeader1Name
                      Value: AllowActionHeader1Value
                    - Name: AllowActionHeader2Name
                      Value: AllowActionHeader2Value
            VisibilityConfig:
              SampledRequestsEnabled: true
              CloudWatchMetricsEnabled: true
              MetricName: RuleOneMetric
            Statement:
              ByteMatchStatement:
                FieldToMatch:
                  AllQueryArguments: {}
                PositionalConstraint: CONTAINS
                SearchString: testagent
                TextTransformations:
                  - Priority: 1
                    Type: HTML_ENTITY_DECODE
          - Name: RuleTwo
            Priority: 2
            Action:
              Block:
                CustomResponse:
                  ResponseCode: 503
                  CustomResponseBodyKey: CustomResponseBodyKey1
                  ResponseHeaders:
                    - Name: BlockActionHeader1Name
                      Value: BlockActionHeader1Value
                    - Name: BlockActionHeader2Name
                      Value: BlockActionHeader2Value
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
              Count:
                CustomRequestHandling:
                  InsertHeaders:
                    - Name: CountActionHeader1Name
                      Value: CountActionHeader1Value
                    - Name: CountActionHeader2Name
                      Value: CountActionHeader2Value
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

#### JSON<a name="aws-resource-wafv2-rulegroup--examples--Create_a_rule_group_--json"></a>

```
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
            "CustomResponseBodies": {
                "CustomResponseBodyKey1": {
                    "ContentType": "TEXT_PLAIN",
                    "Content": "this is a plain text"
                },
                "CustomResponseBodyKey2": {
                    "ContentType": "APPLICATION_JSON",
                    "Content": "{\"jsonfieldname\": \"jsonfieldvalue\"}"
                },
                "CustomResponseBodyKey3": {
                    "ContentType": "TEXT_HTML",
                    "Content": "<html>HTML text content</html>"
                }
            },              
            "Capacity": 1000,
            "Rules": [
                {
                    "Name": "RuleOne",
                    "Priority": 1,
                    "Action": {
                        "Allow": {
                            "CustomRequestHandling": {
                                "InsertHeaders": [
                                    {
                                        "Name": "AllowActionHeader1Name",
                                        "Value": "AllowActionHeader1Value"
                                    },
                                    {
                                        "Name": "AllowActionHeader2Name",
                                        "Value": "AllowActionHeader2Value"
                                    }
                                ]
                            }
                        }
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
                        "Block": {
                            "CustomResponse": {
                                "ResponseCode": 503,
                                "CustomResponseBodyKey": "CustomResponseBodyKey1",
                                "ResponseHeaders": [
                                    {
                                        "Name": "BlockActionHeader1Name",
                                        "Value": "BlockActionHeader1Value"
                                    },
                                    {
                                        "Name": "BlockActionHeader2Name",
                                        "Value": "BlockActionHeader2Value"
                                    }
                                ]
                            }
                        }
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
                        "Count": {
                            "CustomRequestHandling": {
                                "InsertHeaders": [
                                    {
                                        "Name": "CountActionHeader1Name",
                                        "Value": "CountActionHeader1Value"
                                    },
                                    {
                                        "Name": "CountActionHeader2Name",
                                        "Value": "CountActionHeader2Value"
                                    }
                                ]
                            }
                        }
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
```