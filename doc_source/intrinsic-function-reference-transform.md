# `Fn::Transform`<a name="intrinsic-function-reference-transform"></a>

The intrinsic function `Fn::Transform` specifies a macro to perform custom processing on part of a stack template\. Macros enable you to perform custom processing on templates, from simple actions like find\-and\-replace operations to extensive transformations of entire templates\. For more information, see [Using AWS CloudFormation macros to perform custom processing on templates](template-macros.md)\.

You can also use `Fn::Transform` to call the `AWS::Include transform` transform, which is a macro hosted by AWS CloudFormation\.

## Declaration<a name="intrinsic-function-reference-transform-declaration"></a>

### JSON<a name="intrinsic-function-reference-transform-syntax.json"></a>

Syntax for the full function name:

```
{
    "Fn::Transform": {
        "Name": "macro name",
        "Parameters": {
            "Key": "value"
        }
    }
}
```

Syntax for the short form:

```
{
    "Transform": {
        "Name": "macro name",
        "Parameters": {
            "Key": "value"
        }
    }
}
```

### YAML<a name="intrinsic-function-reference-transform-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Transform:
  Name : macro name
  Parameters :
          Key : value
```

Syntax for the short form:

```
Transform:
  Name: macro name
  Parameters:
    Key: value
```

## Parameters<a name="intrinsic-function-reference-transform-parameters"></a>

Name  
The name of the macro you want to perform the processing\.

Parameters  
The list parameters, specified as key\-value pairs, to pass to the macro\.

## Return value<a name="intrinsic-function-reference-transform-returnvalue"></a>

The processed template snippet to be included in the processed stack template\.

## Examples<a name="intrinsic-function-reference-transform-examples"></a>

The following example calls the `AWS::Include` transform, specifying that the location to retrieve a template snippet from is passed in the `InputValue` parameter\.

### JSON<a name="intrinsic-function-reference-transform-example-1.json"></a>

```
1. {
2.    "Fn::Transform" : {
3.        "Name" : "AWS::Include",
4.        "Parameters" : {
5.            "Location" : { "Ref" : "InputValue" }
6.         }
7.     }
8. }
```

### YAML<a name="intrinsic-function-reference-transform-example-1.yaml"></a>

```
1. 'Fn::Transform':
2.     Name: 'AWS::Include'
3.     Parameters: {Location: {Ref: InputValue}}
```

The following example calls the `AWS::Include` transform, specifying that the location to retrieve a template snippet from is located in the `RegionMap` mapping, under the key `us-east-1` and nested key `s3Location`\.

### JSON<a name="intrinsic-function-reference-transform-example-2.json"></a>

```
1. {
2.    "Fn::Transform" : {
3.        "Name" : "AWS::Include",
4.        "Parameters" : {
5.            "Location" : {"Fn::FindInMap" : ["RegionMap", "us-east-1", "s3Location"] }
6.         }
7.     }
8. }
```

### YAML<a name="intrinsic-function-reference-transform-example-2.yaml"></a>

```
1. 'Fn::Transform':
2.     Name: 'AWS::Include'
3.     Parameters: {Location: {'Fn::FindInMap': [RegionMap, us-east-1, s3Location]}}
```

## Supported functions<a name="intrinsic-function-reference-transform-supported-functions"></a>

None\. AWS CloudFormation passes any intrinsic function calls included in `Fn::Transform` to the specified macro as literal strings\. For more information, see [AWS CloudFormation macro function interface](template-macros.md#template-macros-lambda-interface)\.