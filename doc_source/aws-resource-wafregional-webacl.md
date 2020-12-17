# AWS::WAFRegional::WebACL<a name="aws-resource-wafregional-webacl"></a>

Contains the `Rules` that identify the requests that you want to allow, block, or count\. In a `WebACL`, you also specify a default action \(`ALLOW` or `BLOCK`\), and the action for each `Rule` that you add to a `WebACL`, for example, block requests from specified IP addresses or block requests from specified referrers\. If you add more than one `Rule` to a `WebACL`, a request needs to match only one of the specifications to be allowed, blocked, or counted\.

To identify the requests that you want AWS WAF to filter, you associate the `WebACL` with an API Gateway API or an Application Load Balancer\. 

## Syntax<a name="aws-resource-wafregional-webacl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-webacl-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::WebACL",
  "Properties" : {
      "[DefaultAction](#cfn-wafregional-webacl-defaultaction)" : Action,
      "[MetricName](#cfn-wafregional-webacl-metricname)" : String,
      "[Name](#cfn-wafregional-webacl-name)" : String,
      "[Rules](#cfn-wafregional-webacl-rules)" : [ Rule, ... ]
    }
}
```

### YAML<a name="aws-resource-wafregional-webacl-syntax.yaml"></a>

```
Type: AWS::WAFRegional::WebACL
Properties: 
  [DefaultAction](#cfn-wafregional-webacl-defaultaction): 
    Action
  [MetricName](#cfn-wafregional-webacl-metricname): String
  [Name](#cfn-wafregional-webacl-name): String
  [Rules](#cfn-wafregional-webacl-rules): 
    - Rule
```

## Properties<a name="aws-resource-wafregional-webacl-properties"></a>

`DefaultAction`  <a name="cfn-wafregional-webacl-defaultaction"></a>
The action to perform if none of the `Rules` contained in the `WebACL` match\. The action is specified by the `WafAction` object\.  
*Required*: Yes  
*Type*: [Action](aws-properties-wafregional-webacl-action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-wafregional-webacl-metricname"></a>
A friendly name or description for the metrics for this `WebACL`\. The name can contain only alphanumeric characters \(A\-Z, a\-z, 0\-9\), with maximum length 128 and minimum length one\. It can't contain whitespace or metric names reserved for AWS WAF, including "All" and "Default\_Action\." You can't change `MetricName` after you create the `WebACL`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-wafregional-webacl-name"></a>
A friendly name or description of the `WebACL`\. You can't change the name of a `WebACL` after you create it\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Rules`  <a name="cfn-wafregional-webacl-rules"></a>
An array that contains the action for each `Rule` in a `WebACL`, the priority of the `Rule`, and the ID of the `Rule`\.  
*Required*: No  
*Type*: List of [Rule](aws-properties-wafregional-webacl-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafregional-webacl-return-values"></a>

### Ref<a name="aws-resource-wafregional-webacl-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-wafregional-webacl--examples"></a>



### Create a Web ACL<a name="aws-resource-wafregional-webacl--examples--Create_a_Web_ACL"></a>

The following example defines a web ACL that allows, by default, any web request\. However, if the request matches any rule, AWS WAF blocks the request\. AWS WAF evaluates each rule in priority order, starting with the lowest value\.

#### JSON<a name="aws-resource-wafregional-webacl--examples--Create_a_Web_ACL--json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAFRegional::WebACL",
  "Properties": {
    "Name": "WebACL to with three rules",
    "DefaultAction": {
      "Type": "ALLOW"
    },
    "MetricName" : "MyWebACL",
    "Rules": [
      {
        "Action" : {
          "Type" : "BLOCK"
        },
        "Priority" : 1,
        "RuleId" : { "Ref" : "MyRule" }
      },
      {
        "Action" : {
          "Type" : "BLOCK"
        },
        "Priority" : 2,
        "RuleId" : { "Ref" : "BadReferersRule" }
      },
      {
        "Action" : {
          "Type" : "BLOCK"
        },
        "Priority" : 3,
        "RuleId" : { "Ref" : "SqlInjRule" }
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-webacl--examples--Create_a_Web_ACL--yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAFRegional::WebACL"
  Properties: 
    Name: "WebACL to with three rules"
    DefaultAction: 
      Type: "ALLOW"
    MetricName: "MyWebACL"
    Rules: 
      - 
        Action: 
          Type: "BLOCK"
        Priority: 1
        RuleId: 
          Ref: "MyRule"
      - 
        Action: 
          Type: "BLOCK"
        Priority: 2
        RuleId: 
          Ref: "BadReferersRule"
      - 
        Action: 
          Type: "BLOCK"
        Priority: 3
        RuleId: 
          Ref: "SqlInjRule"
```