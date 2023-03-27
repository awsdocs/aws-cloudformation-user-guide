# `Fn::FindInMap enhancements`<a name="intrinsic-function-reference-findinmap-enhancements"></a>

When you add the `AWS::LanguageExtensions` transform in a AWS CloudFormation template, you can use intrinsic functions to define the fields of `Fn::FindInMap`\. You can also use a new optional field to return a default value if a mapping is not found\.

For more information about the `AWS::LanguageExtensions` transform, see [AWS::LanguageExtensions transform](transform-aws-languageextensions.md)\.

For more information about the `Fn::FindInMap` intrinsic function, see [`Fn::FindInMap`](intrinsic-function-reference-findinmap.md)\.

## Declaration<a name="intrinsic-function-reference-findinmap-enhancements-declaration"></a>

### JSON<a name="intrinsic-function-reference-findinmap-enhancements-syntax.json"></a>

```
{ "Fn::FindInMap" : [
    "MapName",
    "TopLevelKey",
    "SecondLevelKey",
    {"DefaultValue": "DefaultValue"}
  ]
}
```

### YAML<a name="intrinsic-function-reference-findinmap-enhancements-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::FindInMap:
  - MapName
  - TopLevelKey
  - SecondLevelKey
  - DefaultValue: DefaultValue
```

Syntax for the short form:

```
!FindInMap
  - MapName
  - TopLevelKey
  - SecondLevelKey
  - DefaultValue: DefaultValue
```

**Note**  


## Parameters<a name="intrinsic-function-reference-findinmap-enhancements-parameters"></a>

DefaultValue  <a name="DefaultValue"></a>
The value that `Fn::FindInMap` will resolve to if the `TopLevelKey` and/or `SecondLevelKey` can not be found from the `MapName` map\. This field is optional\.

All parameters `MapName`, `TopLevelKey`, `SecondLevelKey`, and `DefaultValue` can be an intrinsic function as long as it's able to resolve to a valid value during the transform\.

## Example<a name="intrinsic-function-reference-findinmap-enhancements-example"></a>

The following is an example of using intrinsic functions to define the top level key:

### JSON<a name="intrinsic-function-reference-findinmap-enhancement-example.json"></a>

```
 1. {
 2. //...
 3.     "Transform": "AWS::LanguageExtensions",
 4.     //...
 5.         "Fn::FindInMap": [
 6.             "MyMap",
 7.             "Fn::Select": [
 8.                 0,
 9.                 "Fn::Split": [
10.                     "|",
11.                     { "Ref": "InputKeys" }
12.                 ]
13.             ],
14.             "SecondKey"
15.         ]
16. //...
17. }
```

### YAML<a name="intrinsic-function-reference-findinmap-example.yaml"></a>

```
Transform: 'AWS::LanguageExtensions'
#...
    !FindInMap: [MyMap, !Select [0, !Split [|, !Ref InputKeys]], SecondKey]
#...
```

The following is an example of using default values:

### JSON<a name="intrinsic-function-reference-findinmap-enhancement-example2.json"></a>

```
 1. {
 2. //...
 3.     "Transform": "AWS::LanguageExtensions",
 4.     //...
 5.     "Fn::FindInMap": [
 6.         "InstanceConfiguration",
 7.         { "Ref": "AWS::Region" },
 8.         "Type",
 9.         { "DefaultValue": "m5.small" }
10.     ]
11. //...
12. }
```

### YAML<a name="intrinsic-function-reference-findinmap-example2.yaml"></a>

```
Transform: 'AWS::LanguageExtensions'
#...
    !FindInMap 
        - 'InstanceConfiguration'
        - !Ref 'AWS::Region'
        - 'Type'
        - DefaultValue: m5.small
#...
```

## Supported functions<a name="intrinsic-function-reference-findinmap-enhancements-supported-functions"></a>

You can use the following functions in the parameters of `Fn::FindInMap:` enhancements:
+ `Fn::FindInMap`
+ `Fn::Join`
+ `Fn::Sub`
+ `Fn::If`
+ `Fn::Select`
+ `Fn::Length`
+ `Fn::ToJsonString`
+ `Fn::Split` \- Unless it’s used for the default value, `Fn::Split` has to be used in conjunction with intrinsic functions that produce a string, such as `Fn::Join` or `Fn::Select`\.
+ `Ref`