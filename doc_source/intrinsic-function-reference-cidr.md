# `Fn::Cidr`<a name="intrinsic-function-reference-cidr"></a>

The intrinsic function `Fn::Cidr` returns the specified Cidr address block\.

## Declaration<a name="w3ab2c21c28c16b5"></a>

### JSON<a name="intrinsic-function-reference-cidr-syntax.json"></a>

```
{ "Fn::Cidr" : [ipBlock, count, sizeMask]}
```

### YAML<a name="intrinsic-function-reference-cidr-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Cidr: [ ipBlock, count, sizeMask ] 
```

Syntax for the short form:

```
!Cidr [ ipBlock, count, sizeMask ]
```

## Parameters<a name="w3ab2c21c28c16b7"></a>

ipBlock  
The user\-specified default Cidr address block\.

count  
The number of subnets' Cidr block wanted\. Count can be 1 to 256\.

sizeMask  
Optional\. The digit covered in the subnet\.

## Return Value<a name="w3ab2c21c28c16b9"></a>

The specified Cidr block\.

## Example<a name="intrinsic-function-reference-cidr-examples"></a>

### <a name="intrinsic-function-reference-cidr-example1"></a>

#### YAML<a name="intrinsic-function-reference-cidr-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
    cidrBlock :
        Type : String
    count:
        Type : String
    maskSizeForIPv4:
        Type: String
    maskSizeForIPv6:
        Type: String
Resources:
    Subnet1:
        Type: AWS::EC2::Subnet
        Properties:
            AssignIPv6AddressOnCreation: true
            VpcId: !Ref VPC
            #Test Ipv4 CidrBlock
            CidrBlock: !Select [0, !Cidr [!Ref cidrBlock, !Ref count, !Ref maskSizeForIPv4]]
            #Test Ipv6 CidrBlock
            Ipv6CidrBlock: !Select [0, !Cidr [!Select [0, !GetAtt VPC.Ipv6CidrBlocks], !Ref count, !Ref maskSizeForIPv6]]
        DependsOn: Ipv6VPCCidrBlock
    Subnet2:
        Type: AWS::EC2::Subnet
        Properties:
            AssignIPv6AddressOnCreation: true
            VpcId: !Ref VPC
            #Test Ipv4 CidrBlock
            CidrBlock: !Select [1, !Cidr [!Ref cidrBlock, !Ref count, !Ref maskSizeForIPv4]]
            #Test Ipv6 CidrBlock
            Ipv6CidrBlock: !Select [1, !Cidr [!Select [0, !GetAtt VPC.Ipv6CidrBlocks], !Ref count, !Ref maskSizeForIPv6]]
        DependsOn: Ipv6VPCCidrBlock
    VPC:
        Type: AWS::EC2::VPC
        Properties:
          CidrBlock: !Ref cidrBlock
    Ipv6VPCCidrBlock:
        Type: AWS::EC2::VPCCidrBlock
        Properties:
            AmazonProvidedIpv6CidrBlock: true
            VpcId: !Ref VPC
```

## Supported Functions<a name="w3ab2c21c28c16c13"></a>

You can use the following functions in a `Fn::Cidr` function:
+ `[`Fn::Select`](intrinsic-function-reference-select.md)` 
+ `[`Ref`](intrinsic-function-reference-ref.md)` 