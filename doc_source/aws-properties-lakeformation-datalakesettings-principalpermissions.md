# AWS::LakeFormation::DataLakeSettings PrincipalPermissions<a name="aws-properties-lakeformation-datalakesettings-principalpermissions"></a>

Permissions granted to a principal\.

## Syntax<a name="aws-properties-lakeformation-datalakesettings-principalpermissions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-datalakesettings-principalpermissions-syntax.json"></a>

```
{
  "[Permissions](#cfn-lakeformation-datalakesettings-principalpermissions-permissions)" : [ String, ... ],
  "[Principal](#cfn-lakeformation-datalakesettings-principalpermissions-principal)" : DataLakePrincipal
}
```

### YAML<a name="aws-properties-lakeformation-datalakesettings-principalpermissions-syntax.yaml"></a>

```
  [Permissions](#cfn-lakeformation-datalakesettings-principalpermissions-permissions): 
    - String
  [Principal](#cfn-lakeformation-datalakesettings-principalpermissions-principal): 
    DataLakePrincipal
```

## Properties<a name="aws-properties-lakeformation-datalakesettings-principalpermissions-properties"></a>

`Permissions`  <a name="cfn-lakeformation-datalakesettings-principalpermissions-permissions"></a>
The permissions that are granted to the principal\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Principal`  <a name="cfn-lakeformation-datalakesettings-principalpermissions-principal"></a>
The principal who is granted permissions\.  
*Required*: Yes  
*Type*: [DataLakePrincipal](aws-properties-lakeformation-datalakesettings-datalakeprincipal.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)