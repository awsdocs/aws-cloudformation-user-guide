# Amazon Elastic Compute Cloud SpotFleet NetworkInterfaces PrivateIpAddresses<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses"></a>

`PrivateIpAddresses` is a property of the [Amazon Elastic Compute Cloud SpotFleet NetworkInterfaces](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces.md) property that specifies the private IP address that you want to assign to the network interface\.

## Syntax<a name="w3ab2c21c14d810b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-syntax.json"></a>

```
{
  "[Primary](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-primary)" : Boolean,
  "[PrivateIpAddress](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-privateipaddress)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-syntax.yaml"></a>

```
[Primary](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-primary): Boolean
[PrivateIpAddress](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-privateipaddress): String
```

## Properties<a name="w3ab2c21c14d810b7"></a>

`Primary`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-primary"></a>
Indicates whether the private IP address is the primary private IP address\. You can designate only one IP address as primary\.  
*Required*: No  
*Type*: Boolean

`PrivateIpAddress`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-privateipaddress"></a>
The private IP address\.  
*Required*: Yes  
*Type*: String