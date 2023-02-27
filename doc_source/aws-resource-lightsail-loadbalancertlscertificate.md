# AWS::Lightsail::LoadBalancerTlsCertificate<a name="aws-resource-lightsail-loadbalancertlscertificate"></a>

The `AWS::Lightsail::LoadBalancerTlsCertificate` resource specifies a TLS certificate that can be used with a Lightsail load balancer\.

## Syntax<a name="aws-resource-lightsail-loadbalancertlscertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lightsail-loadbalancertlscertificate-syntax.json"></a>

```
{
  "Type" : "AWS::Lightsail::LoadBalancerTlsCertificate",
  "Properties" : {
      "[CertificateAlternativeNames](#cfn-lightsail-loadbalancertlscertificate-certificatealternativenames)" : [ String, ... ],
      "[CertificateDomainName](#cfn-lightsail-loadbalancertlscertificate-certificatedomainname)" : String,
      "[CertificateName](#cfn-lightsail-loadbalancertlscertificate-certificatename)" : String,
      "[HttpsRedirectionEnabled](#cfn-lightsail-loadbalancertlscertificate-httpsredirectionenabled)" : Boolean,
      "[IsAttached](#cfn-lightsail-loadbalancertlscertificate-isattached)" : Boolean,
      "[LoadBalancerName](#cfn-lightsail-loadbalancertlscertificate-loadbalancername)" : String
    }
}
```

### YAML<a name="aws-resource-lightsail-loadbalancertlscertificate-syntax.yaml"></a>

```
Type: AWS::Lightsail::LoadBalancerTlsCertificate
Properties: 
  [CertificateAlternativeNames](#cfn-lightsail-loadbalancertlscertificate-certificatealternativenames): 
    - String
  [CertificateDomainName](#cfn-lightsail-loadbalancertlscertificate-certificatedomainname): String
  [CertificateName](#cfn-lightsail-loadbalancertlscertificate-certificatename): String
  [HttpsRedirectionEnabled](#cfn-lightsail-loadbalancertlscertificate-httpsredirectionenabled): Boolean
  [IsAttached](#cfn-lightsail-loadbalancertlscertificate-isattached): Boolean
  [LoadBalancerName](#cfn-lightsail-loadbalancertlscertificate-loadbalancername): String
```

## Properties<a name="aws-resource-lightsail-loadbalancertlscertificate-properties"></a>

`CertificateAlternativeNames`  <a name="cfn-lightsail-loadbalancertlscertificate-certificatealternativenames"></a>
An array of alternative domain names and subdomain names for your SSL/TLS certificate\.  
In addition to the primary domain name, you can have up to nine alternative domain names\. Wildcards \(such as `*.example.com`\) are not supported\.  
*Required*: No  
*Type*: List of String  
*Update requires*: Updates are not supported\.

`CertificateDomainName`  <a name="cfn-lightsail-loadbalancertlscertificate-certificatedomainname"></a>
The domain name for the SSL/TLS certificate\. For example, `example.com` or `www.example.com`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`CertificateName`  <a name="cfn-lightsail-loadbalancertlscertificate-certificatename"></a>
The name of the SSL/TLS certificate\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HttpsRedirectionEnabled`  <a name="cfn-lightsail-loadbalancertlscertificate-httpsredirectionenabled"></a>
A Boolean value indicating whether HTTPS redirection is enabled for the load balancer that the TLS certificate is attached to\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsAttached`  <a name="cfn-lightsail-loadbalancertlscertificate-isattached"></a>
A Boolean value indicating whether the SSL/TLS certificate is attached to a Lightsail load balancer\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerName`  <a name="cfn-lightsail-loadbalancertlscertificate-loadbalancername"></a>
The name of the load balancer that the SSL/TLS certificate is attached to\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `\w[\w\-]*\w`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-lightsail-loadbalancertlscertificate-return-values"></a>

### Ref<a name="aws-resource-lightsail-loadbalancertlscertificate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-lightsail-loadbalancertlscertificate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lightsail-loadbalancertlscertificate-return-values-fn--getatt-fn--getatt"></a>

`LoadBalancerTlsCertificateArn`  <a name="LoadBalancerTlsCertificateArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the SSL/TLS certificate\.

`Status`  <a name="Status-fn::getatt"></a>
The validation status of the SSL/TLS certificate\.  
Valid Values: `PENDING_VALIDATION` \| `ISSUED` \| `INACTIVE` \| `EXPIRED` \| `VALIDATION_TIMED_OUT` \| `REVOKED` \| `FAILED` \| `UNKNOWN`

## Remarks<a name="aws-resource-lightsail-loadbalancertlscertificate--remarks"></a>

*Attaching certificates to load balancers*

Use the `IsAttached` parameter to attach a certificate to a load balancer\. The certificate must be in a valid state before it can be attached\.

*Replacing certificates attached to load balancers*

After a certificate is attached to a load balancer, it cannot be detached\. It can only be replaced\. If the `isAttached` parameter is changed from `true` to `false` for a certificate, it won’t be detached from the load balancer and the stack will drift\. You can replace a certificate by changing the `isAttached` parameter of a different certificate to `true` and changing the current certificate’s `isAttached` parameter to `false`\.

*Maximum attached certificates*

Don't attach more than one certificate to a load balancer\. If you attach multiple certificates to a load balancer, the behavior is unpredictable, and any one of the certificates might be in effect\. This will cause the stack to drift because only one of the certificates is attached to the load balancer, but the template shows multiple\.

*Configuring HTTPS redirection*

The `HttpsRedirectionEnabled` parameter can only be set on a certificate that is in a valid state and is also attached to a load balancer\.