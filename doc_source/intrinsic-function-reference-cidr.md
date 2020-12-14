# `Fn::Cidr`<a name="intrinsic-function-reference-cidr"></a>

The intrinsic function `Fn::Cidr` returns an array of CIDR address blocks\. The number of CIDR blocks returned is dependent on the `count` parameter\.

## Declaration<a name="intrinsic-function-reference-cidr-declaration"></a>

### JSON<a name="intrinsic-function-reference-cidr-syntax.json"></a>

```
{ "Fn::Cidr" : [ipBlock, count, cidrBits]}
```

### YAML<a name="intrinsic-function-reference-cidr-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Cidr: 
  - ipBlock 
  - count
  - cidrBits
```

Syntax for the short form:

```
!Cidr [ ipBlock, count, cidrBits ]
```

## Parameters<a name="intrinsic-function-reference-cidr-parameters"></a>

ipBlock  
The user\-specified CIDR address block to be split into smaller CIDR blocks\.

count  
The number of CIDRs to generate\. Valid range is between 1 and 256\.

cidrBits  
The number of subnet bits for the CIDR\. For example, specifying a value "8" for this parameter will create a CIDR with a mask of "/24"\.  
Subnet bits is the inverse of subnet mask\. To calculate the required host bits for a given subnet bits, subtract the subnet bits from 32 for IPv4 or 128 for IPv6\.

## Return value<a name="intrinsic-function-reference-cidr-return-values"></a>

An array of CIDR address blocks\.

## Example<a name="intrinsic-function-reference-cidr-examples"></a>

### Basic usage<a name="intrinsic-function-reference-cidr-example1"></a>

This example creates 6 CIDRs with a subnet mask "/27" inside from a CIDR with a mask of "/24"\.

#### JSON<a name="intrinsic-function-reference-cidr-example1.json"></a>

```
{ "Fn::Cidr" : [ "192.168.0.0/24", "6", "5"] }
```

#### YAML<a name="intrinsic-function-reference-cidr-example1.yaml"></a>

```
!Cidr [ "192.168.0.0/24", 6, 5 ]
```

### Creating an IPv6 enabled VPC<a name="intrinsic-function-reference-cidr-example2"></a>

This example template creates an IPv6 enabled subnet\.

#### JSON<a name="intrinsic-function-reference-cidr-example2.json"></a>

```
{
  "Resources" : {
    "ExampleVpc" : {
      "Type" : "AWS::EC2::VPC",
      "Properties" : {
        "CidrBlock" : "10.0.0.0/16"
      }
    },
    "IPv6CidrBlock" : {
      "Type" : "AWS::EC2::VPCCidrBlock",
      "Properties" : {
        "AmazonProvidedIpv6CidrBlock" : true,
        "VpcId" : { "Ref" : "ExampleVpc" }
      }
    },
    "ExampleSubnet" : {
      "Type" : "AWS::EC2::Subnet",
      "DependsOn" : "IPv6CidrBlock",
      "Properties" : {
        "AssignIpv6AddressOnCreation" : true,
        "CidrBlock" : { "Fn::Select" : [ 0, { "Fn::Cidr" : [{ "Fn::GetAtt" : [ "ExampleVpc", "CidrBlock" ]}, 1, 8 ]}]},
        "Ipv6CidrBlock" : { "Fn::Select" : [ 0, { "Fn::Cidr" : [{ "Fn::Select" : [ 0, { "Fn::GetAtt" : [ "ExampleVpc", "Ipv6CidrBlocks" ]}]}, 1, 64 ]}]},
        "VpcId" : { "Ref" : "ExampleVpc" }
      }
    }
  }
}
```

#### YAML<a name="intrinsic-function-reference-cidr-example2.yaml"></a>

```
Resources:
    ExampleVpc:
        Type: AWS::EC2::VPC
        Properties:
            CidrBlock: "10.0.0.0/16"
     IPv6CidrBlock:
        Type: AWS::EC2::VPCCidrBlock
        Properties:
            AmazonProvidedIpv6CidrBlock: true
            VpcId: !Ref ExampleVpc
     ExampleSubnet:
        Type: AWS::EC2::Subnet
        DependsOn: IPv6CidrBlock
        Properties:
            AssignIpv6AddressOnCreation: true
            CidrBlock: !Select [ 0, !Cidr [ !GetAtt ExampleVpc.CidrBlock, 1, 8 ]]
            Ipv6CidrBlock: !Select [ 0, !Cidr [ !Select [ 0, !GetAtt ExampleVpc.Ipv6CidrBlocks], 1, 64 ]]
            VpcId: !Ref ExampleVpc
```

## Supported functions<a name="intrinsic-function-reference-cidr-functions"></a>

You can use the following functions in a `Fn::Cidr` function:
+ ``Fn::Select`` 
+ ``Ref`` 