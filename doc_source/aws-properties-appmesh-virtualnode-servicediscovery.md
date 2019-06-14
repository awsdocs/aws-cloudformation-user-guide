# AWS::AppMesh::VirtualNode ServiceDiscovery<a name="aws-properties-appmesh-virtualnode-servicediscovery"></a>

An object representing the service discovery information for a virtual node\.

## Syntax<a name="aws-properties-appmesh-virtualnode-servicediscovery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-servicediscovery-syntax.json"></a>

```
{
  "[AWSCloudMap](#cfn-appmesh-virtualnode-servicediscovery-awscloudmap)" : [AwsCloudMapServiceDiscovery](aws-properties-appmesh-virtualnode-awscloudmapservicediscovery.md),
  "[DNS](#cfn-appmesh-virtualnode-servicediscovery-dns)" : [DnsServiceDiscovery](aws-properties-appmesh-virtualnode-dnsservicediscovery.md)
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-servicediscovery-syntax.yaml"></a>

```
  [AWSCloudMap](#cfn-appmesh-virtualnode-servicediscovery-awscloudmap): 
    [AwsCloudMapServiceDiscovery](aws-properties-appmesh-virtualnode-awscloudmapservicediscovery.md)
  [DNS](#cfn-appmesh-virtualnode-servicediscovery-dns): 
    [DnsServiceDiscovery](aws-properties-appmesh-virtualnode-dnsservicediscovery.md)
```

## Properties<a name="aws-properties-appmesh-virtualnode-servicediscovery-properties"></a>

`AWSCloudMap`  <a name="cfn-appmesh-virtualnode-servicediscovery-awscloudmap"></a>
Specifies any AWS Cloud Map information for the virtual node\.  
*Required*: No  
*Type*: [AwsCloudMapServiceDiscovery](aws-properties-appmesh-virtualnode-awscloudmapservicediscovery.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DNS`  <a name="cfn-appmesh-virtualnode-servicediscovery-dns"></a>
Specifies the DNS information for the virtual node\.  
*Required*: No  
*Type*: [DnsServiceDiscovery](aws-properties-appmesh-virtualnode-dnsservicediscovery.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)