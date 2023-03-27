# AWS::WAFv2::WebACL<a name="aws-resource-wafv2-webacl"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Use an [AWS::WAFv2::WebACL](#aws-resource-wafv2-webacl) to define a collection of rules to use to inspect and control web requests\. Each rule has an action defined \(allow, block, or count\) for requests that match the statement of the rule\. In the web ACL, you specify a default action to take \(allow, block\) for any request that doesn't match any of the rules\. The rules in a web ACL can contain rule statements that you define explicitly and rule statements that reference rule groups and managed rule groups\. You can associate a web ACL with one or more AWS resources to protect\. The resources can be an Amazon CloudFront distribution, an Amazon API Gateway REST API, an Application Load Balancer, an AWS AppSync GraphQL API, or an Amazon Cognito user pool\. 

## Syntax<a name="aws-resource-wafv2-webacl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafv2-webacl-syntax.json"></a>

```
{
  "Type" : "AWS::WAFv2::WebACL",
  "Properties" : {
      "[CaptchaConfig](#cfn-wafv2-webacl-captchaconfig)" : CaptchaConfig,
      "[ChallengeConfig](#cfn-wafv2-webacl-challengeconfig)" : ChallengeConfig,
      "[CustomResponseBodies](#cfn-wafv2-webacl-customresponsebodies)" : {Key : Value, ...},
      "[DefaultAction](#cfn-wafv2-webacl-defaultaction)" : DefaultAction,
      "[Description](#cfn-wafv2-webacl-description)" : String,
      "[Name](#cfn-wafv2-webacl-name)" : String,
      "[Rules](#cfn-wafv2-webacl-rules)" : [ Rule, ... ],
      "[Scope](#cfn-wafv2-webacl-scope)" : String,
      "[Tags](#cfn-wafv2-webacl-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TokenDomains](#cfn-wafv2-webacl-tokendomains)" : [ String, ... ],
      "[VisibilityConfig](#cfn-wafv2-webacl-visibilityconfig)" : VisibilityConfig
    }
}
```

### YAML<a name="aws-resource-wafv2-webacl-syntax.yaml"></a>

```
Type: AWS::WAFv2::WebACL
Properties: 
  [CaptchaConfig](#cfn-wafv2-webacl-captchaconfig): 
    CaptchaConfig
  [ChallengeConfig](#cfn-wafv2-webacl-challengeconfig): 
    ChallengeConfig
  [CustomResponseBodies](#cfn-wafv2-webacl-customresponsebodies): 
    Key : Value
  [DefaultAction](#cfn-wafv2-webacl-defaultaction): 
    DefaultAction
  [Description](#cfn-wafv2-webacl-description): String
  [Name](#cfn-wafv2-webacl-name): String
  [Rules](#cfn-wafv2-webacl-rules): 
    - Rule
  [Scope](#cfn-wafv2-webacl-scope): String
  [Tags](#cfn-wafv2-webacl-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TokenDomains](#cfn-wafv2-webacl-tokendomains): 
    - String
  [VisibilityConfig](#cfn-wafv2-webacl-visibilityconfig): 
    VisibilityConfig
```

## Properties<a name="aws-resource-wafv2-webacl-properties"></a>

`CaptchaConfig`  <a name="cfn-wafv2-webacl-captchaconfig"></a>
Specifies how AWS WAF should handle `CAPTCHA` evaluations for rules that don't have their own `CaptchaConfig` settings\. If you don't specify this, AWS WAF uses its default settings for `CaptchaConfig`\.   
*Required*: No  
*Type*: [CaptchaConfig](aws-properties-wafv2-webacl-captchaconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChallengeConfig`  <a name="cfn-wafv2-webacl-challengeconfig"></a>
Specifies how AWS WAF should handle challenge evaluations for rules that don't have their own `ChallengeConfig` settings\. If you don't specify this, AWS WAF uses its default settings for `ChallengeConfig`\.   
*Required*: No  
*Type*: [ChallengeConfig](aws-properties-wafv2-webacl-challengeconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomResponseBodies`  <a name="cfn-wafv2-webacl-customresponsebodies"></a>
A map of custom response keys and content bodies\. When you create a rule with a block action, you can send a custom response to the web request\. You define these for the web ACL, and then use them in the rules and default actions that you define in the web ACL\.   
For information about customizing web requests and responses, see [Customizing web requests and responses in AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-custom-request-response.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
For information about the limits on count and size for custom request and response settings, see [AWS WAF quotas](https://docs.aws.amazon.com/waf/latest/developerguide/limits.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: Map of [CustomResponseBody](aws-properties-wafv2-webacl-customresponsebody.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultAction`  <a name="cfn-wafv2-webacl-defaultaction"></a>
The action to perform if none of the `Rules` contained in the `WebACL` match\.   
*Required*: Yes  
*Type*: [DefaultAction](aws-properties-wafv2-webacl-defaultaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-wafv2-webacl-description"></a>
A description of the web ACL that helps with identification\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[\w+=:#@/\-,\.][\w+=:#@/\-,\.\s]+[\w+=:#@/\-,\.]$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-wafv2-webacl-name"></a>
The name of the web ACL\. You cannot change the name of a web ACL after you create it\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Rules`  <a name="cfn-wafv2-webacl-rules"></a>
The rule statements used to identify the web requests that you want to allow, block, or count\. Each rule includes one top\-level statement that AWS WAF uses to identify matching web requests, and parameters that govern how AWS WAF handles them\.   
*Required*: No  
*Type*: List of [Rule](aws-properties-wafv2-webacl-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-wafv2-webacl-scope"></a>
Specifies whether this is for an Amazon CloudFront distribution or for a regional application\. A regional application can be an Application Load Balancer \(ALB\), an Amazon API Gateway REST API, an AWS AppSync GraphQL API, or an Amazon Cognito user pool\. Valid Values are `CLOUDFRONT` and `REGIONAL`\.  
For `CLOUDFRONT`, you must create your WAFv2 resources in the US East \(N\. Virginia\) Region, `us-east-1`\.
For information about how to define the association of the web ACL with your resource, see [AWS::WAFv2::WebACLAssociation](aws-resource-wafv2-webaclassociation.md)\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-wafv2-webacl-tags"></a>
Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.  
To modify tags on existing resources, use the AWS WAF APIs or command line interface\. With AWS CloudFormation, you can only add tags to AWS WAF resources during resource creation\. 
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenDomains`  <a name="cfn-wafv2-webacl-tokendomains"></a>
Specifies the domains that AWS WAF should accept in a web request token\. This enables the use of tokens across multiple protected websites\. When AWS WAF provides a token, it uses the domain of the AWS resource that the web ACL is protecting\. If you don't specify a list of token domains, AWS WAF accepts tokens only for the domain of the protected resource\. With a token domain list, AWS WAF accepts the resource's host domain plus all domains in the token domain list, including their prefixed subdomains\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisibilityConfig`  <a name="cfn-wafv2-webacl-visibilityconfig"></a>
Defines and enables Amazon CloudWatch metrics and web request sample collection\.   
*Required*: Yes  
*Type*: [VisibilityConfig](aws-properties-wafv2-webacl-visibilityconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafv2-webacl-return-values"></a>

### Ref<a name="aws-resource-wafv2-webacl-return-values-ref"></a>

The `Ref` for the resource, containing the resource name, physical ID, and scope, formatted as follows: `name|id|scope`\.

For example: `my-webacl-name|1234a1a-a1b1-12a1-abcd-a123b123456|REGIONAL`\.

### Fn::GetAtt<a name="aws-resource-wafv2-webacl-return-values-fn--getatt"></a>

#### <a name="aws-resource-wafv2-webacl-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the web ACL\.

`Capacity`  <a name="Capacity-fn::getatt"></a>
The web ACL capacity units \(WCUs\) currently being used by this web ACL\.   
AWS WAF uses WCUs to calculate and control the operating resources that are used to run your rules, rule groups, and web ACLs\. AWS WAF calculates capacity differently for each rule type, to reflect the relative cost of each rule\. Simple rules that cost little to run use fewer WCUs than more complex rules that use more processing power\. Rule group capacity is fixed at creation, which helps users plan their web ACL WCU usage when they use a rule group\. The WCU limit for web ACLs is 1,500\. 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the web ACL\.

`LabelNamespace`  <a name="LabelNamespace-fn::getatt"></a>
The label namespace prefix for this web ACL\. All labels added by rules in this web ACL have this prefix\.  
The syntax for the label namespace prefix for a web ACL is the following: `awswaf:<account ID>:webacl:<web ACL name>:`  
When a rule with a label matches a web request, AWS WAF adds the fully qualified label to the request\. A fully qualified label is made up of the label namespace from the rule group or web ACL where the rule is defined and the label from the rule, separated by a colon\.

## Examples<a name="aws-resource-wafv2-webacl--examples"></a>



### Create a web ACL with custom request and response handling<a name="aws-resource-wafv2-webacl--examples--Create_a_web_ACL_with_custom_request_and_response_handling"></a>

The following shows an example web ACL specification\. This example includes custom request and response configurations\.

#### YAML<a name="aws-resource-wafv2-webacl--examples--Create_a_web_ACL_with_custom_request_and_response_handling--yaml"></a>

```
 ExampleWebACL:
    Type: 'AWS::WAFv2::WebACL'
    Properties:
      Name: ExampleWebACL1
      Scope: REGIONAL
      Description: This is an example WebACL
      DefaultAction:
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
        MetricName: ExampleWebACLMetric
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
      Rules:
        - Name: RuleWithAWSManagedRules
          Priority: 0
          OverrideAction:
            Count: {}
          VisibilityConfig:
            SampledRequestsEnabled: true
            CloudWatchMetricsEnabled: true
            MetricName: RuleWithAWSManagedRulesMetric
          Statement:
            ManagedRuleGroupStatement:
              VendorName: AWS
              Name: AWSManagedRulesCommonRuleSet
              ExcludedRules: []
        - Name: BlockXssAttack
          Priority: 1
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
            MetricName: BlockXssAttackMetric
          Statement:
            XssMatchStatement:
              FieldToMatch:
                AllQueryArguments: {}
              TextTransformations:
                - Priority: 1
                  Type: NONE
```

#### JSON<a name="aws-resource-wafv2-webacl--examples--Create_a_web_ACL_with_custom_request_and_response_handling--json"></a>

```
 "ExampleWebACL": {
      "Type": "AWS::WAFv2::WebACL",
      "Properties": {
        "Name": "ExampleWebACL1",
        "Scope": "REGIONAL",
        "Description": "This is an example WebACL",
        "DefaultAction": {
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
          "MetricName": "ExampleWebACLMetric"
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
        "Rules": [
          {
            "Name": "RuleWithAWSManagedRules",
            "Priority": 0,
            "OverrideAction": {
              "Count": {}
            },
            "VisibilityConfig": {
              "SampledRequestsEnabled": true,
              "CloudWatchMetricsEnabled": true,
              "MetricName": "RuleWithAWSManagedRulesMetric"
            },
            "Statement": {
              "ManagedRuleGroupStatement": {
            "VendorName": "AWS",
                "Name": "AWSManagedRulesCommonRuleSet",
                "ExcludedRules": []
              }
            }
          },
          {
            "Name": "BlockXssAttack",
            "Priority": 1,
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
              "MetricName": "BlockXssAttackMetric"
            },
            "Statement": {
              "XssMatchStatement": {
                "FieldToMatch": {
                  "AllQueryArguments": {}
                },
                "TextTransformations": [
                  {
                    "Priority": 1,
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

### Create a web ACL with JSON body parsing<a name="aws-resource-wafv2-webacl--examples--Create_a_web_ACL_with_JSON_body_parsing"></a>

The following shows an example web ACL specification\. This example includes inspection of the web request body as JSON\.

#### YAML<a name="aws-resource-wafv2-webacl--examples--Create_a_web_ACL_with_JSON_body_parsing--yaml"></a>

```
  ExampleWebACL:
    Type: 'AWS::WAFv2::WebACL'
    Properties:
      Name: TestingJsonBody
      Scope: REGIONAL
      Description: WebACL for JsonBody Testing
      DefaultAction:
        Allow: {}
      VisibilityConfig:
        SampledRequestsEnabled: true
        CloudWatchMetricsEnabled: true
        MetricName: ExampleWebACLMetric
      Rules:
        - Name: TestJsonBodyRule
          Priority: 0
          Action:
            Block: {}
          VisibilityConfig:
            SampledRequestsEnabled: true
            CloudWatchMetricsEnabled: true
            MetricName: JsonBodyMatchMetric
          Statement:
            ByteMatchStatement:
              FieldToMatch:
                JsonBody:
                  MatchPattern:
                    IncludedPaths:
                      - /foo
                      - /bar
                  MatchScope: VALUE
                  InvalidFallbackBehavior: MATCH
              PositionalConstraint: EXACTLY
              SearchString: BadBot
              TextTransformations:
                - Type: NONE
                  Priority: 0
```

#### JSON<a name="aws-resource-wafv2-webacl--examples--Create_a_web_ACL_with_JSON_body_parsing--json"></a>

```
  "ExampleWebACL": {
    "Type": "AWS::WAFv2::WebACL",
    "Properties": {
      "Name": "TestingJsonBody",
      "Scope": "REGIONAL",
      "DefaultAction": 
       {
        "Allow": 
         {}
       },
      "Description": "WebACL for JsonBody Testing",
      "Rules": [
      {
        "Name": "TestJsonBodyRule",
        "Priority": 1,
        "Statement": {
          "ByteMatchStatement": {
            "SearchString": "BadBot",
            "FieldToMatch": {
              "JsonBody": {
                "MatchPattern": {
                  "IncludedPaths": [
                    "/foo", "/bar"
                  ]
                },
                "MatchScope": "VALUE",  
                "InvalidFallbackBehavior": "MATCH"
               }
            },
            "TextTransformations": [
              {
                "Priority": 1,
                "Type": "NONE"
              }
            ],
            "PositionalConstraint": "EXACTLY"
          }
        },
        "Action": {
          "Block": {}
        },
        "VisibilityConfig": {
             "SampledRequestsEnabled": true,
             "CloudWatchMetricsEnabled": true,
             "MetricName": "JsonBodyMatchMetric"
         }
      } ],
      "VisibilityConfig": {
         "SampledRequestsEnabled": true,
         "CloudWatchMetricsEnabled": true,
         "MetricName": "TestingJsonBodyMetric"
      }
    }
  }
```