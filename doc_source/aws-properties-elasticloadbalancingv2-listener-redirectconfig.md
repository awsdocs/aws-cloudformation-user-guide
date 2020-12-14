# AWS::ElasticLoadBalancingV2::Listener RedirectConfig<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig"></a>

Information about a redirect action\.

A URI consists of the following components: protocol://hostname:port/path?query\. You must modify at least one of the following components to avoid a redirect loop: protocol, hostname, port, or path\. Any components that you do not modify retain their original values\.

You can reuse URI components using the following reserved keywords:
+ \#\{protocol\}
+ \#\{host\}
+ \#\{port\}
+ \#\{path\} \(the leading "/" is removed\)
+ \#\{query\}

For example, you can change the path to "/new/\#\{path\}", the hostname to "example\.\#\{host\}", or the query to "\#\{query\}&value=xyz"\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-syntax.json"></a>

```
{
  "[Host](#cfn-elasticloadbalancingv2-listener-redirectconfig-host)" : String,
  "[Path](#cfn-elasticloadbalancingv2-listener-redirectconfig-path)" : String,
  "[Port](#cfn-elasticloadbalancingv2-listener-redirectconfig-port)" : String,
  "[Protocol](#cfn-elasticloadbalancingv2-listener-redirectconfig-protocol)" : String,
  "[Query](#cfn-elasticloadbalancingv2-listener-redirectconfig-query)" : String,
  "[StatusCode](#cfn-elasticloadbalancingv2-listener-redirectconfig-statuscode)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-syntax.yaml"></a>

```
  [Host](#cfn-elasticloadbalancingv2-listener-redirectconfig-host): String
  [Path](#cfn-elasticloadbalancingv2-listener-redirectconfig-path): String
  [Port](#cfn-elasticloadbalancingv2-listener-redirectconfig-port): String
  [Protocol](#cfn-elasticloadbalancingv2-listener-redirectconfig-protocol): String
  [Query](#cfn-elasticloadbalancingv2-listener-redirectconfig-query): String
  [StatusCode](#cfn-elasticloadbalancingv2-listener-redirectconfig-statuscode): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-properties"></a>

`Host`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-host"></a>
The hostname\. This component is not percent\-encoded\. The hostname can contain \#\{host\}\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-path"></a>
The absolute path, starting with the leading "/"\. This component is not percent\-encoded\. The path can contain \#\{host\}, \#\{path\}, and \#\{port\}\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-port"></a>
The port\. You can specify a value from 1 to 65535 or \#\{port\}\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-protocol"></a>
The protocol\. You can specify HTTP, HTTPS, or \#\{protocol\}\. You can redirect HTTP to HTTP, HTTP to HTTPS, and HTTPS to HTTPS\. You cannot redirect HTTPS to HTTP\.  
*Required*: No  
*Type*: String  
*Pattern*: `^(HTTPS?|#\{protocol\})$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Query`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-query"></a>
The query parameters, URL\-encoded when necessary, but not percent\-encoded\. Do not include the leading "?", as it is automatically added\. You can specify any of the reserved keywords\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatusCode`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-statuscode"></a>
The HTTP redirect code\. The redirect is either permanent \(HTTP 301\) or temporary \(HTTP 302\)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `HTTP_301 | HTTP_302`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)