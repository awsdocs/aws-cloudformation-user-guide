# AWS::Transfer::Server EndpointDetails<a name="aws-properties-transfer-server-endpointdetails"></a>

The virtual private cloud \(VPC\) endpoint settings that are configured for your SFTP server\. With a VPC endpoint, you can restrict access to your SFTP server to resources only within your VPC\. To control incoming internet traffic, you will need to invoke the `UpdateServer` API and attach an Elastic IP to your server's endpoint\. 

## Syntax<a name="aws-properties-transfer-server-endpointdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-server-endpointdetails-syntax.json"></a>

```
{
  "[AddressAllocationIds](#cfn-transfer-server-endpointdetails-addressallocationids)" : [ String, ... ],
  "[SubnetIds](#cfn-transfer-server-endpointdetails-subnetids)" : [ String, ... ],
  "[VpcEndpointId](#cfn-transfer-server-endpointdetails-vpcendpointid)" : String,
  "[VpcId](#cfn-transfer-server-endpointdetails-vpcid)" : String
}
```

### YAML<a name="aws-properties-transfer-server-endpointdetails-syntax.yaml"></a>

```
  [AddressAllocationIds](#cfn-transfer-server-endpointdetails-addressallocationids): 
    - String
  [SubnetIds](#cfn-transfer-server-endpointdetails-subnetids): 
    - String
  [VpcEndpointId](#cfn-transfer-server-endpointdetails-vpcendpointid): String
  [VpcId](#cfn-transfer-server-endpointdetails-vpcid): String
```

## Properties<a name="aws-properties-transfer-server-endpointdetails-properties"></a>

`AddressAllocationIds`  <a name="cfn-transfer-server-endpointdetails-addressallocationids"></a>
A list of address allocation IDs that are required to attach an Elastic IP address to your SFTP server's endpoint\. This is only valid in the `UpdateServer` API\.  
This property can only be use when `EndpointType` is set to `VPC`\.
*Required*: No  
*Type*: List of String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SubnetIds`  <a name="cfn-transfer-server-endpointdetails-subnetids"></a>
A list of subnet IDs that are required to host your SFTP server endpoint in your VPC\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcEndpointId`  <a name="cfn-transfer-server-endpointdetails-vpcendpointid"></a>
The ID of the VPC endpoint\.  
*Required*: No  
*Type*: String  
*Minimum*: `22`  
*Maximum*: `22`  
*Pattern*: `^vpce-[0-9a-f]{17}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-transfer-server-endpointdetails-vpcid"></a>
The VPC ID of the virtual private cloud in which the SFTP server's endpoint will be hosted\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)