# AWS::RDS::OptionGroup<a name="aws-resource-rds-optiongroup"></a>

The `AWS::RDS::OptionGroup` resource creates an option group, to enable and configure features that are specific to a particular DB engine\.

## Syntax<a name="aws-resource-rds-optiongroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-optiongroup-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::OptionGroup",
  "Properties" : {
      "[EngineName](#cfn-rds-optiongroup-enginename)" : String,
      "[MajorEngineVersion](#cfn-rds-optiongroup-majorengineversion)" : String,
      "[OptionConfigurations](#cfn-rds-optiongroup-optionconfigurations)" : [ [OptionConfiguration](aws-properties-rds-optiongroup-optionconfigurations.md), ... ],
      "[OptionGroupDescription](#cfn-rds-optiongroup-optiongroupdescription)" : String,
      "[Tags](#cfn-rds-optiongroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rds-optiongroup-syntax.yaml"></a>

```
Type: AWS::RDS::OptionGroup
Properties : 
﻿  [EngineName](#cfn-rds-optiongroup-enginename) : String
﻿  [MajorEngineVersion](#cfn-rds-optiongroup-majorengineversion) : String
﻿  [OptionConfigurations](#cfn-rds-optiongroup-optionconfigurations) : 
    - [OptionConfiguration](aws-properties-rds-optiongroup-optionconfigurations.md)
﻿  [OptionGroupDescription](#cfn-rds-optiongroup-optiongroupdescription) : String
﻿  [Tags](#cfn-rds-optiongroup-tags) : 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-rds-optiongroup-properties"></a>

`EngineName`  <a name="cfn-rds-optiongroup-enginename"></a>
Specifies the name of the engine that this option group should be associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MajorEngineVersion`  <a name="cfn-rds-optiongroup-majorengineversion"></a>
Specifies the major version of the engine that this option group should be associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OptionConfigurations`  <a name="cfn-rds-optiongroup-optionconfigurations"></a>
A list of all available options  
*Required*: Yes  
*Type*: List of [OptionConfiguration](aws-properties-rds-optiongroup-optionconfigurations.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OptionGroupDescription`  <a name="cfn-rds-optiongroup-optiongroupdescription"></a>
The description of the option group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-rds-optiongroup-tags"></a>
Tags to assign to the option group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-rds-optiongroup-return-values"></a>

### Ref<a name="aws-resource-rds-optiongroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the option group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-rds-optiongroup--examples"></a>

### Multiple Option Configurations<a name="aws-resource-rds-optiongroup--examples--Multiple_Option_Configurations"></a>

The following example creates an option group with two option configurations \(`OEM` and `APEX`\): 

#### JSON<a name="aws-resource-rds-optiongroup--examples--Multiple_Option_Configurations--json"></a>

```
{
    "OracleOptionGroup": {
        "Type": "AWS::RDS::OptionGroup",
        "Properties": {
            "EngineName": "oracle-ee",
            "MajorEngineVersion": "12.1",
            "OptionGroupDescription": "A test option group",
            "OptionConfigurations": [
                {
                    "OptionName": "OEM",
                    "DBSecurityGroupMemberships": [
                        "default"
                    ],
                    "Port": "5500"
                },
                {
                    "OptionName": "APEX"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-rds-optiongroup--examples--Multiple_Option_Configurations--yaml"></a>

```
--- 
OracleOptionGroup: 
  Properties: 
    EngineName: oracle-ee
    MajorEngineVersion: "12.1"
    OptionConfigurations: 
      - 
        DBSecurityGroupMemberships: 
          - default
        OptionName: OEM
        Port: "5500"
      - 
        OptionName: APEX
    OptionGroupDescription: "A test option group"
  Type: "AWS::RDS::OptionGroup"
```

### Multiple Settings<a name="aws-resource-rds-optiongroup--examples--Multiple_Settings"></a>

The following snippet creates an option group that specifies two option settings for the `MEMCACHED` option: 

#### JSON<a name="aws-resource-rds-optiongroup--examples--Multiple_Settings--json"></a>

```
{
    "SQLOptionGroup": {
        "Type": "AWS::RDS::OptionGroup",
        "Properties": {
            "EngineName": "mysql",
            "MajorEngineVersion": "5.6",
            "OptionGroupDescription": "A test option group",
            "OptionConfigurations": [
                {
                    "OptionName": "MEMCACHED",
                    "VpcSecurityGroupMemberships": [
                        "sg-a1238db7"
                    ],
                    "Port": "1234",
                    "OptionSettings": [
                        {
                            "Name": "CHUNK_SIZE",
                            "Value": "32"
                        },
                        {
                            "Name": "BINDING_PROTOCOL",
                            "Value": "ascii"
                        }
                    ]
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-rds-optiongroup--examples--Multiple_Settings--yaml"></a>

```
--- 
SQLOptionGroup: 
  Properties: 
    EngineName: mysql
    MajorEngineVersion: "5.6"
    OptionConfigurations: 
      - 
        OptionName: MEMCACHED
        OptionSettings: 
          - 
            Name: CHUNK_SIZE
            Value: "32"
          - 
            Name: BINDING_PROTOCOL
            Value: ascii
        Port: "1234"
        VpcSecurityGroupMemberships: 
          - sg-a1238db7
    OptionGroupDescription: "A test option group"
  Type: "AWS::RDS::OptionGroup"
```