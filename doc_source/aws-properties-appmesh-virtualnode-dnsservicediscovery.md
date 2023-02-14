# AWS::AppMesh::VirtualNode DnsServiceDiscovery<a name="aws-properties-appmesh-virtualnode-dnsservicediscovery"></a>

An object that represents the DNS service discovery information for your virtual node\.

## Syntax<a name="aws-properties-appmesh-virtualnode-dnsservicediscovery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-dnsservicediscovery-syntax.json"></a>

```
{
  "[Hostname](#cfn-appmesh-virtualnode-dnsservicediscovery-hostname)" : String,
  "[ResponseType](#cfn-appmesh-virtualnode-dnsservicediscovery-responsetype)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-dnsservicediscovery-syntax.yaml"></a>

```
  [Hostname](#cfn-appmesh-virtualnode-dnsservicediscovery-hostname): String
  [ResponseType](#cfn-appmesh-virtualnode-dnsservicediscovery-responsetype): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-dnsservicediscovery-properties"></a>

`Hostname`  <a name="cfn-appmesh-virtualnode-dnsservicediscovery-hostname"></a>
Specifies the DNS service discovery hostname for the virtual node\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseType`  <a name="cfn-appmesh-virtualnode-dnsservicediscovery-responsetype"></a>
Specifies the DNS response type for the virtual node\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ENDPOINTS | LOADBALANCER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)