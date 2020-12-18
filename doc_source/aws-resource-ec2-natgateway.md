# AWS::EC2::NatGateway<a name="aws-resource-ec2-natgateway"></a>

Specifies a network address translation \(NAT\) gateway in the specified public subnet\. Use a NAT gateway to allow instances in a private subnet to connect to the Internet or to other AWS services, but prevent the Internet from initiating a connection with those instances\. For more information and a sample architectural diagram, see [NAT Gateways](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html) in the *Amazon VPC User Guide*\.

If you add a default route \(`AWS::EC2::Route` resource\) that points to a NAT gateway, specify the NAT gateway ID for the route's `NatGatewayId` property\.

## Syntax<a name="aws-resource-ec2-natgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-natgateway-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NatGateway",
  "Properties" : {
      "[AllocationId](#cfn-ec2-natgateway-allocationid)" : String,
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
  [SubnetId](#cfn-ec2-natgateway-subnetid): String
  [Tags](#cfn-ec2-natgateway-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-natgateway-properties"></a>

`AllocationId`  <a name="cfn-ec2-natgateway-allocationid"></a>
The allocation ID of an Elastic IP address to associate with the NAT gateway\. If the Elastic IP address is associated with another resource, you must first disassociate it\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-ec2-natgateway-subnetid"></a>
The public subnet in which to create the NAT gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-natgateway-tags"></a>
The tags \(key\-value pairs\) to associate with this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-natgateway-return-values"></a>

### Ref<a name="aws-resource-ec2-natgateway-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example, `nat-0a12bc456789de0fg`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-natgateway--examples"></a>



### NAT Gateway<a name="aws-resource-ec2-natgateway--examples--NAT_Gateway"></a>

The following example creates a NAT gateway and a route that associates the NAT gateway with a route table\. The route table must be associated with an Internet gateway so that the NAT gateway can connect to the Internet\.

#### JSON<a name="aws-resource-ec2-natgateway--examples--NAT_Gateway--json"></a>

```
"NAT" : {
   "Type" : "AWS::EC2::NatGateway",
   "Properties" : {
      "AllocationId" : { "Fn::GetAtt" : ["EIP", "AllocationId"]},
      "SubnetId" : { "Ref" : "Subnet"},
      "Tags" : [ {"Key" : "foo", "Value" : "bar" } ]
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

#### YAML<a name="aws-resource-ec2-natgateway--examples--NAT_Gateway--yaml"></a>

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
      - Key: foo
        Value: bar
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