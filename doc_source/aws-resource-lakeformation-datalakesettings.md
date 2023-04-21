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
      "[AllowExternalDataFiltering](#cfn-lakeformation-datalakesettings-allowexternaldatafiltering)" : Boolean,
      "[AuthorizedSessionTagValueList](#cfn-lakeformation-datalakesettings-authorizedsessiontagvaluelist)" : [ String, ... ],
      "[CreateDatabaseDefaultPermissions](#cfn-lakeformation-datalakesettings-createdatabasedefaultpermissions)" : CreateDatabaseDefaultPermissions,
      "[CreateTableDefaultPermissions](#cfn-lakeformation-datalakesettings-createtabledefaultpermissions)" : CreateTableDefaultPermissions,
      "[ExternalDataFilteringAllowList](#cfn-lakeformation-datalakesettings-externaldatafilteringallowlist)" : ExternalDataFilteringAllowList,
      "[Parameters](#cfn-lakeformation-datalakesettings-parameters)" : Json,
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
  [AllowExternalDataFiltering](#cfn-lakeformation-datalakesettings-allowexternaldatafiltering): Boolean
  [AuthorizedSessionTagValueList](#cfn-lakeformation-datalakesettings-authorizedsessiontagvaluelist): 
    - String
  [CreateDatabaseDefaultPermissions](#cfn-lakeformation-datalakesettings-createdatabasedefaultpermissions): 
    CreateDatabaseDefaultPermissions
  [CreateTableDefaultPermissions](#cfn-lakeformation-datalakesettings-createtabledefaultpermissions): 
    CreateTableDefaultPermissions
  [ExternalDataFilteringAllowList](#cfn-lakeformation-datalakesettings-externaldatafilteringallowlist): 
    ExternalDataFilteringAllowList
  [Parameters](#cfn-lakeformation-datalakesettings-parameters): Json
  [TrustedResourceOwners](#cfn-lakeformation-datalakesettings-trustedresourceowners): 
    - String
```

## Properties<a name="aws-resource-lakeformation-datalakesettings-properties"></a>

`Admins`  <a name="cfn-lakeformation-datalakesettings-admins"></a>
A list of AWS Lake Formation principals\.  
*Required*: No  
*Type*: [Admins](aws-properties-lakeformation-datalakesettings-admins.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowExternalDataFiltering`  <a name="cfn-lakeformation-datalakesettings-allowexternaldatafiltering"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizedSessionTagValueList`  <a name="cfn-lakeformation-datalakesettings-authorizedsessiontagvaluelist"></a>
Property description not available\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreateDatabaseDefaultPermissions`  <a name="cfn-lakeformation-datalakesettings-createdatabasedefaultpermissions"></a>
Property description not available\.  
*Required*: No  
*Type*: [CreateDatabaseDefaultPermissions](aws-properties-lakeformation-datalakesettings-createdatabasedefaultpermissions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreateTableDefaultPermissions`  <a name="cfn-lakeformation-datalakesettings-createtabledefaultpermissions"></a>
Property description not available\.  
*Required*: No  
*Type*: [CreateTableDefaultPermissions](aws-properties-lakeformation-datalakesettings-createtabledefaultpermissions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExternalDataFilteringAllowList`  <a name="cfn-lakeformation-datalakesettings-externaldatafilteringallowlist"></a>
Property description not available\.  
*Required*: No  
*Type*: [ExternalDataFilteringAllowList](aws-properties-lakeformation-datalakesettings-externaldatafilteringallowlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-lakeformation-datalakesettings-parameters"></a>
Property description not available\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustedResourceOwners`  <a name="cfn-lakeformation-datalakesettings-trustedresourceowners"></a>
 An array of UTF\-8 strings\.  
A list of the resource\-owning account IDs that the caller's account can use to share their user access details \(user ARNs\)\. The user ARNs can be logged in the resource owner's CloudTrail log\. You may want to specify this property when you are in a high\-trust boundary, such as the same team or company\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)