# AWS::ServiceDiscovery::Service DnsConfig<a name="aws-properties-servicediscovery-service-dnsconfig"></a>

A complex type that contains information about the Amazon Route 53 DNS records that you want AWS Cloud Map to create when you register an instance\.

## Syntax<a name="aws-properties-servicediscovery-service-dnsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-service-dnsconfig-syntax.json"></a>

```
{
  "[DnsRecords](#cfn-servicediscovery-service-dnsconfig-dnsrecords)" : [ DnsRecord, ... ],
  "[NamespaceId](#cfn-servicediscovery-service-dnsconfig-namespaceid)" : String,
  "[RoutingPolicy](#cfn-servicediscovery-service-dnsconfig-routingpolicy)" : String
}
```

### YAML<a name="aws-properties-servicediscovery-service-dnsconfig-syntax.yaml"></a>

```
  [DnsRecords](#cfn-servicediscovery-service-dnsconfig-dnsrecords): 
    - DnsRecord
  [NamespaceId](#cfn-servicediscovery-service-dnsconfig-namespaceid): String
  [RoutingPolicy](#cfn-servicediscovery-service-dnsconfig-routingpolicy): String
```

## Properties<a name="aws-properties-servicediscovery-service-dnsconfig-properties"></a>

`DnsRecords`  <a name="cfn-servicediscovery-service-dnsconfig-dnsrecords"></a>
An array that contains one `DnsRecord` object for each Route 53 DNS record that you want AWS Cloud Map to create when you register an instance\.  
*Required*: Yes  
*Type*: List of [DnsRecord](aws-properties-servicediscovery-service-dnsrecord.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NamespaceId`  <a name="cfn-servicediscovery-service-dnsconfig-namespaceid"></a>
The ID of the namespace to use for DNS configuration\.  
You must specify a value for `NamespaceId` either for `DnsConfig` or for the [service properties](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)\. Don't specify a value in both places\. 
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoutingPolicy`  <a name="cfn-servicediscovery-service-dnsconfig-routingpolicy"></a>
The routing policy that you want to apply to all Route 53 DNS records that AWS Cloud Map creates when you register an instance and specify this service\.  
If you want to use this service to register instances that create alias records, specify `WEIGHTED` for the routing policy\.
You can specify the following values:    
MULTIVALUE  
If you define a health check for the service and the health check is healthy, Route 53 returns the applicable value for up to eight instances\.  
For example, suppose the service includes configurations for one `A` record and a health check, and you use the service to register 10 instances\. Route 53 responds to DNS queries with IP addresses for up to eight healthy instances\. If fewer than eight instances are healthy, Route 53 responds to every DNS query with the IP addresses for all of the healthy instances\.  
If you don't define a health check for the service, Route 53 assumes that all instances are healthy and returns the values for up to eight instances\.  
For more information about the multivalue routing policy, see [Multivalue Answer Routing](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-multivalue) in the *Route 53 Developer Guide*\.  
WEIGHTED  
Route 53 returns the applicable value from one randomly selected instance from among the instances that you registered using the same service\. Currently, all records have the same weight, so you can't route more or less traffic to any instances\.  
For example, suppose the service includes configurations for one `A` record and a health check, and you use the service to register 10 instances\. Route 53 responds to DNS queries with the IP address for one randomly selected instance from among the healthy instances\. If no instances are healthy, Route 53 responds to DNS queries as if all of the instances were healthy\.  
If you don't define a health check for the service, Route 53 assumes that all instances are healthy and returns the applicable value for one randomly selected instance\.  
For more information about the weighted routing policy, see [Weighted Routing](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-weighted) in the *Route 53 Developer Guide*\.
*Required*: No  
*Type*: String  
*Allowed values*: `MULTIVALUE | WEIGHTED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-servicediscovery-service-dnsconfig--seealso"></a>
+  [Return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html#aws-resource-servicediscovery-service-return-values) in the topic [AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html) 
+  [DnsConfig](https://docs.aws.amazon.com/cloud-map/latest/api/API_DnsConfig.html) in the *AWS Cloud Map API Reference* 

