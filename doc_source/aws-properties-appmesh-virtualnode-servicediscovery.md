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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
