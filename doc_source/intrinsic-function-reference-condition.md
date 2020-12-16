# Condition<a name="intrinsic-function-reference-condition"></a>

The intrinsic function `Condition` returns the evaluated result of the specified *condition*\.

When you are declaring a condition in a template and you need to use another condition in the evaluation, you can use `Condition` to refer to that other condition\. This is used when declaring a condition in the [Conditions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-conditions.html) section of the template\.

## Declaration<a name="intrinsic-function-reference-condition-declaration"></a>

### JSON<a name="intrinsic-function-reference-condition.json"></a>

```
{ "Condition" : "conditionName" }
```

### YAML<a name="intrinsic-function-reference-condition.yaml"></a>

Syntax for the full function name:

```
Condition: conditionName
```

Syntax for the short function name:

```
!Condition conditionName
```

## Parameters<a name="intrinsic-function-reference-condition-syntax-parameters"></a>

`conditionName`  
The name of the condition you want to reference\.

## Return Value<a name="intrinsic-function-reference-condition-syntax-return-value"></a>

The boolean result of the condition referenced\.

## Example<a name="intrinsic-function-reference-condition-syntax-example"></a>

The following snippet is from the `Conditions` section of a template\. The `MyAndCondition` condition includes the `SomeOtherCondition` condition:

### JSON<a name="intrinsic-function-reference-condition-mycondition-example.json"></a>

```
"MyAndCondition": {
   "Fn::And": [
      {"Fn::Equals": ["sg-mysggroup", {"Ref": "ASecurityGroup"}]},
      {"Condition": "SomeOtherCondition"}
   ]
}
```

### YAML<a name="intrinsic-function-reference-conditions-mycondition-example.yaml"></a>

```
MyAndCondition: !And
  - !Equals ["sg-mysggroup", !Ref "ASecurityGroup"]
  - !Condition SomeOtherCondition
```

## Supported functions<a name="intrinsic-function-reference-condition-syntax-supported-functions"></a>

You cannot use any functions in the `Condition` function\. You must specify a string that is a condition name\.