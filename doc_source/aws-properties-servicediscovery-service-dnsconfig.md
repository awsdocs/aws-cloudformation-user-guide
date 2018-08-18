# Amazon Route 53 ServiceDiscovery DnsConfig<a name="aws-properties-servicediscovery-service-dnsconfig"></a>

<a name="aws-properties-servicediscovery-service-dnsconfig-description"></a>The `DnsConfig` property type specifies settings for the records that you want Amazon Route 53 to create when you register an instance

<a name="aws-properties-servicediscovery-service-dnsconfig-inheritance"></a>`DnsConfig` is a property of the [AWS::ServiceDiscovery::Service](aws-resource-servicediscovery-service.md) resource\.

## Syntax<a name="aws-properties-servicediscovery-service-dnsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-service-dnsconfig-syntax.json"></a>

```
{
  "[DnsRecords](#cfn-servicediscovery-service-dnsconfig-dnsrecords)" : [ [*DnsRecord*](aws-properties-servicediscovery-service-dnsrecord.md), ... ],
  "[NamespaceId](#cfn-servicediscovery-service-dnsconfig-namespaceid)" : String
}
```

### YAML<a name="aws-properties-servicediscovery-service-dnsconfig-syntax.yaml"></a>

```
[DnsRecords](#cfn-servicediscovery-service-dnsconfig-dnsrecords): 
  - [*DnsRecord*](aws-properties-servicediscovery-service-dnsrecord.md)
[NamespaceId](#cfn-servicediscovery-service-dnsconfig-namespaceid): String
```

## Properties<a name="aws-properties-servicediscovery-service-dnsconfig-properties"></a>

`DnsRecords`  <a name="cfn-servicediscovery-service-dnsconfig-dnsrecords"></a>
Contains one `DnsRecord` element for each DNS record that you want Route 53 to create when you register an instance\.  
*Required*: Yes  
*Type*: List of [Amazon Route 53 ServiceDiscovery DnsRecord](aws-properties-servicediscovery-service-dnsrecord.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NamespaceId`  <a name="cfn-servicediscovery-service-dnsconfig-namespaceid"></a>
The ID of the namespace that you want to use for DNS configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## See Also<a name="aws-properties-servicediscovery-service-dnsconfig-seealso"></a>
+ [Using Autonaming for Service Discovery](http://docs.aws.amazon.com/Route53/latest/APIReference/overview-service-discovery.html) in the *Amazon Route 53 API Reference*
+ [CreateService](http://docs.aws.amazon.com/Route53/latest/APIReference/API_autonaming_CreateService.html) in the *Amazon Route 53 API Reference*