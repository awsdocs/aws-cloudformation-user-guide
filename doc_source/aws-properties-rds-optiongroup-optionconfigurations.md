# Amazon Relational Database Service OptionGroup OptionConfiguration<a name="aws-properties-rds-optiongroup-optionconfigurations"></a>

Use the `OptionConfigurations` property to configure an option and its settings for an [AWS::RDS::OptionGroup](aws-resource-rds-optiongroup.md) resource\.

## Syntax<a name="w3ab2c21c14e1424b5"></a>

### JSON<a name="aws-properties-rds-optiongroup-optionconfigurations-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfigurations-dbsecuritygroupmemberships)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfigurations-optionname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfigurations-optionsettings)" : [ OptionSetting, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfiguration-optionversion)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfigurations-port)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfigurations-vpcsecuritygroupmemberships)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-rds-optiongroup-optionconfigurations-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfigurations-dbsecuritygroupmemberships):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfigurations-optionname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfigurations-optionsettings):
  - OptionSetting
[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfiguration-optionversion): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfigurations-port): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-optiongroup-optionconfigurations-vpcsecuritygroupmemberships):
  - String
```

## Properties<a name="w3ab2c21c14e1424b7"></a>

`DBSecurityGroupMemberships`  
A list of database security group names for this option\. If the option requires access to a port, the security groups must allow access to that port\. If you specify this property, don't specify the `VPCSecurityGroupMemberships` property\.  
*Required: *No  
*Type*: List of String values

`OptionName`  
The name of the option\. For more information about options, see [Working with Option Groups](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithOptionGroups.html) in the *Amazon Relational Database Service User Guide*\.  
*Required: *Yes  
*Type*: String

`OptionSettings`  
The settings for this option\.  
*Required: *No  
*Type*: List of [Amazon RDS OptionGroup OptionSetting](aws-properties-rds-optiongroup-optionconfigurations-optionsettings.md)

`OptionVersion`  
The version for the option\.  
*Required: *No  
*Type*: String

`Port`  
The port number that this option uses\.  
*Required: *No  
*Type*: Integer

`VpcSecurityGroupMemberships`  
A list of VPC security group IDs for this option\. If the option requires access to a port, the security groups must allow access to that port\. If you specify this property, don't specify the `DBSecurityGroupMemberships` property\.  
*Required: *No  
*Type*: List of String values

## Examples<a name="aws-properties-rds-optiongroup-optionconfiguration-examples"></a>

### <a name="aws-properties-rds-optiongroup-optionconfiguration-example1"></a>

The following example template uses `OptionName` and `OptionVersion` parameters when creating an `AWS::RDS::OptionGroup` resource\.

#### JSON<a name="aws-properties-rds-optiongroup-optionconfiguration-example1.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description":"APEX has a dependency on XMLDB, so, there must be at least one XMLDB when there is a APEX",
  "Parameters" : {
    "OptionName" : {
      "Type" : "String"
    },
    "OptionVersion" : {
      "Type" : "String"
    }
  },
  "Resources": {
    "myOptionGroup": {
      "Type": "AWS::RDS::OptionGroup",
      "Properties": {
        "EngineName": "oracle-ee",
        "MajorEngineVersion": "11.2",
        "OptionGroupDescription": "testing creating optionGroup with APEX version",
        "OptionConfigurations":[
          {
            "OptionName": "XMLDB"
          },
          {
            "OptionName": {"Ref" : "OptionName"},
            "OptionVersion" : {"Ref" : "OptionVersion"}
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-properties-rds-optiongroup-optionconfiguration-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: >-
  APEX has a dependency on XMLDB, so, there must be at least one XMLDB when
  there is a APEX
Parameters:
  OptionName:
    Type: String
  OptionVersion:
    Type: String
Resources:
  myOptionGroup:
    Type: 'AWS::RDS::OptionGroup'
    Properties:
      EngineName: oracle-ee
      MajorEngineVersion: '11.2'
      OptionGroupDescription: testing creating optionGroup with APEX version
      OptionConfigurations:
        - OptionName: XMLDB
        - OptionName: !Ref OptionName
          OptionVersion: !Ref OptionVersion
```

## See Also<a name="aws-properties-rds-optiongroup-optionconfiguration-seealso"></a>

+ [OptionConfiguration](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_OptionConfiguration.html) data type in the *Amazon Relational Database Service API Reference*

+ [Working with Option Groups](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithOptionGroups.html) in the *Amazon Relational Database Service User Guide*