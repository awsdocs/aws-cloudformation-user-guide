# `Fn::Join`<a name="intrinsic-function-reference-join"></a>

The intrinsic function `Fn::Join` appends a set of values into a single value, separated by the specified delimiter\. If a delimiter is the empty string, the set of values are concatenated with no delimiter\.

## Declaration<a name="w7739ab1c33c28c46b5"></a>

### JSON<a name="intrinsic-function-reference-join-syntax.json"></a>

```
{ "Fn::Join" : [ "delimiter", [ comma-delimited list of values ] ] }
```

### YAML<a name="intrinsic-function-reference-join-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Join: [ delimiter, [ comma-delimited list of values ] ]
```

Syntax for the short form:

```
!Join [ delimiter, [ comma-delimited list of values ] ]
```

## Parameters<a name="intrinsic-function-reference-join-parameters"></a>

delimiter  
The value you want to occur between fragments\. The delimiter will occur between fragments only\. It will not terminate the final value\.

ListOfValues  
The list of values you want combined\.

## Return value<a name="intrinsic-function-reference-join-returnvalues"></a>

The combined string\.

## Examples<a name="intrinsic-function-reference-join-examples"></a>

### Join a simple string array<a name="intrinsic-function-reference-join-example1"></a>

The following example returns: `"a:b:c"`\.

#### JSON<a name="intrinsic-function-reference-join-example1.json"></a>

```
1. "Fn::Join" : [ ":", [ "a", "b", "c" ] ]
```

#### YAML<a name="intrinsic-function-reference-join-example1.yaml"></a>

```
1. !Join [ ":", [ a, b, c ] ]
```

### Join using the ref function with parameters<a name="intrinsic-function-reference-join-example2"></a>

The following example uses `Fn::Join` to construct a string value\. It uses the `Ref` function with the `AWS::Partition` parameter and the `AWS::AccountId` pseudo parameter\.

#### JSON<a name="intrinsic-function-reference-join-example2.json"></a>

```
 1. {
 2.   "Fn::Join": [
 3.     "", [
 4.       "arn:",
 5.       {
 6.         "Ref": "AWS::Partition"
 7.       },
 8.       ":s3:::elasticbeanstalk-*-",
 9.       {
10.         "Ref": "AWS::AccountId"
11.       }
12.     ]
13.   ]
14. }
```

#### YAML<a name="intrinsic-function-reference-join-example2.yaml"></a>

```
1. !Join
2.   - ''
3.   - - 'arn:'
4.     - !Ref AWS::Partition
5.     - ':s3:::elasticbeanstalk-*-'
6.     - !Ref 'AWS::AccountId'
```

**Note**  
Also see the [`Fn::Sub`](intrinsic-function-reference-sub.md) function for similar functionality\.

## Supported functions<a name="intrinsic-function-reference-join-supportedfunctions"></a>

For the `Fn::Join` delimiter, you cannot use any functions\. You must specify a string value\.

For the `Fn::Join` list of values, you can use the following functions:
+ `Fn::Base64`
+ `Fn::FindInMap`
+ `Fn::GetAtt`
+ `Fn::GetAZs`
+ `Fn::If`
+ `Fn::ImportValue`
+ `Fn::Join`
+ `Fn::Split`
+ `Fn::Select`
+ `Fn::Sub`
+ `Ref`