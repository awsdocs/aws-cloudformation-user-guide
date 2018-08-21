# AWS::EC2::VPCDHCPOptionsAssociation<a name="aws-resource-ec2-vpc-dhcp-options-assoc"></a>

Associates a set of DHCP options \(that you've previously created\) with the specified VPC\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpcdhcpoptionsassociation-syntax)
+ [Properties](#w3ab2c21c10d519b9)
+ [Return Values](#w3ab2c21c10d519c11)
+ [Example](#w3ab2c21c10d519c13)
+ [See Also](#w3ab2c21c10d519c15)

## Syntax<a name="aws-resource-ec2-vpcdhcpoptionsassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcdhcpoptionsassociation-syntax.json"></a>

```
{ 
   "Type" : "AWS::EC2::VPCDHCPOptionsAssociation",
   "Properties" : {
      "[DhcpOptionsId](#cfn-ec2-vpcdhcpoptionsassociation-dhcpoptionsid)" : String,
      "[VpcId](#cfn-ec2-vpcdhcpoptionsassociation-vpcid)" : String
   }
}
```

### YAML<a name="aws-resource-ec2-vpcdhcpoptionsassociation-syntax.yaml"></a>

```
Type: "AWS::EC2::VPCDHCPOptionsAssociation"
Properties: 
  [DhcpOptionsId](#cfn-ec2-vpcdhcpoptionsassociation-dhcpoptionsid): String
  [VpcId](#cfn-ec2-vpcdhcpoptionsassociation-vpcid): String
```

## Properties<a name="w3ab2c21c10d519b9"></a>

`DhcpOptionsId`  <a name="cfn-ec2-vpcdhcpoptionsassociation-dhcpoptionsid"></a>
The ID of the DHCP options you want to associate with the VPC\. Specify `default` if you want the VPC to use no DHCP options\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-vpcdhcpoptionsassociation-vpcid"></a>
The ID of the VPC to associate with this DHCP options set\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d519c11"></a>

### Ref<a name="w3ab2c21c10d519c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d519c13"></a>

The following snippet uses the `Ref` intrinsic function to associate the `myDHCPOptions` DHCP options with the `myVPC` VPC\. The VPC and DHCP options can be declared in the same template or added as input parameters\. For more information about the VPC or the DHCP options resources, see [AWS::EC2::VPC](aws-resource-ec2-vpc.md) or [AWS::EC2::DHCPOptions](aws-resource-ec2-dhcp-options.md)\.

### JSON<a name="aws-resource-ec2-vpcdhcpoptionsassociation-example-1.json"></a>

```
"myVPCDHCPOptionsAssociation" : {
  "Type" : "AWS::EC2::VPCDHCPOptionsAssociation",
  "Properties" : {
    "VpcId" : {"Ref" : "myVPC"},
    "DhcpOptionsId" : {"Ref" : "myDHCPOptions"}
  }
}
```

### YAML<a name="aws-resource-ec2-vpcdhcpoptionsassociation-example-1.yaml"></a>

```
myVPCDHCPOptionsAssociation:
  Type: AWS::EC2::VPCDHCPOptionsAssociation
  Properties:
    VpcId:
      Ref: myVPC
    DhcpOptionsId:
      Ref: myDHCPOptions
```

## See Also<a name="w3ab2c21c10d519c15"></a>
+ [AssociateDhcpOptions](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-AssociateDhcpOptions.html) in the *Amazon EC2 API Reference*\.