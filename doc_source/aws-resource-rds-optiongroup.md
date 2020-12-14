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
      "[OptionConfigurations](#cfn-rds-optiongroup-optionconfigurations)" : [ OptionConfiguration, ... ],
      "[OptionGroupDescription](#cfn-rds-optiongroup-optiongroupdescription)" : String,
      "[Tags](#cfn-rds-optiongroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rds-optiongroup-syntax.yaml"></a>

```
Type: AWS::RDS::OptionGroup
Properties: 
  [EngineName](#cfn-rds-optiongroup-enginename): String
  [MajorEngineVersion](#cfn-rds-optiongroup-majorengineversion): String
  [OptionConfigurations](#cfn-rds-optiongroup-optionconfigurations): 
    - OptionConfiguration
  [OptionGroupDescription](#cfn-rds-optiongroup-optiongroupdescription): String
  [Tags](#cfn-rds-optiongroup-tags): 
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

## Return values<a name="aws-resource-rds-optiongroup-return-values"></a>

### Ref<a name="aws-resource-rds-optiongroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the option group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-rds-optiongroup--examples"></a>



### Creating an option group with multiple option configurations<a name="aws-resource-rds-optiongroup--examples--Creating_an_option_group_with_multiple_option_configurations"></a>

The following example creates an option group with two option configurations \(`OEM` and `APEX`\)\. For more information about these options, see [ Options for Oracle DB Instances](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Appendix.Oracle.Options.html) in the *Amazon RDS User Guide*\.

#### JSON<a name="aws-resource-rds-optiongroup--examples--Creating_an_option_group_with_multiple_option_configurations--json"></a>

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

#### YAML<a name="aws-resource-rds-optiongroup--examples--Creating_an_option_group_with_multiple_option_configurations--yaml"></a>

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

The following snippet creates an option group that specifies two option settings for the `MEMCACHED` option\. For more information about this option, see [ MySQL memcached Support](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Appendix.MySQL.Options.memcached.html) in the *Amazon RDS User Guide*\.

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

### Microsoft SQL Server Native Backup and Restore Option<a name="aws-resource-rds-optiongroup--examples--Microsoft_SQL_Server_Native_Backup_and_Restore_Option"></a>

The following snippet creates an option group that specifies the Microsoft SQL Server native backup and restore option\. For more information about this option, see [ Support for Native Backup and Restore in SQL Server](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Appendix.SQLServer.Options.BackupRestore.html) in the *Amazon RDS User Guide*\. 

#### JSON<a name="aws-resource-rds-optiongroup--examples--Microsoft_SQL_Server_Native_Backup_and_Restore_Option--json"></a>

```
{
    "myOptionGroup": {
        "Type": "AWS::RDS::OptionGroup",
        "Properties": {
            "EngineName": "sqlserver-se",
            "MajorEngineVersion": "12.00",
            "OptionGroupDescription": "SQL Server Native Backup and Restore",
            "OptionConfigurations": [
                {
                    "OptionName": "SQLSERVER_BACKUP_RESTORE",
                    "OptionSettings": [
                        {
                            "Name": "IAM_ROLE_ARN",
                            "Value": "arn:aws:iam::333333333333333:role/service-role/sqlserverrestore"
                        }
                    ]
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-rds-optiongroup--examples--Microsoft_SQL_Server_Native_Backup_and_Restore_Option--yaml"></a>

```
---                
myOptionGroup:
  Type: 'AWS::RDS::OptionGroup'
  Properties:
    EngineName: sqlserver-se
    MajorEngineVersion: '12.00'
    OptionGroupDescription: SQL Server Native Backup and Restore
    OptionConfigurations:
      - OptionName: SQLSERVER_BACKUP_RESTORE
        OptionSettings:
          - Name: IAM_ROLE_ARN
            Value: 'arn:aws:iam::333333333333333:role/service-role/sqlserverrestore'
```