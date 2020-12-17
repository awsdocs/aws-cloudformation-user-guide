# AWS::Transfer::Server EndpointDetails<a name="aws-properties-transfer-server-endpointdetails"></a>

The virtual private cloud \(VPC\) endpoint settings that are configured for your server\. When you host your endpoint within your VPC, you can make it accessible only to resources within your VPC, or you can attach Elastic IPs and make it accessible to clients over the internet\. You VPC's default security groups are automatically assigned to your endpoint\.

**Note**  
It is recommended that you use `VPC` as the `EndpointType`\. With this endpoint type, you have the option to directly associate up to three Elastic IPv4 addresses \(BYO IP included\) with your server's endpoint and use VPC security groups to restrict traffic by the client's public IP address\. This is not possible with `EndpointType` set to `VPC_ENDPOINT`\.

## Syntax<a name="aws-properties-transfer-server-endpointdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-server-endpointdetails-syntax.json"></a>

```
{
  "[AddressAllocationIds](#cfn-transfer-server-endpointdetails-addressallocationids)" : [ String, ... ],
  "[SecurityGroupIds](#cfn-transfer-server-endpointdetails-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-transfer-server-endpointdetails-subnetids)" : [ String, ... ],
  "[VpcEndpointId](#cfn-transfer-server-endpointdetails-vpcendpointid)" : String,
  "[VpcId](#cfn-transfer-server-endpointdetails-vpcid)" : String
}
```

### YAML<a name="aws-properties-transfer-server-endpointdetails-syntax.yaml"></a>

```
  [AddressAllocationIds](#cfn-transfer-server-endpointdetails-addressallocationids): 
    - String
  [SecurityGroupIds](#cfn-transfer-server-endpointdetails-securitygroupids): 
    - String
  [SubnetIds](#cfn-transfer-server-endpointdetails-subnetids): 
    - String
  [VpcEndpointId](#cfn-transfer-server-endpointdetails-vpcendpointid): String
  [VpcId](#cfn-transfer-server-endpointdetails-vpcid): String
```

## Properties<a name="aws-properties-transfer-server-endpointdetails-properties"></a>

`AddressAllocationIds`  <a name="cfn-transfer-server-endpointdetails-addressallocationids"></a>
A list of address allocation IDs that are required to attach an Elastic IP address to your server's endpoint\. This is only valid in the `UpdateServer` API\.  
This property can only be set when `EndpointType` is set to `VPC`\.
*Required*: No  
*Type*: List of String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SecurityGroupIds`  <a name="cfn-transfer-server-endpointdetails-securitygroupids"></a>
A list of security groups IDs that are available to attach to your server's endpoint\.  
This property can only be set when `EndpointType` is set to `VPC`\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-transfer-server-endpointdetails-subnetids"></a>
A list of subnet IDs that are required to host your server endpoint in your VPC\.  
This property can only be set when `EndpointType` is set to `VPC`\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcEndpointId`  <a name="cfn-transfer-server-endpointdetails-vpcendpointid"></a>
The ID of the VPC endpoint\.  
This property can only be set when `EndpointType` is set to `VPC_ENDPOINT`\.
*Required*: No  
*Type*: String  
*Minimum*: `22`  
*Maximum*: `22`  
*Pattern*: `^vpce-[0-9a-f]{17}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-transfer-server-endpointdetails-vpcid"></a>
The VPC ID of the virtual private cloud in which the server's endpoint will be hosted\.  
This property can only be set when `EndpointType` is set to `VPC`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-transfer-server-endpointdetails--seealso"></a>

[EndpointDetails](https://docs.aws.amazon.com/transfer/latest/userguide/API_EndpointDetails.html) in the *AWS Transfer Family User Guide*\.