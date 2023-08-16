# `Fn::ForEach` in the `Conditions` section<a name="intrinsic-function-reference-foreach-example-conditions"></a>

These examples demonstrate using the `Fn::ForEach` intrinsic function in the [Conditions](conditions-section-structure.md) section\.

**Topics**
+ [Replicate a single condition](#intrinsic-function-reference-foreach-example-replicated-single-condition)

## Replicate a single condition<a name="intrinsic-function-reference-foreach-example-replicated-single-condition"></a>

This example uses the `Fn::ForEach` intrinsic function in the [Conditions](conditions-section-structure.md) section to replicate multiple similar conditions with different properties\.

### JSON<a name="intrinsic-function-reference-foreach-example-conditions.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Transform": "AWS::LanguageExtensions",
    "Parameters": {
        "ParamA": {
            "Type": "String",
            "AllowedValues": [
                "true",
                "false"
            ]
        },
        "ParamB": {
            "Type": "String",
            "AllowedValues": [
                "true",
                "false"
            ]
        },
        "ParamC": {
            "Type": "String",
            "AllowedValues": [
                "true",
                "false"
            ]
        },
        "ParamD": {
            "Type": "String",
            "AllowedValues": [
                "true",
                "false"
            ]
        }
    },
    "Conditions": {
        "Fn::ForEach::CheckTrue": [
            "Identifier",
            ["A", "B", "C", "D"],
            {
                "IsParam${Identifier}Enabled": {
                    "Fn::Equals": [
                        {"Ref": {"Fn::Sub": "Param${Identifier}"}},
                        "true"
                    ]
                }
            }
        ]
    },
    "Resources": {
        "WaitConditionHandle": {
            "Type": "AWS::CloudFormation::WaitConditionHandle"
        }
    }
}
```

### YAML<a name="intrinsic-function-reference-foreach-example-conditions.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Parameters:
  ParamA:
    Type: String
    AllowedValues:
      - 'true'
      - 'false'
  ParamB:
    Type: String
    AllowedValues:
      - 'true'
      - 'false'
  ParamC:
    Type: String
    AllowedValues:
      - 'true'
      - 'false'
  ParamD:
    Type: String
    AllowedValues:
      - 'true'
      - 'false'
Conditions:
  'Fn::ForEach::CheckTrue':
    - Identifier
    - [A, B, C, D]
    - 'IsParam${Identifier}Enabled': !Equals 
        - !Ref 
          'Fn::Sub': 'Param${Identifier}'
        - 'true'
Resources:
  WaitConditionHandle:
    Type: 'AWS::CloudFormation::WaitConditionHandle'
```

The transformed template will be equivalent to the following template:

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  ParamA:
    Type: String
    AllowedValues:
      - 'true'
      - 'false'
  ParamB:
    Type: String
    AllowedValues:
      - 'true'
      - 'false'
  ParamC:
    Type: String
    AllowedValues:
      - 'true'
      - 'false'
  ParamD:
    Type: String
    AllowedValues:
      - 'true'
      - 'false'
Conditions:
  IsParamAEnabled: !Equals 
    - !Ref ParamA
    - 'true'
  IsParamBEnabled: !Equals 
    - !Ref ParamB
    - 'true'
  IsParamCEnabled: !Equals 
    - !Ref ParamC
    - 'true'
  IsParamDEnabled: !Equals 
    - !Ref ParamD
    - 'true'
Resources:
  WaitConditionHandle:
    Type: 'AWS::CloudFormation::WaitConditionHandle'
```