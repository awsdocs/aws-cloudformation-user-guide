# AWS::ServiceDiscovery::PublicDnsNamespace PublicDnsPropertiesMutable<a name="aws-properties-servicediscovery-publicdnsnamespace-publicdnspropertiesmutable"></a>

DNS properties for the public DNS namespace\.

## Syntax<a name="aws-properties-servicediscovery-publicdnsnamespace-publicdnspropertiesmutable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-publicdnsnamespace-publicdnspropertiesmutable-syntax.json"></a>

```
{
  "[SOA](#cfn-servicediscovery-publicdnsnamespace-publicdnspropertiesmutable-soa)" : SOA
}
```

### YAML<a name="aws-properties-servicediscovery-publicdnsnamespace-publicdnspropertiesmutable-syntax.yaml"></a>

```
  [SOA](#cfn-servicediscovery-publicdnsnamespace-publicdnspropertiesmutable-soa): 
    SOA
```

## Properties<a name="aws-properties-servicediscovery-publicdnsnamespace-publicdnspropertiesmutable-properties"></a>

`SOA`  <a name="cfn-servicediscovery-publicdnsnamespace-publicdnspropertiesmutable-soa"></a>
Start of Authority \(SOA\) record for the hosted zone for the public DNS namespace\.  
*Required*: No  
*Type*: [SOA](aws-properties-servicediscovery-publicdnsnamespace-soa.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)