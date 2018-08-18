# Amazon Route 53 ServiceDiscovery DnsRecord<a name="aws-properties-servicediscovery-service-dnsrecord"></a>

<a name="aws-properties-servicediscovery-service-dnsrecord-description"></a>The `DnsRecord` property type specifies settings for one DNS record that you want Amazon Route 53 to create when you register an instance\.

<a name="aws-properties-servicediscovery-service-dnsrecord-inheritance"></a>The `DnsRecords` property of the [Amazon Route 53 ServiceDiscovery DnsConfig](aws-properties-servicediscovery-service-dnsconfig.md) property type contains a list of `DnsRecord` property types\.

## Syntax<a name="aws-properties-servicediscovery-service-dnsrecord-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-service-dnsrecord-syntax.json"></a>

```
{
  "[Type](#cfn-servicediscovery-service-dnsrecord-type)" : String,
  "[TTL](#cfn-servicediscovery-service-dnsrecord-ttl)" : String
}
```

### YAML<a name="aws-properties-servicediscovery-service-dnsrecord-syntax.yaml"></a>

```
[Type](#cfn-servicediscovery-service-dnsrecord-type): String
[TTL](#cfn-servicediscovery-service-dnsrecord-ttl): String
```

## Properties<a name="aws-properties-servicediscovery-service-dnsrecord-properties"></a>

`Type`  <a name="cfn-servicediscovery-service-dnsrecord-type"></a>
The DNS type of the record that you want Route 53 to create\. Supported record types include `A`, `AAAA`, and `SRV`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TTL`  <a name="cfn-servicediscovery-service-dnsrecord-ttl"></a>
The amount of time, in seconds, that you want DNS resolvers to cache the settings for this record\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-servicediscovery-service-dnsrecord-seealso"></a>
+ [Using Autonaming for Service Discovery](http://docs.aws.amazon.com/Route53/latest/APIReference/overview-service-discovery.html) in the *Amazon Route 53 API Reference*
+ [CreateService](http://docs.aws.amazon.com/Route53/latest/APIReference/API_autonaming_CreateService.html) in the *Amazon Route 53 API Reference*