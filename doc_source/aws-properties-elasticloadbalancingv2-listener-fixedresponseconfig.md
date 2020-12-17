# AWS::ElasticLoadBalancingV2::Listener FixedResponseConfig<a name="aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig"></a>

Specifies information required when returning a custom HTTP response\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig-syntax.json"></a>

```
{
  "[ContentType](#cfn-elasticloadbalancingv2-listener-fixedresponseconfig-contenttype)" : String,
  "[MessageBody](#cfn-elasticloadbalancingv2-listener-fixedresponseconfig-messagebody)" : String,
  "[StatusCode](#cfn-elasticloadbalancingv2-listener-fixedresponseconfig-statuscode)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig-syntax.yaml"></a>

```
  [ContentType](#cfn-elasticloadbalancingv2-listener-fixedresponseconfig-contenttype): String
  [MessageBody](#cfn-elasticloadbalancingv2-listener-fixedresponseconfig-messagebody): String
  [StatusCode](#cfn-elasticloadbalancingv2-listener-fixedresponseconfig-statuscode): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig-properties"></a>

`ContentType`  <a name="cfn-elasticloadbalancingv2-listener-fixedresponseconfig-contenttype"></a>
The content type\.  
Valid Values: text/plain \| text/css \| text/html \| application/javascript \| application/json  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageBody`  <a name="cfn-elasticloadbalancingv2-listener-fixedresponseconfig-messagebody"></a>
The message\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatusCode`  <a name="cfn-elasticloadbalancingv2-listener-fixedresponseconfig-statuscode"></a>
The HTTP response code \(2XX, 4XX, or 5XX\)\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^(2|4|5)\d\d$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)