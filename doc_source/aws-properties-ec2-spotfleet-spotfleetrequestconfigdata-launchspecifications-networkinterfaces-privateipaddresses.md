# Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications NetworkInterfaces PrivateIpAddresses<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses"></a>

`PrivateIpAddresses` is a property of the [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications NetworkInterfaces](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces.md) property that specifies the private IP address that you want to assign to the network interface\.

## Syntax<a name="w3ab2c21c14d638b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-primary)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-privateipaddress)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-primary): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses-privateipaddress): String
```

## Properties<a name="w3ab2c21c14d638b7"></a>

`Primary`  
Indicates whether the private IP address is the primary private IP address\. You can designate only one IP address as primary\.  
*Required: *No  
*Type*: Boolean

`PrivateIpAddress`  
The private IP address\.  
*Required: *Yes  
*Type*: String