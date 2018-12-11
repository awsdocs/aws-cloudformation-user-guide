# AWS Cloud Map ServiceDiscovery DnsConfig<a name="aws-properties-servicediscovery-service-dnsconfig"></a>

<a name="aws-properties-servicediscovery-service-dnsconfig-description"></a>The optional `DnsConfig` property type specifies settings for the DNS records that you want AWS Cloud Map to create when you register an instance\.

<a name="aws-properties-servicediscovery-service-dnsconfig-inheritance"></a>`DnsConfig` is a property of the [AWS::ServiceDiscovery::Service](aws-resource-servicediscovery-service.md) resource\.

## Syntax<a name="aws-properties-servicediscovery-service-dnsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-service-dnsconfig-syntax.json"></a>

```
{
  "[DnsRecords](#cfn-servicediscovery-service-dnsconfig-dnsrecords)" : [ [*DnsRecord*](aws-properties-servicediscovery-service-dnsrecord.md), ... ],
  "[NamespaceId](#cfn-servicediscovery-service-dnsconfig-namespaceid)" : String,
  "[RoutingPolicy](#cfn-servicediscovery-service-dnsconfig-routingpolicy)" : String
}
```

### YAML<a name="aws-properties-servicediscovery-service-dnsconfig-syntax.yaml"></a>

```
[DnsRecords](#cfn-servicediscovery-service-dnsconfig-dnsrecords): 
  - [*DnsRecord*](aws-properties-servicediscovery-service-dnsrecord.md)
[NamespaceId](#cfn-servicediscovery-service-dnsconfig-namespaceid): String
[RoutingPolicy](#cfn-servicediscovery-service-dnsconfig-routingpolicy): String
```

## Properties<a name="aws-properties-servicediscovery-service-dnsconfig-properties"></a>

`DnsRecords`  <a name="cfn-servicediscovery-service-dnsconfig-dnsrecords"></a>
Contains one `DnsRecord` element for each DNS record that you want AWS Cloud Map to create when you register an instance\.  
*Required*: Yes  
*Type*: List of [DnsRecord](aws-properties-servicediscovery-service-dnsrecord.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NamespaceId`  <a name="cfn-servicediscovery-service-dnsconfig-namespaceid"></a>
The ID of the namespace that you want to use for DNS configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RoutingPolicy`  <a name="cfn-servicediscovery-service-dnsconfig-routingpolicy"></a>
The routing policy that you want to apply to all DNS records that AWS Cloud Map creates when you register an instance and specify this service\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-servicediscovery-service-dnsconfig-seealso"></a>
+ [CreateService](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreateService.html) in the *AWS Cloud Map API Reference*