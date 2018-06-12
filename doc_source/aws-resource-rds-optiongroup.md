# AWS::RDS::OptionGroup<a name="aws-resource-rds-optiongroup"></a>

Use the `AWS::RDS::OptionGroup` resource to create an option group that can make managing data and databases easier\. For more information about option groups, see [Working with Option Groups](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithOptionGroups.html) in the *Amazon Relational Database Service User Guide*\.

**Topics**
+ [Syntax](#aws-resource-rds-optiongroup-syntax)
+ [Properties](#w3ab2c21c10d984b9)
+ [Return Values](#w3ab2c21c10d984c11)
+ [Examples](#w3ab2c21c10d984c13)

## Syntax<a name="aws-resource-rds-optiongroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-optiongroup-syntax.json"></a>

```
{
   "Type" : "AWS::RDS::OptionGroup",
   "Properties" : {
      "[EngineName](#cfn-rds-optiongroup-enginename)" : String,
      "[MajorEngineVersion](#cfn-rds-optiongroup-majorengineversion)" : String,
      "[OptionGroupDescription](#cfn-rds-optiongroup-optiongroupdescription)" : String,
      "[OptionConfigurations](#cfn-rds-optiongroup-optionconfigurations)" : [ OptionConfiguration, ... ],
      "[Tags](#cfn-rds-optiongroup-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-rds-optiongroup-syntax.yaml"></a>

```
Type: "AWS::RDS::OptionGroup"
Properties: 
  [EngineName](#cfn-rds-optiongroup-enginename): String
  [MajorEngineVersion](#cfn-rds-optiongroup-majorengineversion): String
  [OptionGroupDescription](#cfn-rds-optiongroup-optiongroupdescription): String
  [OptionConfigurations](#cfn-rds-optiongroup-optionconfigurations):
    - OptionConfiguration
  [Tags](#cfn-rds-optiongroup-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d984b9"></a>

`EngineName`  <a name="cfn-rds-optiongroup-enginename"></a>
The name of the database engine that this option group is associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`MajorEngineVersion`  <a name="cfn-rds-optiongroup-majorengineversion"></a>
The major version number of the database engine that this option group is associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`OptionGroupDescription`  <a name="cfn-rds-optiongroup-optiongroupdescription"></a>
A description of the option group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`OptionConfigurations`  <a name="cfn-rds-optiongroup-optionconfigurations"></a>
The configurations for this option group\.  
*Required*: Yes  
*Type*: List of [Amazon RDS OptionGroup OptionConfiguration](aws-properties-rds-optiongroup-optionconfigurations.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-rds-optiongroup-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this option group\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d984c11"></a>

### Ref<a name="w3ab2c21c10d984c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myOptionGroup" }
```

For the `myOptionGroup` resource, `Ref` returns the name of the option group\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d984c13"></a>

### Multiple Option Configurations<a name="w3ab2c21c10d984c13b2"></a>

The following snippet creates an option group with two option configurations \(`OEM` and `APEX`\):

#### JSON<a name="aws-resource-rds-optiongroup-example1.json"></a>

```
"OracleOptionGroup": {
  "Type": "AWS::RDS::OptionGroup",
  "Properties": {
    "EngineName": "oracle-ee",
    "MajorEngineVersion": "12.1",
    "OptionGroupDescription": "A test option group",
    "OptionConfigurations":[
      {
        "OptionName": "OEM",
        "DBSecurityGroupMemberships": ["default"],
        "Port": "5500"
      },
      {
        "OptionName": "APEX"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-rds-optiongroup-example1.yaml"></a>

```
OracleOptionGroup: 
  Type: "AWS::RDS::OptionGroup"
  Properties: 
    EngineName: "oracle-ee"
    MajorEngineVersion: "12.1"
    OptionGroupDescription: "A test option group"
    OptionConfigurations: 
      - 
        OptionName: "OEM"
        DBSecurityGroupMemberships: 
          - "default"
        Port: "5500"
      - 
        OptionName: "APEX"
```

### Multiple Settings<a name="w3ab2c21c10d984c13b4"></a>

The following snippet creates an option group that specifies two option settings for the `MEMCACHED` option:

#### JSON<a name="aws-resource-rds-optiongroup-example2.json"></a>

```
"SQLOptionGroup": {
  "Type": "AWS::RDS::OptionGroup",
  "Properties": {
    "EngineName": "mysql",
    "MajorEngineVersion": "5.6",
    "OptionGroupDescription": "A test option group",
    "OptionConfigurations":[
      {
        "OptionName": "MEMCACHED",
        "VpcSecurityGroupMemberships": ["sg-a1238db7"],
        "Port": "1234",
        "OptionSettings": [
          {"Name": "CHUNK_SIZE", "Value": "32"},
          {"Name": "BINDING_PROTOCOL", "Value": "ascii"}
        ]
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-rds-optiongroup-example2.yaml"></a>

```
SQLOptionGroup:
  Type: 'AWS::RDS::OptionGroup'
  Properties:
    EngineName: mysql
    MajorEngineVersion: '5.6'
    OptionGroupDescription: A test option group
    OptionConfigurations:
      - OptionName: MEMCACHED
        VpcSecurityGroupMemberships:
          - sg-a1238db7
        Port: '1234'
        OptionSettings:
          - Name: CHUNK_SIZE
            Value: '32'
          - Name: BINDING_PROTOCOL
            Value: ascii
```