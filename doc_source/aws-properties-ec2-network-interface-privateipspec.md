# EC2 Network Interface Private IP Specification<a name="aws-properties-ec2-network-interface-privateipspec"></a>

The `PrivateIpAddressSpecification` type is an embedded property of the [AWS::EC2::NetworkInterface](aws-resource-ec2-network-interface.md) type\.

## Syntax<a name="w3ab2c21c14d761b5"></a>

### JSON<a name="aws-properties-ec2-network-interface-privateipspec-syntax.json"></a>

```
{
  "[PrivateIpAddress](#cfn-ec2-networkinterface-privateipspecification-privateipaddress)" : String,
  "[Primary](#cfn-ec2-networkinterface-privateipspecification-primary)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-network-interface-privateipspec-syntax.yaml"></a>

```
[PrivateIpAddress](#cfn-ec2-networkinterface-privateipspecification-privateipaddress): String
[Primary](#cfn-ec2-networkinterface-privateipspecification-primary): Boolean
```

## Properties<a name="w3ab2c21c14d761b7"></a>

`PrivateIpAddress`  <a name="cfn-ec2-networkinterface-privateipspecification-privateipaddress"></a>
The private IP address of the network interface\.  
*Required*: Yes  
*Type*: String

`Primary`  <a name="cfn-ec2-networkinterface-privateipspecification-primary"></a>
Sets the private IP address as the primary private address\. You can set only one primary private IP address\. If you don't specify a primary private IP address, Amazon EC2 automatically assigns a primary private IP address\.  
*Required*: Yes  
*Type*: Boolean