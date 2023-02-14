# AWS::ServiceDiscovery::PrivateDnsNamespace Properties<a name="aws-properties-servicediscovery-privatednsnamespace-properties"></a>

Properties for the private DNS namespace\.

## Syntax<a name="aws-properties-servicediscovery-privatednsnamespace-properties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-privatednsnamespace-properties-syntax.json"></a>

```
{
  "[DnsProperties](#cfn-servicediscovery-privatednsnamespace-properties-dnsproperties)" : PrivateDnsPropertiesMutable
}
```

### YAML<a name="aws-properties-servicediscovery-privatednsnamespace-properties-syntax.yaml"></a>

```
  [DnsProperties](#cfn-servicediscovery-privatednsnamespace-properties-dnsproperties): 
    PrivateDnsPropertiesMutable
```

## Properties<a name="aws-properties-servicediscovery-privatednsnamespace-properties-properties"></a>

`DnsProperties`  <a name="cfn-servicediscovery-privatednsnamespace-properties-dnsproperties"></a>
DNS properties for the private DNS namespace\.  
*Required*: No  
*Type*: [PrivateDnsPropertiesMutable](aws-properties-servicediscovery-privatednsnamespace-privatednspropertiesmutable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)