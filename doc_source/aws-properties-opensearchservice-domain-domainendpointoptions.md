# AWS::OpenSearchService::Domain DomainEndpointOptions<a name="aws-properties-opensearchservice-domain-domainendpointoptions"></a>

Specifies additional options for the domain endpoint, such as whether to require HTTPS for all traffic or whether to use a custom endpoint rather than the default endpoint\.

## Syntax<a name="aws-properties-opensearchservice-domain-domainendpointoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-domainendpointoptions-syntax.json"></a>

```
{
  "[CustomEndpoint](#cfn-opensearchservice-domain-domainendpointoptions-customendpoint)" : String,
  "[CustomEndpointCertificateArn](#cfn-opensearchservice-domain-domainendpointoptions-customendpointcertificatearn)" : String,
  "[CustomEndpointEnabled](#cfn-opensearchservice-domain-domainendpointoptions-customendpointenabled)" : Boolean,
  "[EnforceHTTPS](#cfn-opensearchservice-domain-domainendpointoptions-enforcehttps)" : Boolean,
  "[TLSSecurityPolicy](#cfn-opensearchservice-domain-domainendpointoptions-tlssecuritypolicy)" : String
}
```

### YAML<a name="aws-properties-opensearchservice-domain-domainendpointoptions-syntax.yaml"></a>

```
  [CustomEndpoint](#cfn-opensearchservice-domain-domainendpointoptions-customendpoint): String
  [CustomEndpointCertificateArn](#cfn-opensearchservice-domain-domainendpointoptions-customendpointcertificatearn): String
  [CustomEndpointEnabled](#cfn-opensearchservice-domain-domainendpointoptions-customendpointenabled): Boolean
  [EnforceHTTPS](#cfn-opensearchservice-domain-domainendpointoptions-enforcehttps): Boolean
  [TLSSecurityPolicy](#cfn-opensearchservice-domain-domainendpointoptions-tlssecuritypolicy): String
```

## Properties<a name="aws-properties-opensearchservice-domain-domainendpointoptions-properties"></a>

`CustomEndpoint`  <a name="cfn-opensearchservice-domain-domainendpointoptions-customendpoint"></a>
The fully qualified URL for your custom endpoint\. Required if you enabled a custom endpoint for the domain\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^(((?!-)[A-Za-z0-9-]{0,62}[A-Za-z0-9])\.)+((?!-)[A-Za-z0-9-]{1,62}[A-Za-z0-9])$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomEndpointCertificateArn`  <a name="cfn-opensearchservice-domain-domainendpointoptions-customendpointcertificatearn"></a>
The AWS Certificate Manager ARN for your domain's SSL/TLS certificate\. Required if you enabled a custom endpoint for the domain\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomEndpointEnabled`  <a name="cfn-opensearchservice-domain-domainendpointoptions-customendpointenabled"></a>
True to enable a custom endpoint for the domain\. If enabled, you must also provide values for `CustomEndpoint` and `CustomEndpointCertificateArn`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnforceHTTPS`  <a name="cfn-opensearchservice-domain-domainendpointoptions-enforcehttps"></a>
True to require that all traffic to the domain arrive over HTTPS\. Required if you enable fine\-grained access control in [AdvancedSecurityOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-opensearchservice-domain-advancedsecurityoptionsinput.html)\.  
*Required*: Conditional  
*Type*: Boolean  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`TLSSecurityPolicy`  <a name="cfn-opensearchservice-domain-domainendpointoptions-tlssecuritypolicy"></a>
The minimum TLS version required for traffic to the domain\. Valid values are TLS 1\.0 \(default\) or 1\.2:  
+ `Policy-Min-TLS-1-0-2019-07`
+ `Policy-Min-TLS-1-2-2019-07`
*Required*: No  
*Type*: String  
*Allowed values*: `Policy-Min-TLS-1-0-2019-07 | Policy-Min-TLS-1-2-2019-07`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)