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
  [SubnetId](#cfn-ec2-natgateway-subnetid): String
  [Tags](#cfn-ec2-natgateway-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-natgateway-properties"></a>

`AllocationId`  <a name="cfn-ec2-natgateway-allocationid"></a>
\[Public NAT gateway only\] The allocation ID of the Elastic IP address that's associated with the NAT gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConnectivityType`  <a name="cfn-ec2-natgateway-connectivitytype"></a>
Indicates whether the NAT gateway supports public or private connectivity\.  
*Required*: No  
*Type*: String  
*Allowed values*: `private | public`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

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

## Examples<a name="aws-resource-ec2-natgateway--examples"></a>



### NAT gateway<a name="aws-resource-ec2-natgateway--examples--NAT_gateway"></a>

The following example creates a NAT gateway and a route that associates the NAT gateway with a route table\. The route table must be associated with an Internet gateway so that the NAT gateway can connect to the Internet\.

#### JSON<a name="aws-resource-ec2-natgateway--examples--NAT_gateway--json"></a>

```
"NAT" : {
   "Type" : "AWS::EC2::NatGateway",
   "Properties" : {
      "AllocationId" : { "Fn::GetAtt" : ["EIP", "AllocationId"]},
      "SubnetId" : { "Ref" : "Subnet"},
      "Tags" : [ {"Key" : "stack", "Value" : "production" } ]
     }
},
"EIP" : {
   "DependsOn" : "VPCGatewayAttach",
   "Type" : "AWS::EC2::EIP",
   "Properties" : {
      "Domain" : "vpc"
   }
},
"Route" : {
   "Type" : "AWS::EC2::Route",
   "Properties" : {
      "RouteTableId" : { "Ref" : "RouteTable" },
      "DestinationCidrBlock" : "0.0.0.0/0",
      "NatGatewayId" : { "Ref" : "NAT" }
   }
}
```

#### YAML<a name="aws-resource-ec2-natgateway--examples--NAT_gateway--yaml"></a>

```
NAT:
   Type: AWS::EC2::NatGateway
   Properties:
      AllocationId:
         Fn::GetAtt:
         - EIP
         - AllocationId
      SubnetId:
         Ref: Subnet
      Tags:
      - Key: stack
        Value: production
EIP:
   DependsOn: VPCGatewayAttach
   Type: AWS::EC2::EIP
   Properties:
      Domain: vpc
Route:
   Type: AWS::EC2::Route
   Properties:
      RouteTableId:
         Ref: RouteTable
      DestinationCidrBlock: 0.0.0.0/0
      NatGatewayId:
         Ref: NAT
```