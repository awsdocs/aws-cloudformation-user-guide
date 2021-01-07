# `Fn::Base64`<a name="intrinsic-function-reference-base64"></a>

The intrinsic function `Fn::Base64` returns the Base64 representation of the input string\. This function is typically used to pass encoded data to Amazon EC2 instances by way of the `UserData` property\.

## Declaration<a name="w7739ab1c33c28c12b5"></a>

### JSON<a name="intrinsic-function-reference-base64-syntax.json"></a>

```
{ "Fn::Base64" : valueToEncode }
```

### YAML<a name="intrinsic-function-reference-base64-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Base64: valueToEncode
```

Syntax for the short form:

```
!Base64 valueToEncode
```

**Note**  
If you use the short form and immediately include another function in the `valueToEncode` parameter, use the full function name for at least one of the functions\. For example, the following syntax is invalid:   

```
!Base64 !Sub string
!Base64 !Ref logical_ID
```
 Instead, use the full function name for at least one of the functions, as shown in the following examples:   

```
!Base64
  "Fn::Sub": string

Fn::Base64:
  !Sub string
```

## Parameters<a name="w7739ab1c33c28c12b7"></a>

valueToEncode  
The string value you want to convert to Base64\.

## Return value:<a name="w7739ab1c33c28c12b9"></a>

The original string, in Base64 representation\.

## Example<a name="w7739ab1c33c28c12c11"></a>

### JSON<a name="intrinsic-function-reference-base64-example.json"></a>

```
{ "Fn::Base64" : "AWS CloudFormation" }
```

### YAML<a name="intrinsic-function-reference-base64-example.yaml"></a>

```
Fn::Base64: AWS CloudFormation
```

## Supported functions<a name="w7739ab1c33c28c12c13"></a>

You can use any function that returns a string inside the `Fn::Base64` function\.

## See also<a name="w7739ab1c33c28c12c15"></a>
+ [Intrinsic Function Reference](intrinsic-function-reference.md)