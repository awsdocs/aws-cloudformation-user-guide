# AWS::WAFv2::WebACL<a name="aws-resource-wafv2-webacl"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Use an [AWS::WAFv2::WebACL](#aws-resource-wafv2-webacl) to define a collection of rules to use to inspect and control web requests\. Each rule has an action defined \(allow, block, or count\) for requests that match the statement of the rule\. In the web ACL, you assign a default action to take \(allow, block\) for any request that does not match any of the rules\. The rules in a web ACL can contain rule statements that you define explicitly and rule statements that reference rule groups and managed rule groups\. You can associate a web ACL with one or more AWS resources to protect\. The resources can be an Amazon CloudFront distribution, an Amazon API Gateway REST API, an Application Load Balancer, or an AWS AppSync GraphQL API\. 

**Note**  
You can only use up to 3 levels of nested rule statements when you manage your web ACLs and rule groups using AWS CloudFormation\. This limitation doesn't exist when you use the API and SDKs\. 

## Syntax<a name="aws-resource-wafv2-webacl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafv2-webacl-syntax.json"></a>

```
{
  "Type" : "AWS::WAFv2::WebACL",
  "Properties" : {
      "[DefaultAction](#cfn-wafv2-webacl-defaultaction)" : DefaultAction,
      "[Description](#cfn-wafv2-webacl-description)" : String,
      "[Name](#cfn-wafv2-webacl-name)" : String,
      "[Rules](#cfn-wafv2-webacl-rules)" : [ Rule, ... ],
      "[Scope](#cfn-wafv2-webacl-scope)" : String,
      "[Tags](#cfn-wafv2-webacl-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VisibilityConfig](#cfn-wafv2-webacl-visibilityconfig)" : VisibilityConfig
    }
}
```

### YAML<a name="aws-resource-wafv2-webacl-syntax.yaml"></a>

```
Type: AWS::WAFv2::WebACL
Properties: 
  [DefaultAction](#cfn-wafv2-webacl-defaultaction): 
    DefaultAction
  [Description](#cfn-wafv2-webacl-description): String
  [Name](#cfn-wafv2-webacl-name): String
  [Rules](#cfn-wafv2-webacl-rules): 
    - Rule
  [Scope](#cfn-wafv2-webacl-scope): String
  [Tags](#cfn-wafv2-webacl-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VisibilityConfig](#cfn-wafv2-webacl-visibilityconfig): 
    VisibilityConfig
```

## Properties<a name="aws-resource-wafv2-webacl-properties"></a>

`DefaultAction`  <a name="cfn-wafv2-webacl-defaultaction"></a>
The action to perform if none of the `Rules` contained in the `WebACL` match\.   
*Required*: Yes  
*Type*: [DefaultAction](aws-properties-wafv2-webacl-defaultaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-wafv2-webacl-description"></a>
A friendly description of the Web ACL\. You cannot change the description of a Web ACL after you create it\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[\w+=:#@/\-,\.][\w+=:#@/\-,\.\s]+[\w+=:#@/\-,\.]$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-wafv2-webacl-name"></a>
A friendly name of the Web ACL\. You cannot change the name of a Web ACL after you create it\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rules`  <a name="cfn-wafv2-webacl-rules"></a>
The Rule statements used to identify the web requests that you want to allow, block, or count\. Each rule includes one top\-level statement that AWS WAF uses to identify matching web requests, and parameters that govern how AWS WAF handles them\.   
*Required*: No  
*Type*: List of [Rule](aws-properties-wafv2-webacl-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-wafv2-webacl-scope"></a>
Specifies whether this is for an AWS CloudFront distribution or for a regional application\. A regional application can be an Application Load Balancer \(ALB\), an Amazon API Gateway REST API, or an AWS AppSync GraphQL API\. Valid Values are `CLOUDFRONT` and `REGIONAL`\.  
For `CLOUDFRONT`, you must create your WAFv2 resources in the US East \(N\. Virginia\) Region, `us-east-1`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-wafv2-webacl-tags"></a>
Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.  
To modify tags on existing resources, use the AWS WAF console or the APIs\. With AWS CloudFormation, you can only add tags to AWS WAF resources during resource creation\. 
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisibilityConfig`  <a name="cfn-wafv2-webacl-visibilityconfig"></a>
Defines and enables Amazon CloudWatch metrics and web request sample collection\.   
*Required*: Yes  
*Type*: [VisibilityConfig](aws-properties-wafv2-webacl-visibilityconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafv2-webacl-return-values"></a>

### Ref<a name="aws-resource-wafv2-webacl-return-values-ref"></a>

The `Ref` for the resource, containing the resource name, physical ID, and scope, formatted as follows: `name|id|scope`\.

For example: `my-webacl-name|1234a1a-a1b1-12a1-abcd-a123b123456|REGIONAL`

### Fn::GetAtt<a name="aws-resource-wafv2-webacl-return-values-fn--getatt"></a>

#### <a name="aws-resource-wafv2-webacl-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the web ACL\.

`Capacity`  <a name="Capacity-fn::getatt"></a>
The current web ACL capacity \(WCU\) usage by the web ACL\. 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the web ACL\.

## Examples<a name="aws-resource-wafv2-webacl--examples"></a>



### Create a web ACL<a name="aws-resource-wafv2-webacl--examples--Create_a_web_ACL"></a>

The following shows an example web ACL specification\. 

#### YAML<a name="aws-resource-wafv2-webacl--examples--Create_a_web_ACL--yaml"></a>

```
Description: Create WebACL example
Resources:
  ExampleWebACL:
    Type: AWS::WAFv2::WebACL
    Properties:
      Name: ExampleWebACL
      Scope: REGIONAL
      Description: This is an example WebACL
      DefaultAction:
        Allow: {}
      VisibilityConfig:
        SampledRequestsEnabled: true
        CloudWatchMetricsEnabled: true
        MetricName: ExampleWebACLMetric
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
            Block: {}
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

#### JSON<a name="aws-resource-wafv2-webacl--examples--Create_a_web_ACL--json"></a>

```
"Description": "Create WebACL example",
  "Resources": {
    "ExampleWebACL": {
      "Type": "AWS::WAFv2::WebACL",
      "Properties": {
        "Name": "ExampleWebACL1",
        "Scope": "REGIONAL",
        "Description": "This is an example WebACL",
        "DefaultAction": {
          "Allow": {}
        },
        "VisibilityConfig": {
          "SampledRequestsEnabled": true,
          "CloudWatchMetricsEnabled": true,
          "MetricName": "ExampleWebACLMetric"
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
              "Block": {}
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
  }
```