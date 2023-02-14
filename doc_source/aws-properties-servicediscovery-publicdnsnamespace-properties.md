# AWS::ServiceDiscovery::PublicDnsNamespace Properties<a name="aws-properties-servicediscovery-publicdnsnamespace-properties"></a>

Properties for the public DNS namespace\.

## Syntax<a name="aws-properties-servicediscovery-publicdnsnamespace-properties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-publicdnsnamespace-properties-syntax.json"></a>

```
{
  "[DnsProperties](#cfn-servicediscovery-publicdnsnamespace-properties-dnsproperties)" : PublicDnsPropertiesMutable
}
```

### YAML<a name="aws-properties-servicediscovery-publicdnsnamespace-properties-syntax.yaml"></a>

```
  [DnsProperties](#cfn-servicediscovery-publicdnsnamespace-properties-dnsproperties): 
    PublicDnsPropertiesMutable
```

## Properties<a name="aws-properties-servicediscovery-publicdnsnamespace-properties-properties"></a>

`DnsProperties`  <a name="cfn-servicediscovery-publicdnsnamespace-properties-dnsproperties"></a>
DNS properties for the public DNS namespace\.  
*Required*: No  
*Type*: [PublicDnsPropertiesMutable](aws-properties-servicediscovery-publicdnsnamespace-publicdnspropertiesmutable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)