# AWS::AppMesh::VirtualNode DnsServiceDiscovery<a name="aws-properties-appmesh-virtualnode-dnsservicediscovery"></a>

An object representing the DNS service discovery information for your virtual node\.

## Syntax<a name="aws-properties-appmesh-virtualnode-dnsservicediscovery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-dnsservicediscovery-syntax.json"></a>

```
{
  "[Hostname](#cfn-appmesh-virtualnode-dnsservicediscovery-hostname)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-dnsservicediscovery-syntax.yaml"></a>

```
  [Hostname](#cfn-appmesh-virtualnode-dnsservicediscovery-hostname): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-dnsservicediscovery-properties"></a>

`Hostname`  <a name="cfn-appmesh-virtualnode-dnsservicediscovery-hostname"></a>
Specifies the DNS service discovery hostname for the virtual node\.   
*Required*: Yes  
*Type*: String  
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
