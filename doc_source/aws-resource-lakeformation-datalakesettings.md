# AWS::LakeFormation::DataLakeSettings<a name="aws-resource-lakeformation-datalakesettings"></a>

The `AWS::LakeFormation::DataLakeSettings` resource is an AWS Lake Formation resource type that manages the data lake settings for your account\. Note that the CloudFormation template only supports updating the `Admins` list\. It does not support updating the [CreateDatabaseDefaultPermissions](https://docs.aws.amazon.com/lake-formation/latest/dg/aws-lake-formation-api-aws-lake-formation-api-settings.html#aws-lake-formation-api-aws-lake-formation-api-settings-DataLakeSettings) or [CreateTableDefaultPermissions](https://docs.aws.amazon.com/lake-formation/latest/dg/aws-lake-formation-api-aws-lake-formation-api-settings.html#aws-lake-formation-api-aws-lake-formation-api-settings-DataLakeSettings)\. Those permissions can only be edited in the DataLakeSettings resource via the API\.

## Syntax<a name="aws-resource-lakeformation-datalakesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-datalakesettings-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::DataLakeSettings",
  "Properties" : {
      "[Admins](#cfn-lakeformation-datalakesettings-admins)" : Admins,
      "[TrustedResourceOwners](#cfn-lakeformation-datalakesettings-trustedresourceowners)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-lakeformation-datalakesettings-syntax.yaml"></a>

```
Type: AWS::LakeFormation::DataLakeSettings
Properties: 
  [Admins](#cfn-lakeformation-datalakesettings-admins): 
    Admins
  [TrustedResourceOwners](#cfn-lakeformation-datalakesettings-trustedresourceowners): 
    - String
```

## Properties<a name="aws-resource-lakeformation-datalakesettings-properties"></a>

`Admins`  <a name="cfn-lakeformation-datalakesettings-admins"></a>
A list of AWS Lake Formation principals\.  
*Required*: No  
*Type*: [Admins](aws-properties-lakeformation-datalakesettings-admins.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustedResourceOwners`  <a name="cfn-lakeformation-datalakesettings-trustedresourceowners"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)