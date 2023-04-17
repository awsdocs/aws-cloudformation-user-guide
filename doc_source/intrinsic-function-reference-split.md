# `Fn::Split`<a name="intrinsic-function-reference-split"></a>

To split a string into a list of string values so that you can select an element from the resulting string list, use the `Fn::Split` intrinsic function\. Specify the location of splits with a delimiter, such as `,` \(a comma\)\. After you split a string, use the [`Fn::Select`](intrinsic-function-reference-select.md) function to pick a specific element\.

For example, if a comma\-delimited string of subnet IDs is imported to your stack template, you can split the string at each comma\. From the list of subnet IDs, use the `Fn::Select` intrinsic function to specify a subnet ID for a resource\.

## Declaration<a name="w4ab1c33c28c60b7"></a>

### JSON<a name="intrinsic-function-reference-split-syntax.json"></a>

```
{ "Fn::Split" : [ "delimiter", "source string" ] }
```

### YAML<a name="intrinsic-function-reference-split-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Split: [ delimiter, source string ]
```

Syntax for the short form:

```
!Split [ delimiter, source string ]
```

## Parameters<a name="w4ab1c33c28c60b9"></a>

You must specify both parameters\.

delimiter  
A string value that determines where the source string is divided\.

source string  
The string value that you want to split\.

## Return value<a name="w4ab1c33c28c60c11"></a>

A list of string values\.

## Examples<a name="w4ab1c33c28c60c13"></a>

The following examples demonstrate the behavior of the `Fn::Split` function\.

### Simple list<a name="w4ab1c33c28c60c13b5"></a>

The following example splits a string at each vertical bar \(`|`\)\. The function returns `["a", "b", "c"]`\.

#### JSON<a name="intrinsic-function-reference-split-example.json"></a>

```
1. { "Fn::Split" : [ "|" , "a|b|c" ] }
```

#### YAML<a name="intrinsic-function-reference-split-example.yaml"></a>

```
1. !Split [ "|" , "a|b|c" ]
```

 

### List with empty string values<a name="w4ab1c33c28c60c13b7"></a>

If you split a string with consecutive delimiters, the resulting list will include an empty string\. The following example shows how a string with two consecutive delimiters and an appended delimiter is split\. The function returns `["a", "", "c", ""]`\.

#### JSON<a name="w4ab1c33c28c60c13b7b5"></a>

```
1. { "Fn::Split" : [ "|" , "a||c|" ] }
```

#### YAML<a name="w4ab1c33c28c60c13b7b7"></a>

```
1. !Split [ "|" , "a||c|" ]
```

 

### Split an imported output value<a name="w4ab1c33c28c60c13b9"></a>

The following example splits an imported output value, and then selects the third element from the resulting list of subnet IDs, as specified by the `Fn::Select` function\.

#### JSON<a name="w4ab1c33c28c60c13b9b5"></a>

```
1. { "Fn::Select" : [ "2", { "Fn::Split": [",", {"Fn::ImportValue": "AccountSubnetIDs"}]}] }
```

#### YAML<a name="w4ab1c33c28c60c13b9b7"></a>

```
1. !Select [2, !Split [",", !ImportValue AccountSubnetIDs]]
```

## Supported functions<a name="w4ab1c33c28c60c15"></a>

For the `Fn::Split` delimiter, you can't use any functions\. You must specify a string value\.

For the `Fn::Split` list of values, you can use the following functions:
+ `Fn::Base64`
+ `Fn::FindInMap`
+ `Fn::GetAtt`
+ `Fn::GetAZs`
+ `Fn::If`
+ `Fn::ImportValue`
+ `Fn::Join`
+ `Fn::Select`
+ `Fn::Sub`
+ `Ref`