# `Fn::Cidr`<a name="intrinsic-function-reference-cidr"></a>

The intrinsic function `Fn::Cidr` returns an array of Cidr address blocks\. The number of Cidr blocks returned is dependent on the count parameter\.

## Declaration<a name="w3ab2c21c28c37b5"></a>

### JSON<a name="intrinsic-function-reference-getcidr-syntax.json"></a>

```
{ "Fn::Cidr" : [ipBlock, count, sizeMask] }
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
The number of subnets to generate. Valid values for count are 1 to 256\.

sizeMask  
The number of host bits for the subnet\. For example, a sizeMask of "8" will create a subnet with a range of "/24".


## Return Value<a name="w3ab2c21c28c37b9"></a>

An array of Cidr address blocks\.


## Supported Functions<a name="w3ab2c21c28c37c13"></a>

You can use the following functions in a `Fn::Cidr` function:

+ `[`Fn::Select`](intrinsic-function-reference-select.md)` 

+ `[`Ref`](intrinsic-function-reference-ref.md)` 