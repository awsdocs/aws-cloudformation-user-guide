# `Fn::GetCidr`<a name="intrinsic-function-reference-getcidr"></a>

The intrinsic function `Fn::GetCidr` returns the specified Cidr address block\.

## Declaration<a name="w3ab2c21c28c37b5"></a>

### JSON<a name="intrinsic-function-reference-getcidr-syntax.json"></a>

```
{ "Fn::GetCidr" : [ipBlock, count, sizeMask]}
```

### YAML<a name="intrinsic-function-reference-cidr-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::GetCidr: [ ipBlock, count, sizeMask ] 
```

Syntax for the short form:

```
!GetCidr [ ipBlock, count, sizeMask ]
```

## Parameters<a name="w3ab2c21c28c37b7"></a>

ipBlock  
The user\-specified default Cidr address block\.

count  
The number of subnets' Cidr block wanted\. Count can be 1 to 256\.

sizeMask  
Optional\. The digit covered in the subnet\.

## Return Value<a name="w3ab2c21c28c37b9"></a>

The specified Cidr block\.

## Supported Functions<a name="w3ab2c21c28c37c13"></a>

You can use the following functions in a `Fn::GetCidr` function:

+ `[`Fn::Select`](intrinsic-function-reference-select.md)` 

+ `[`Ref`](intrinsic-function-reference-ref.md)` 