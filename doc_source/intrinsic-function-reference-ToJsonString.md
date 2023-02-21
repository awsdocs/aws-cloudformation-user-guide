# `Fn::ToJsonString`<a name="intrinsic-function-reference-ToJsonString"></a>

The `Fn::ToJsonString` intrinsic function converts an object or array to its corresponding JSON string\.

**Important**  
You must use the [AWS::LanguageExtensions transform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-languageextension-transform.html) to use the `Fn::ToJsonString` intrinsic function\.

## Declaration<a name="tojsonstring-declaration"></a>

### JSON<a name="intrinsic-function-reference-tojsonstring-syntax.json"></a>

```
{ "Fn::ToJsonString": Object }
```

```
{ "Fn::ToJsonString": Array }
```

### YAML<a name="intrinsic-function-reference-tojsonstring-syntax.yaml"></a>

```
Fn::ToJsonString: Object
```

```
Fn::ToJsonString: Array
```

## Parameters<a name="tojsonstring-parameters"></a>

`Object`  
The object you want to convert to a JSON string\.

`Array`  
The array you want to convert to a JSON string\.

## Return value<a name="intrinsic-function-reference-tojsonstring-return"></a>

The object or array converted to a JSON string\. 

## Examples<a name="intrinsic-function-reference-tojsonstring-examples"></a>

### Convert an object to a JSON string<a name="intrinsic-function-reference-tojsonstring-example"></a>

This example snippet converts the object passed to the intrinsic function to a JSON string\.

#### JSON<a name="intrinsic-function-reference-tojsonstring-example.json"></a>

```
 1. {
 2. //...
 3.     "Transform": "AWS::LanguageExtensions"
 4.     //...
 5.         "Fn::ToJsonString": {
 6.             "key1": "value1",
 7.             "key2": { 
 8.                 "Ref": "ParameterName"
 9.             }
10.         }
11. //...
12. }
```

#### YAML<a name="intrinsic-function-reference-tojsonstring-example.yaml"></a>

```
1. Transform: 'AWS::LanguageExtensions'
2. #...
3.   Fn::ToJsonString: 
4.     key1: value1
5.     key2: !Ref ParameterName
6. #...
```

In both of these examples, if the `Ref` to `ParameterName` resolves to `resolvedValue`, the function resolves to the following JSON string:

```
1. "{\"key1\":\"value1\"},{\"key2\":\"resolvedValue\"}"
```

### Convert an array to a JSON string<a name="intrinsic-function-reference-tojsonstring-example2"></a>

This example snippet converts the array passed to the intrinsic function to a JSON string\.

#### JSON<a name="intrinsic-function-reference-tojsonstring-example2.json"></a>

```
 1. {
 2. //...
 3.     "Transform": "AWS::LanguageExtensions"
 4.     //...
 5.         "Fn::ToJsonString": [{
 6.             "key1": "value1",
 7.             "key2": { 
 8.                 "Ref": "ParameterName" 
 9.             }
10.         }]
11. //...
12. }
```

#### YAML<a name="intrinsic-function-reference-tojsonstring-example2.yaml"></a>

```
1. Transform: 'AWS::LanguageExtensions'
2. #...
3.   Fn::ToJsonString: 
4.     - key1: value1
5.       key2: !Ref ParameterName
6. #...
```

In both of these examples, if the `Ref` to `ParameterName` resolves to `resolvedValue`, the function resolves to the following JSON String:

```
"[{\"key1\":\"value1\"},{\"key2\":\"resolvedValue\"}]"
```

## Supported functions<a name="tojsonstring-supported-functions"></a>

You can use the following functions in the `Fn::ToJsonString` intrinsic function or array:
+ `Fn::Base64`
+ `Fn::FindInMap`
+ `Fn::GetAtt`
+ `Fn::GetAZs`
+ `Fn::If`
+ `Fn::ImportValue`
+ `Fn::Join`
+ `Fn::Length`
+ `Fn::Select`
+ `Fn::Split`
+ `Fn::Sub`
+ `Fn::ToJsonString`
+ `Ref`