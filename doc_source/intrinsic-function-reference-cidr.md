# `Fn::Cidr`<a name="intrinsic-function-reference-cidr"></a>

The intrinsic function `Fn::Cidr` returns the specified Cidr address block\.

## Declaration<a name="w3ab2c21c28c37b5"></a>

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

## Parameters<a name="w3ab2c21c28c37b7"></a>

ipBlock  
The user\-specified default Cidr address block\.

count  
The number of subnets' Cidr block wanted\. Count can be 1 to 256\.

sizeMask  
The digit covered in the subnet\.

## Return Value<a name="w3ab2c21c28c37b9"></a>

The specified Cidr block\.

## Supported Functions<a name="w3ab2c21c28c37c13"></a>

You can use the following functions in a `Fn::Cidr` function:

+ `[`Fn::Select`](intrinsic-function-reference-select.md)` 

+ `[`Ref`](intrinsic-function-reference-ref.md)` 


## Example

In order to use the "Fn::Cidr" function to create 6 subnets with mask "/27" inside a "/24" mask VPC, you should use the below values:

+ VpcCidr: "192.168.0.0/24"
+ CidrCount: "6"
+ sizeMask: "5" (i.e. 32-27=5)
