# AWS::ServiceDiscovery::PrivateDnsNamespace PrivateDnsPropertiesMutable<a name="aws-properties-servicediscovery-privatednsnamespace-privatednspropertiesmutable"></a>

DNS properties for the private DNS namespace\.

## Syntax<a name="aws-properties-servicediscovery-privatednsnamespace-privatednspropertiesmutable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-privatednsnamespace-privatednspropertiesmutable-syntax.json"></a>

```
{
  "[SOA](#cfn-servicediscovery-privatednsnamespace-privatednspropertiesmutable-soa)" : SOA
}
```

### YAML<a name="aws-properties-servicediscovery-privatednsnamespace-privatednspropertiesmutable-syntax.yaml"></a>

```
  [SOA](#cfn-servicediscovery-privatednsnamespace-privatednspropertiesmutable-soa): 
    SOA
```

## Properties<a name="aws-properties-servicediscovery-privatednsnamespace-privatednspropertiesmutable-properties"></a>

`SOA`  <a name="cfn-servicediscovery-privatednsnamespace-privatednspropertiesmutable-soa"></a>
Fields for the Start of Authority \(SOA\) record for the hosted zone for the private DNS namespace\.  
*Required*: No  
*Type*: [SOA](aws-properties-servicediscovery-privatednsnamespace-soa.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)