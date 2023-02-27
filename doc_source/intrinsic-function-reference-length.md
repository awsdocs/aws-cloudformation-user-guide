# `Fn::Length`<a name="intrinsic-function-reference-length"></a>

The intrinsic function `Fn::Length` returns the number of elements within an array or an intrinsic function that returns an array\.

**Important**  
You must use the [AWS::LanguageExtensions transform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-languageextension-transform.html) to use the `Fn::Length` intrinsic function\.

## Declaration<a name="length-declaration"></a>

### JSON<a name="intrinsic-function-reference-length-syntax.json"></a>

```
{ "Fn::Length" : IntrinsicFunction }
```

```
{ "Fn::Length" : Array }
```

### YAML<a name="intrinsic-function-reference-length-syntax.yaml"></a>

```
Fn::Length : IntrinsicFunction
```

```
Fn::Length : Array
```

## Parameters<a name="length-parameters"></a>

`IntrinsicFunction`  
The intrinsic function that returns an array that you want to return a number of elements from\.

`Array`  
The array you want to return the number of elements from\.

## Return value<a name="intrinsic-function-reference-length-return"></a>

The number of elements in the intrinsic function that returns an array or in the array passed to the intrinsic function\. 

## Examples<a name="intrinsic-function-reference-length-examples"></a>

### Return the number of elements in an intrinsic function that returns an array<a name="intrinsic-function-reference-length-example"></a>

This example snippet returns the number of elements in an intrinsic function that returns an array\. The function returns 3\.

#### JSON<a name="intrinsic-function-reference-length-example.json"></a>

```
1. {
2. //...
3.     "Transform": "AWS::LanguageExtensions"
4.     //...
5.         "Fn::Length" : {
6.             "Fn::Split": ["|", "a|b|c"]
7.         }
8. //...
9. }
```

#### YAML<a name="intrinsic-function-reference-length-example.yaml"></a>

```
1. Transform: 'AWS::LanguageExtensions'
2. #...
3.   Fn::Length: 
4.     !Split ["|", "a|b|c"]
5. #...
```

### Return the number of elements in a Ref intrinsic function that refers to a list parameter type<a name="intrinsic-function-reference-length-example2"></a>

This example snippet returns the number of elements in a `Ref` intrinsic function that refers to a list parameter type\. If the parameter with the name `ListParameter` is a list with 3 elements, the function returns 3\.

#### JSON<a name="intrinsic-function-reference-length-example2.json"></a>

```
1. {
2. //...
3.     "Transform": "AWS::LanguageExtensions"
4.     //...
5.         "Fn::Length": {
6.             "Ref": "ListParameter"
7.         }
8. //...
9. }
```

#### YAML<a name="intrinsic-function-reference-length-example2.yaml"></a>

```
1. Transform: 'AWS::LanguageExtensions'
2. #...
3.   Fn::Length: 
4.     !Ref ListParameter
5. #...
```

### Return the number of elements in an array<a name="intrinsic-function-reference-length-example3"></a>

This example snippet returns the number of elements in the array passed to the intrinsic function\. The function returns 3\.

#### JSON<a name="intrinsic-function-reference-length-example3.json"></a>

```
 1. {
 2. //...
 3.     "Transform": "AWS::LanguageExtensions"
 4.     //...
 5.         "Fn::Length": [
 6.             1,
 7.             {"Ref": "ParameterName"}, 
 8.             3
 9.         ]
10. //...
11. }
```

#### YAML<a name="intrinsic-function-reference-length-example3.yaml"></a>

```
1. Transform: 'AWS::LanguageExtensions'
2. #...
3.   Fn::Length: 
4.     - 1
5.     - !Ref ParameterName
6.     - 3
7. #...
```

## Supported functions<a name="length-supported-functions"></a>

You can use the following functions in the `Fn::Length` intrinsic function or array:
+ `Condition Functions`
+ `Fn::Base64`
+ `Fn::FindInMap`
+ `Fn::Join`
+ `Fn::Length`
+ `Fn::Select`
+ `Fn::Split`
+ `Fn::Sub`
+ `Fn::ToJsonString`
+ `Ref`