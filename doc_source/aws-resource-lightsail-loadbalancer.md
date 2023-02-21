# AWS::Lightsail::LoadBalancer<a name="aws-resource-lightsail-loadbalancer"></a>

The `AWS::Lightsail::LoadBalancer` resource specifies a load balancer that can be used with Lightsail instances\.

**Note**  
You cannot attach a TLS certificate to a load balancer using the `AWS::Lightsail::LoadBalancer` resource type\. Instead, use the `AWS::Lightsail::LoadBalancerTlsCertificate` resource type to create a certificate and attach it to a load balancer\.

## Syntax<a name="aws-resource-lightsail-loadbalancer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lightsail-loadbalancer-syntax.json"></a>

```
{
  "Type" : "AWS::Lightsail::LoadBalancer",
  "Properties" : {
      "[AttachedInstances](#cfn-lightsail-loadbalancer-attachedinstances)" : [ String, ... ],
      "[HealthCheckPath](#cfn-lightsail-loadbalancer-healthcheckpath)" : String,
      "[InstancePort](#cfn-lightsail-loadbalancer-instanceport)" : Integer,
      "[IpAddressType](#cfn-lightsail-loadbalancer-ipaddresstype)" : String,
      "[LoadBalancerName](#cfn-lightsail-loadbalancer-loadbalancername)" : String,
      "[SessionStickinessEnabled](#cfn-lightsail-loadbalancer-sessionstickinessenabled)" : Boolean,
      "[SessionStickinessLBCookieDurationSeconds](#cfn-lightsail-loadbalancer-sessionstickinesslbcookiedurationseconds)" : String,
      "[Tags](#cfn-lightsail-loadbalancer-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TlsPolicyName](#cfn-lightsail-loadbalancer-tlspolicyname)" : String
    }
}
```

### YAML<a name="aws-resource-lightsail-loadbalancer-syntax.yaml"></a>

```
Type: AWS::Lightsail::LoadBalancer
Properties: 
  [AttachedInstances](#cfn-lightsail-loadbalancer-attachedinstances): 
    - String
  [HealthCheckPath](#cfn-lightsail-loadbalancer-healthcheckpath): String
  [InstancePort](#cfn-lightsail-loadbalancer-instanceport): Integer
  [IpAddressType](#cfn-lightsail-loadbalancer-ipaddresstype): String
  [LoadBalancerName](#cfn-lightsail-loadbalancer-loadbalancername): String
  [SessionStickinessEnabled](#cfn-lightsail-loadbalancer-sessionstickinessenabled): Boolean
  [SessionStickinessLBCookieDurationSeconds](#cfn-lightsail-loadbalancer-sessionstickinesslbcookiedurationseconds): String
  [Tags](#cfn-lightsail-loadbalancer-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TlsPolicyName](#cfn-lightsail-loadbalancer-tlspolicyname): String
```

## Properties<a name="aws-resource-lightsail-loadbalancer-properties"></a>

`AttachedInstances`  <a name="cfn-lightsail-loadbalancer-attachedinstances"></a>
The Lightsail instances to attach to the load balancer\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckPath`  <a name="cfn-lightsail-loadbalancer-healthcheckpath"></a>
The path on the attached instance where the health check will be performed\. If no path is specified, the load balancer tries to make a request to the default \(root\) page \(`/index.html`\)\.  
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstancePort`  <a name="cfn-lightsail-loadbalancer-instanceport"></a>
The port that the load balancer uses to direct traffic to your Lightsail instances\. For HTTP traffic, specify port `80`\. For HTTPS traffic, specify port `443`\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: Updates are not supported\.

`IpAddressType`  <a name="cfn-lightsail-loadbalancer-ipaddresstype"></a>
The IP address type of the load balancer\.  
The possible values are `ipv4` for IPv4 only, and `dualstack` for both IPv4 and IPv6\.  
*Required*: No  
*Type*: String  
*Allowed values*: `dualstack | ipv4`  
*Update requires*: Updates are not supported\.

`LoadBalancerName`  <a name="cfn-lightsail-loadbalancer-loadbalancername"></a>
The name of the load balancer\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `\w[\w\-]*\w`  
*Update requires*: Updates are not supported\.

`SessionStickinessEnabled`  <a name="cfn-lightsail-loadbalancer-sessionstickinessenabled"></a>
A Boolean value indicating whether session stickiness is enabled\.  
Enable session stickiness \(also known as *session affinity*\) to bind a user's session to a specific instance\. This ensures that all requests from the user during the session are sent to the same instance\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionStickinessLBCookieDurationSeconds`  <a name="cfn-lightsail-loadbalancer-sessionstickinesslbcookiedurationseconds"></a>
The time period, in seconds, after which the load balancer session stickiness cookie should be considered stale\. If you do not specify this parameter, the default value is 0, which indicates that the sticky session should last for the duration of the browser session\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-lightsail-loadbalancer-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS CloudFormation User Guide*\.  
The `Value` of `Tags` is optional for Lightsail resources\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TlsPolicyName`  <a name="cfn-lightsail-loadbalancer-tlspolicyname"></a>
The name of the TLS security policy for the load balancer\.  
*Required*: No  
*Type*: String  
*Pattern*: `\w[\w\-]*\w`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lightsail-loadbalancer-return-values"></a>

### Ref<a name="aws-resource-lightsail-loadbalancer-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-lightsail-loadbalancer-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lightsail-loadbalancer-return-values-fn--getatt-fn--getatt"></a>

`LoadBalancerArn`  <a name="LoadBalancerArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the load balancer\.

## Remarks<a name="aws-resource-lightsail-loadbalancer--remarks"></a>

*Load balancer TLS certificate*

You cannot attach a TLS certificate to a load balancer using the `AWS::Lightsail::LoadBalancer` resource type\. Instead, use the `AWS::Lightsail::LoadBalancerTlsCertificate` resource type to create and attach certificates to a load balancer\.

*Configuring HTTPS redirection*

HTTPS redirection can only be set using the `HttpsRedirectionEnabled` parameter on the `AWS::Lightsail::LoadBalancerTlsCertificate` resource that is attached to the load balancer\.