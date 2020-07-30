# AWS::LakeFormation::DataLakeSettings Admins<a name="aws-properties-lakeformation-datalakesettings-admins"></a>

A list of AWS Lake Formation principals\.

## Syntax<a name="aws-resource-lakeformation-datalakesettings-admins-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-datalakesettings-admins-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::DataLakeSettings",
  "Properties" : {
      "[Admins](#cfn-lakeformation-datalakesettings-admins)" : {
          DataLakePrincipalIdentifier (#cfn-lakeformation-datalakesettings-datalakeprincipal-datalakeprincipalidentifier) : String
      }
   }
}
```

### YAML<a name="aws-resource-lakeformation-datalakesettings-admins-syntax.yaml"></a>

```
Type: AWS::LakeFormation::DataLakeSettings
Properties: 
  [Admins](#cfn-lakeformation-datalakesettings-admins): 
    - DataLakePrincipalIdentifier (#cfn-lakeformation-datalakesettings-datalakeprincipal-datalakeprincipalidentifier) : String
```

## Properties<a name="aws-resource-lakeformation-datalakesettings-admins-properties"></a>

`DataLakePrincipalIdentifier`  <a name="cfn-lakeformation-datalakesettings-datalakeprincipal-datalakeprincipalidentifier"></a>
An identifier for the AWS Lake Formation principal\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
