# `Fn::Select`<a name="intrinsic-function-reference-select"></a>

The intrinsic function `Fn::Select` returns a single object from a list of objects by index\.

**Important**  
Fn::Select does not check for null values or if the index is out of bounds of the array\. Both conditions will result in a stack error, so you should be certain that the index you choose is valid, and that the list contains non\-null values\.

## Declaration<a name="w7739ab1c33c28c51b7"></a>

### JSON<a name="intrinsic-function-reference-select-syntax.json"></a>

```
{ "Fn::Select" : [ index, listOfObjects ] }
```

### YAML<a name="intrinsic-function-reference-select-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Select: [ index, listOfObjects ] 
```

Syntax for the short form:

```
!Select [ index, listOfObjects ]
```

## Parameters<a name="w7739ab1c33c28c51b9"></a>

index  
The index of the object to retrieve\. This must be a value from zero to N\-1, where N represents the number of elements in the array\.

listOfObjects  
The list of objects to select from\. This list must not be null, nor can it have null entries\.

## Return value<a name="w7739ab1c33c28c51c11"></a>

The selected object\.

## Examples<a name="w7739ab1c33c28c51c13"></a>

### Basic example<a name="w7739ab1c33c28c51c13b2"></a>

The following example returns: `"grapes"`\.

#### JSON<a name="intrinsic-function-reference-select-example0.json"></a>

```
{ "Fn::Select" : [ "1", [ "apples", "grapes", "oranges", "mangoes" ] ] }
```

#### YAML<a name="intrinsic-function-reference-select-example0.yaml"></a>

```
!Select [ "1", [ "apples", "grapes", "oranges", "mangoes" ] ]
```

 

### Comma\-delimited list parameter type<a name="w7739ab1c33c28c51c13b4"></a>

You can use `Fn::Select` to select an object from a `CommaDelimitedList` parameter\. You might use a `CommaDelimitedList` parameter to combine the values of related parameters, which reduces the total number of parameters in your template\. For example, the following parameter specifies a comma\-delimited list of three CIDR blocks:

#### JSON<a name="intrinsic-function-reference-select-example1.json"></a>

```
1. "Parameters" : {
2.   "DbSubnetIpBlocks": {
3.     "Description": "Comma-delimited list of three CIDR blocks",
4.     "Type": "CommaDelimitedList",
5.       "Default": "10.0.48.0/24, 10.0.112.0/24, 10.0.176.0/24"
6.   }
7. }
```

#### YAML<a name="intrinsic-function-reference-select-example1.yaml"></a>

```
1. Parameters: 
2.   DbSubnetIpBlocks: 
3.     Description: "Comma-delimited list of three CIDR blocks"
4.     Type: CommaDelimitedList
5.     Default: "10.0.48.0/24, 10.0.112.0/24, 10.0.176.0/24"
```

To specify one of the three CIDR blocks, use `Fn::Select` in the Resources section of the same template, as shown in the following sample snippet:

#### JSON<a name="intrinsic-function-reference-select-example2.json"></a>

```
"Subnet0": {
  "Type": "AWS::EC2::Subnet",
    "Properties": {
      "VpcId": { "Ref": "VPC" },
      "CidrBlock": { "Fn::Select" : [ "0", {"Ref": "DbSubnetIpBlocks"} ] }
    }
}
```

#### YAML<a name="intrinsic-function-reference-select-example2.yaml"></a>

```
Subnet0: 
  Type: "AWS::EC2::Subnet"
  Properties: 
    VpcId: !Ref VPC
    CidrBlock: !Select [ 0, !Ref DbSubnetIpBlocks ]
```

 

### Nested functions with short form YAML<a name="w7739ab1c33c28c51c13b6"></a>

The following examples show valid patterns for using nested intrinsic functions with the `!Select` short form\. You can't nest short form functions consecutively, so a pattern like `!GetAZs !Ref` is invalid\.

#### YAML<a name="intrinsic-function-reference-select-example3.yaml"></a>

```
1. AvailabilityZone: !Select 
2.   - 0
3.   - !GetAZs 
4.     Ref: 'AWS::Region'
```

#### YAML<a name="intrinsic-function-reference-select-example4.yaml"></a>

```
1. AvailabilityZone: !Select 
2.   - 0
3.   - Fn::GetAZs: !Ref 'AWS::Region'
```

## Supported functions<a name="w7739ab1c33c28c51c15"></a>

For the `Fn::Select` index value, you can use the `Ref` and `Fn::FindInMap` functions\.

For the `Fn::Select` list of objects, you can use the following functions:
+ `Fn::FindInMap`
+ `Fn::GetAtt`
+ `Fn::GetAZs`
+ `Fn::If`
+ `Fn::Split`
+ `Ref`