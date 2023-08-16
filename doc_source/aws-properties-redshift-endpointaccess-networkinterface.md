# AWS::Redshift::EndpointAccess NetworkInterface<a name="aws-properties-redshift-endpointaccess-networkinterface"></a>

Describes a network interface\. 

## Syntax<a name="aws-properties-redshift-endpointaccess-networkinterface-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-redshift-endpointaccess-networkinterface-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-redshift-endpointaccess-networkinterface-availabilityzone)" : String,
  "[NetworkInterfaceId](#cfn-redshift-endpointaccess-networkinterface-networkinterfaceid)" : String,
  "[PrivateIpAddress](#cfn-redshift-endpointaccess-networkinterface-privateipaddress)" : String,
  "[SubnetId](#cfn-redshift-endpointaccess-networkinterface-subnetid)" : String
}
```

### YAML<a name="aws-properties-redshift-endpointaccess-networkinterface-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-redshift-endpointaccess-networkinterface-availabilityzone): String
  [NetworkInterfaceId](#cfn-redshift-endpointaccess-networkinterface-networkinterfaceid): String
  [PrivateIpAddress](#cfn-redshift-endpointaccess-networkinterface-privateipaddress): String
  [SubnetId](#cfn-redshift-endpointaccess-networkinterface-subnetid): String
```

## Properties<a name="aws-properties-redshift-endpointaccess-networkinterface-properties"></a>

`AvailabilityZone`  <a name="cfn-redshift-endpointaccess-networkinterface-availabilityzone"></a>
The Availability Zone\.   
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceId`  <a name="cfn-redshift-endpointaccess-networkinterface-networkinterfaceid"></a>
The network interface identifier\.   
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateIpAddress`  <a name="cfn-redshift-endpointaccess-networkinterface-privateipaddress"></a>
The IPv4 address of the network interface within the subnet\.   
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-redshift-endpointaccess-networkinterface-subnetid"></a>
The subnet identifier\.   
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)