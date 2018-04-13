# `Fn::Cidr`<a name="intrinsic-function-reference-cidr"></a>

The intrinsic function `Fn::Cidr` returns an array of CIDR address blocks\. The number of CIDR blocks returned is dependent on the count parameter\.

## Declaration<a name="w3ab2c21c28c37b5"></a>

### JSON<a name="intrinsic-function-reference-getcidr-syntax.json"></a>

```
{ "Fn::Cidr" : [ipBlock, count, cidrBits] }
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

## Parameters<a name="w3ab2c21c28c37b7"></a>

ipBlock  
The user\-specified CIDR address block to be split into smaller CIDR blocks\.

count  
The number of CIDRs to generate. Valid range is between 1 and 256\.

cidrBits  
The number of subnet bits for the CIDR\. For example, cidrBits of "8" will create a CIDR with a mask of "/24".

**Note**
Subnet bits is the inverse of subnet mask\. To workout the required host bits for a given subnet bits, subtract the subnet bits from 32 for IPv4 or 128 for IPv6\.

## Return Value<a name="w3ab2c21c28c37b9"></a>

An array of CIDR address blocks\.

## Supported Functions<a name="w3ab2c21c28c37c13"></a>

You can use the following functions in a `Fn::Cidr` function:

+ `[`Fn::Select`](intrinsic-function-reference-select.md)` 

+ `[`Ref`](intrinsic-function-reference-ref.md)` 

+ `[`Fn::GetAtt`](intrinsic-function-reference-getatt.md)` 

## Examples

### Basic Usage

This example create 6 CIDRs with a subnet mask "/27" inside from a CIDR with a mask of "/24":

### JSON
```
{ "Fn::Cidr" : [ "192.168.0.0/24", "6", "5"] }
```

### YAML

```
!Cidr [ "192.168.0.0/24", 6, 5 ]
```

## Creating an IPv6 enabled VPC

This example template creates an IPv6 enabled subnet:

### JSON
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

### YAML

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
