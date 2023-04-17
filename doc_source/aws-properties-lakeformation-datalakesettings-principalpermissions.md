# AWS::LakeFormation::DataLakeSettings PrincipalPermissions<a name="aws-properties-lakeformation-datalakesettings-principalpermissions"></a>

Permissions granted to a principal\.

## Syntax<a name="aws-properties-lakeformation-datalakesettings-principalpermissions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-datalakesettings-principalpermissions-syntax.json"></a>

```
{
  "[Permissions](#cfn-lakeformation-datalakesettings-principalpermissions-permissions)" : Permissions,
  "[Principal](#cfn-lakeformation-datalakesettings-principalpermissions-principal)" : DataLakePrincipal
}
```

### YAML<a name="aws-properties-lakeformation-datalakesettings-principalpermissions-syntax.yaml"></a>

```
  [Permissions](#cfn-lakeformation-datalakesettings-principalpermissions-permissions): 
    Permissions
  [Principal](#cfn-lakeformation-datalakesettings-principalpermissions-principal): 
    DataLakePrincipal
```

## Properties<a name="aws-properties-lakeformation-datalakesettings-principalpermissions-properties"></a>

`Permissions`  <a name="cfn-lakeformation-datalakesettings-principalpermissions-permissions"></a>
The permissions that are granted to the principal\.  
*Required*: No  
*Type*: [Permissions](aws-properties-lakeformation-datalakesettings-permissions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Principal`  <a name="cfn-lakeformation-datalakesettings-principalpermissions-principal"></a>
The principal who is granted permissions\.  
*Required*: No  
*Type*: [DataLakePrincipal](aws-properties-lakeformation-datalakesettings-datalakeprincipal.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)