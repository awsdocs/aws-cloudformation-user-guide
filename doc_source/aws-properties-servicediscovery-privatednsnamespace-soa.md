# AWS::ServiceDiscovery::PrivateDnsNamespace SOA<a name="aws-properties-servicediscovery-privatednsnamespace-soa"></a>

Start of Authority \(SOA\) properties for a public or private DNS namespace\.

## Syntax<a name="aws-properties-servicediscovery-privatednsnamespace-soa-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-privatednsnamespace-soa-syntax.json"></a>

```
{
  "[TTL](#cfn-servicediscovery-privatednsnamespace-soa-ttl)" : Double
}
```

### YAML<a name="aws-properties-servicediscovery-privatednsnamespace-soa-syntax.yaml"></a>

```
  [TTL](#cfn-servicediscovery-privatednsnamespace-soa-ttl): Double
```

## Properties<a name="aws-properties-servicediscovery-privatednsnamespace-soa-properties"></a>

`TTL`  <a name="cfn-servicediscovery-privatednsnamespace-soa-ttl"></a>
The time to live \(TTL\) for purposes of negative caching\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)