# Elastic Load Balancing V2 FixedResponseConfig<a name="aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig"></a>

<a name="aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig-description"></a>The `FixedResponseConfig` property type specifies information about an action that returns a custom HTTP response\.

<a name="aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig-inheritance"></a> `FixedResponseConfig` is a property of the [Elastic Load Balancing V2 Actions](aws-properties-elasticloadbalancingv2-listenerrule-actions.md) property type\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig-syntax.json"></a>

```
{
  "[ContentType](#cfn-elasticloadbalancingv2-listenerrule-fixedresponseconfig-contenttype)" : String ,
  "[MessageBody](#cfn-elasticloadbalancingv2-listenerrule-fixedresponseconfig-messagebody)" : String,
  "[StatusCode](#cfn-elasticloadbalancingv2-listenerrule-fixedresponseconfig-statuscode)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig-syntax.yaml"></a>

```
[ContentType](#cfn-elasticloadbalancingv2-listenerrule-fixedresponseconfig-contenttype): String
[MessageBody](#cfn-elasticloadbalancingv2-listenerrule-fixedresponseconfig-messagebody): String
[StatusCode](#cfn-elasticloadbalancingv2-listenerrule-fixedresponseconfig-statuscode): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig-properties"></a>

`ContentType`  <a name="cfn-elasticloadbalancingv2-listenerrule-fixedresponseconfig-contenttype"></a>
The content type\.  
Valid Values: `text/plain` \| `text/css` \| `text/html` \| `application/javascript` \| `application/json`  
Length Constraints: Minimum length of 0\. Maximum length of 32\.  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MessageBody`  <a name="cfn-elasticloadbalancingv2-listenerrule-fixedresponseconfig-messagebody"></a>
The message\.  
Length Constraints: Minimum length of 0\. Maximum length of 1024\.  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StatusCode`  <a name="cfn-elasticloadbalancingv2-listenerrule-fixedresponseconfig-statuscode"></a>
The HTTP response code \(2XX, 4XX, or 5XX\)\.  
Pattern: `^(2|4|5)\d\d$`  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig-seealso"></a>
+ [FixedResponseActionConfig](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_FixedResponseActionConfig.html) in the *Elastic Load Balancing API Reference version 2015\-12\-01*