# AWS::LakeFormation::DataLakeSettings Admins<a name="aws-properties-lakeformation-datalakesettings-admins"></a>

A list of AWS Lake Formation principals\.

## Syntax<a name="aws-resource-lakeformation-datalakesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-datalakesettings-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::DataLakeSettings",
  "Properties" : {
      "[DataLakePrincipalIdentifier](aws-properties-lakeformation-datalakesettings-datalakeprincipal.md)" : String)
    }
}
```

### YAML<a name="aws-resource-lakeformation-datalakesettings-syntax.yaml"></a>

```
Type: AWS::LakeFormation::DataLakeSettings
Properties: 
  [Admins](#cfn-lakeformation-datalakesettings-admins): 
    [DataLakePrincipalIdentifier](aws-properties-lakeformation-datalakesettings-datalakeprincipal.md): String
```
