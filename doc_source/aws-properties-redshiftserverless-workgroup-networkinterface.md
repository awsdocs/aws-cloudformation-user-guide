# AWS::RedshiftServerless::Workgroup NetworkInterface<a name="aws-properties-redshiftserverless-workgroup-networkinterface"></a>

Contains information about a network interface in an Amazon Redshift Serverless managed VPC endpoint\. 

## Syntax<a name="aws-properties-redshiftserverless-workgroup-networkinterface-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-redshiftserverless-workgroup-networkinterface-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-redshiftserverless-workgroup-networkinterface-availabilityzone)" : String,
  "[NetworkInterfaceId](#cfn-redshiftserverless-workgroup-networkinterface-networkinterfaceid)" : String,
  "[PrivateIpAddress](#cfn-redshiftserverless-workgroup-networkinterface-privateipaddress)" : String,
  "[SubnetId](#cfn-redshiftserverless-workgroup-networkinterface-subnetid)" : String
}
```

### YAML<a name="aws-properties-redshiftserverless-workgroup-networkinterface-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-redshiftserverless-workgroup-networkinterface-availabilityzone): String
  [NetworkInterfaceId](#cfn-redshiftserverless-workgroup-networkinterface-networkinterfaceid): String
  [PrivateIpAddress](#cfn-redshiftserverless-workgroup-networkinterface-privateipaddress): String
  [SubnetId](#cfn-redshiftserverless-workgroup-networkinterface-subnetid): String
```

## Properties<a name="aws-properties-redshiftserverless-workgroup-networkinterface-properties"></a>

`AvailabilityZone`  <a name="cfn-redshiftserverless-workgroup-networkinterface-availabilityzone"></a>
The availability Zone\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceId`  <a name="cfn-redshiftserverless-workgroup-networkinterface-networkinterfaceid"></a>
The unique identifier of the network interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateIpAddress`  <a name="cfn-redshiftserverless-workgroup-networkinterface-privateipaddress"></a>
The IPv4 address of the network interface within the subnet\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-redshiftserverless-workgroup-networkinterface-subnetid"></a>
The unique identifier of the subnet\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)