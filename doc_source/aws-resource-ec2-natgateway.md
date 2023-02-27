# AWS::EC2::NatGateway<a name="aws-resource-ec2-natgateway"></a>

Specifies a network address translation \(NAT\) gateway in the specified subnet\. You can create either a public NAT gateway or a private NAT gateway\. The default is a public NAT gateway\. If you create a public NAT gateway, you must specify an elastic IP address\.

With a NAT gateway, instances in a private subnet can connect to the internet, other AWS services, or an on\-premises network using the IP address of the NAT gateway\.

If you add a default route \(`AWS::EC2::Route` resource\) that points to a NAT gateway, specify the NAT gateway ID for the route's `NatGatewayId` property\.

For more information, see [NAT Gateways](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html) in the *Amazon VPC User Guide*\.

## Syntax<a name="aws-resource-ec2-natgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-natgateway-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NatGateway",
  "Properties" : {
      "[AllocationId](#cfn-ec2-natgateway-allocationid)" : String,
      "[ConnectivityType](#cfn-ec2-natgateway-connectivitytype)" : String,
      "[MaxDrainDurationSeconds](#cfn-ec2-natgateway-maxdraindurationseconds)" : Integer,
      "[PrivateIpAddress](#cfn-ec2-natgateway-privateipaddress)" : String,
      "[SecondaryAllocationIds](#cfn-ec2-natgateway-secondaryallocationids)" : [ String, ... ],
      "[SecondaryPrivateIpAddressCount](#cfn-ec2-natgateway-secondaryprivateipaddresscount)" : Integer,
      "[SecondaryPrivateIpAddresses](#cfn-ec2-natgateway-secondaryprivateipaddresses)" : [ String, ... ],
      "[SubnetId](#cfn-ec2-natgateway-subnetid)" : String,
      "[Tags](#cfn-ec2-natgateway-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-natgateway-syntax.yaml"></a>

```
Type: AWS::EC2::NatGateway
Properties: 
  [AllocationId](#cfn-ec2-natgateway-allocationid): String
  [ConnectivityType](#cfn-ec2-natgateway-connectivitytype): String
  [MaxDrainDurationSeconds](#cfn-ec2-natgateway-maxdraindurationseconds): Integer
  [PrivateIpAddress](#cfn-ec2-natgateway-privateipaddress): String
  [SecondaryAllocationIds](#cfn-ec2-natgateway-secondaryallocationids): 
    - String
  [SecondaryPrivateIpAddressCount](#cfn-ec2-natgateway-secondaryprivateipaddresscount): Integer
  [SecondaryPrivateIpAddresses](#cfn-ec2-natgateway-secondaryprivateipaddresses): 
    - String
  [SubnetId](#cfn-ec2-natgateway-subnetid): String
  [Tags](#cfn-ec2-natgateway-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-natgateway-properties"></a>

`AllocationId`  <a name="cfn-ec2-natgateway-allocationid"></a>
\[Public NAT gateway only\] The allocation ID of the Elastic IP address that's associated with the NAT gateway\. This property is required for a public NAT gateway and cannot be specified with a private NAT gateway\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConnectivityType`  <a name="cfn-ec2-natgateway-connectivitytype"></a>
Indicates whether the NAT gateway supports public or private connectivity\. The default is public connectivity\.  
*Required*: No  
*Type*: String  
*Allowed values*: `private | public`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxDrainDurationSeconds`  <a name="cfn-ec2-natgateway-maxdraindurationseconds"></a>
The maximum amount of time to wait \(in seconds\) before forcibly releasing the IP addresses if connections are still in progress\. Default value is 350 seconds\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `4000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateIpAddress`  <a name="cfn-ec2-natgateway-privateipaddress"></a>
The private IPv4 address to assign to the NAT gateway\. If you don't provide an address, a private IPv4 address will be automatically assigned\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecondaryAllocationIds`  <a name="cfn-ec2-natgateway-secondaryallocationids"></a>
Secondary EIP allocation IDs\. For more information about secondary addresses, see [Create a NAT gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html#nat-gateway-creating) in the *Amazon Virtual Private Cloud User Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryPrivateIpAddressCount`  <a name="cfn-ec2-natgateway-secondaryprivateipaddresscount"></a>
\[Private NAT gateway only\] The number of secondary private IPv4 addresses you want to assign to the NAT gateway\. For more information about secondary addresses, see [Create a NAT gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html#nat-gateway-creating) in the *Amazon Virtual Private Cloud User Guide*\.  
`SecondaryPrivateIpAddressCount` and `SecondaryPrivateIpAddresses` cannot be set at the same time\.
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `7`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryPrivateIpAddresses`  <a name="cfn-ec2-natgateway-secondaryprivateipaddresses"></a>
Secondary private IPv4 addresses\. For more information about secondary addresses, see [Create a NAT gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html#nat-gateway-creating) in the *Amazon Virtual Private Cloud User Guide*\.  
`SecondaryPrivateIpAddressCount` and `SecondaryPrivateIpAddresses` cannot be set at the same time\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-ec2-natgateway-subnetid"></a>
The ID of the subnet in which the NAT gateway is located\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-natgateway-tags"></a>
The tags for the NAT gateway\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-natgateway-return-values"></a>

### Ref<a name="aws-resource-ec2-natgateway-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example, `nat-0a12bc456789de0fg`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-natgateway-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-natgateway-return-values-fn--getatt-fn--getatt"></a>

`NatGatewayId`  <a name="NatGatewayId-fn::getatt"></a>
The ID of the NAT gateway\.

## Examples<a name="aws-resource-ec2-natgateway--examples"></a>



### NAT gateway<a name="aws-resource-ec2-natgateway--examples--NAT_gateway"></a>

The following example creates a public NAT gateway and a route that sends all internet\-bound traffic from the private subnet with EC2 instances to the NAT gateway\. A public NAT gateway uses an elastic IP address to provide it with a public IP address that doesn't change\. Note that the route table for the public subnet with the NAT gateway must also have a route that sends all internet\-bound traffic to an internet gateway, so that the NAT gateway can connect to the internet\.

#### JSON<a name="aws-resource-ec2-natgateway--examples--NAT_gateway--json"></a>

```
"NATGateway" : {
   "Type" : "AWS::EC2::NatGateway",
   "Properties" : {
      "AllocationId" : { 
          "Fn::GetAtt" : ["NATGatewayEIP", "AllocationId"] 
      },
      "SubnetId" : { 
          "Ref" : "PublicSubnet" 
      },
      "Tags" : [ 
          {"Key" : "stack", "Value" : "production" } 
      ]
     }
},
"NATGatewayEIP" : {
   "Type" : "AWS::EC2::EIP",
   "Properties" : {
      "Domain" : "vpc"
   }
},
"RouteNATGateway" : {
   "DependsOn": [ "NATGateway" ],
   "Type" : "AWS::EC2::Route",
   "Properties" : {
      "RouteTableId" : { "Ref" : "PrivateRouteTable" },
      "DestinationCidrBlock" : "0.0.0.0/0",
      "NatGatewayId" : { "Ref" : "NATGateway" }
   }
}
```

#### YAML<a name="aws-resource-ec2-natgateway--examples--NAT_gateway--yaml"></a>

```
NATGateway:
   Type: AWS::EC2::NatGateway
   Properties:
      AllocationId: !GetAtt NATGatewayEIP.AllocationId
      SubnetId: !Ref PublicSubnet
      Tags:
      - Key: stack
        Value: production
NATGatewayEIP:
   Type: AWS::EC2::EIP
   Properties:
      Domain: vpc
RouteNATGateway:
   DependsOn: NATGateway
   Type: AWS::EC2::Route
   Properties:
      RouteTableId: !Ref PrivateRouteTable
      DestinationCidrBlock: '0.0.0.0/0'
      NatGatewayId: !Ref NATGateway
```