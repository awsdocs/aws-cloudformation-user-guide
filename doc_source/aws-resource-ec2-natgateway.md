# AWS::EC2::NatGateway<a name="aws-resource-ec2-natgateway"></a>

The `AWS::EC2::NatGateway` resource creates a network address translation \(NAT\) gateway in the specified public subnet\. Use a NAT gateway to allow instances in a private subnet to connect to the Internet or to other AWS services, but prevent the Internet from initiating a connection with those instances\. For more information and a sample architectural diagram, see [NAT Gateways](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-nat-gateway.html) in the *Amazon VPC User Guide*\.

**Note**  
If you add a default route \(`AWS::EC2::Route` resource\) that points to a NAT gateway, specify NAT gateway's ID for the route's `NatGatewayId` property\.

**Topics**
+ [Syntax](#aws-resource-ec2-natgateway-syntax)
+ [Properties](#w3ab2c21c10d423c11)
+ [Return Value](#w3ab2c21c10d423c13)
+ [Example](#w3ab2c21c10d423c15)

## Syntax<a name="aws-resource-ec2-natgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-natgateway-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NatGateway",
  "Properties" : {
    "[AllocationId](#cfn-ec2-natgateway-allocationid)" : String,
    "[SubnetId](#cfn-ec2-natgateway-subnetid)" : String,
    "[Tags](#cfn-ec2-natgateway-tags)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-ec2-natgateway-syntax.yaml"></a>

```
Type: "AWS::EC2::NatGateway"
Properties: 
  [AllocationId](#cfn-ec2-natgateway-allocationid): String
  [SubnetId](#cfn-ec2-natgateway-subnetid): String
  [Tags](#cfn-ec2-natgateway-tags): 
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d423c11"></a>

`AllocationId`  <a name="cfn-ec2-natgateway-allocationid"></a>
The allocation ID of an Elastic IP address to associate with the NAT gateway\. If the Elastic IP address is associated with another resource, you must first disassociate it\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SubnetId`  <a name="cfn-ec2-natgateway-subnetid"></a>
The public subnet in which to create the NAT gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-ec2-natgateway-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this resource\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d423c13"></a>

### Ref<a name="w3ab2c21c10d423c13b2"></a>

When you pass the logical ID of an `AWS::EC2::NatGateway` resource to the intrinsic `Ref` function, the function returns the ID of the NAT gateway, such as `nat-0a12bc456789de0fg`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d423c15"></a>

The following example creates a NAT gateway and a route that associates the NAT gateway with a route table\. The route table must be associated with an Internet gateway so that the NAT gateway can connect to the Internet\.

### JSON<a name="aws-resource-ec2-natgateway-example.json"></a>

```
"NAT" : {
  "DependsOn" : "VPCGatewayAttach",
  "Type" : "AWS::EC2::NatGateway",
  "Properties" : {
    "AllocationId" : { "Fn::GetAtt" : ["EIP", "AllocationId"]},
    "SubnetId" : { "Ref" : "Subnet"},
    "Tags" : [ {"Key" : "foo", "Value" : "bar" } ]
  }
},
"EIP" : {
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

### YAML<a name="aws-resource-ec2-natgateway-example.yaml"></a>

```
NAT:
  DependsOn: VPCGatewayAttach
  Type: AWS::EC2::NatGateway
  Properties:
    AllocationId:
      Fn::GetAtt:
      - EIP
      - AllocationId
    SubnetId:
      Ref: Subnet
    Tags:
      - Key: foo
        Value: bar
EIP:
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