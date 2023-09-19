# AWS::LakeFormation::DataLakeSettings<a name="aws-resource-lakeformation-datalakesettings"></a>

The `AWS::LakeFormation::DataLakeSettings` resource is an AWS Lake Formation resource type that manages the data lake settings for your account\. 

## Syntax<a name="aws-resource-lakeformation-datalakesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-datalakesettings-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::DataLakeSettings",
  "Properties" : {
      "[Admins](#cfn-lakeformation-datalakesettings-admins)" : Admins,
      "[AllowExternalDataFiltering](#cfn-lakeformation-datalakesettings-allowexternaldatafiltering)" : Boolean,
      "[AllowFullTableExternalDataAccess](#cfn-lakeformation-datalakesettings-allowfulltableexternaldataaccess)" : Boolean,
      "[AuthorizedSessionTagValueList](#cfn-lakeformation-datalakesettings-authorizedsessiontagvaluelist)" : [ String, ... ],
      "[CreateDatabaseDefaultPermissions](#cfn-lakeformation-datalakesettings-createdatabasedefaultpermissions)" : CreateDatabaseDefaultPermissions,
      "[CreateTableDefaultPermissions](#cfn-lakeformation-datalakesettings-createtabledefaultpermissions)" : CreateTableDefaultPermissions,
      "[ExternalDataFilteringAllowList](#cfn-lakeformation-datalakesettings-externaldatafilteringallowlist)" : ExternalDataFilteringAllowList,
      "[MutationType](#cfn-lakeformation-datalakesettings-mutationtype)" : String,
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
  [AllowFullTableExternalDataAccess](#cfn-lakeformation-datalakesettings-allowfulltableexternaldataaccess): Boolean
  [AuthorizedSessionTagValueList](#cfn-lakeformation-datalakesettings-authorizedsessiontagvaluelist): 
    - String
  [CreateDatabaseDefaultPermissions](#cfn-lakeformation-datalakesettings-createdatabasedefaultpermissions): 
    CreateDatabaseDefaultPermissions
  [CreateTableDefaultPermissions](#cfn-lakeformation-datalakesettings-createtabledefaultpermissions): 
    CreateTableDefaultPermissions
  [ExternalDataFilteringAllowList](#cfn-lakeformation-datalakesettings-externaldatafilteringallowlist): 
    ExternalDataFilteringAllowList
  [MutationType](#cfn-lakeformation-datalakesettings-mutationtype): String
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
Whether to allow Amazon EMR clusters or other third\-party query engines to access data managed by Lake Formation\.   
If set to true, you allow Amazon EMR clusters or other third\-party engines to access data in Amazon S3 locations that are registered with Lake Formation\.  
If false or null, no third\-party query engines will be able to access data in Amazon S3 locations that are registered with Lake Formation\.  
For more information, see [External data filtering setting](https://docs.aws.amazon.com/lake-formation/latest/dg/initial-LF-setup.html#external-data-filter)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowFullTableExternalDataAccess`  <a name="cfn-lakeformation-datalakesettings-allowfulltableexternaldataaccess"></a>
 Specifies whether query engines and applications can get credentials without IAM session tags if the user has full table access\. It provides query engines and applications performance benefits as well as simplifies data access\. Amazon EMR on Amazon EC2 is able to leverage this setting\.   
For more information, see [https://docs.aws.amazon.com/lake-formation/latest/dg/using-cred-vending.html](https://docs.aws.amazon.com/lake-formation/latest/dg/using-cred-vending.html)  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizedSessionTagValueList`  <a name="cfn-lakeformation-datalakesettings-authorizedsessiontagvaluelist"></a>
Lake Formation relies on a privileged process secured by Amazon EMR or the third party integrator to tag the user's role while assuming it\. Lake Formation will publish the acceptable key\-value pair, for example key = "LakeFormationTrustedCaller" and value = "TRUE" and the third party integrator must properly tag the temporary security credentials that will be used to call Lake Formation's administrative API operations\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreateDatabaseDefaultPermissions`  <a name="cfn-lakeformation-datalakesettings-createdatabasedefaultpermissions"></a>
Specifies whether access control on a newly created database is managed by Lake Formation permissions or exclusively by IAM permissions\.  
A null value indicates that the access is controlled by Lake Formation permissions\. `ALL` permissions assigned to `IAM_ALLOWED_PRINCIPALS` group indicates that the user's IAM permissions determine the access to the database\. This is referred to as the setting "Use only IAM access control," and is to support backward compatibility with the AWS Glue permission model implemented by IAM permissions\.  
The only permitted values are an empty array or an array that contains a single JSON object that grants `ALL` to `IAM_ALLOWED_PRINCIPALS`\.  
For more information, see [Changing the default security settings for your data lake](https://docs.aws.amazon.com/lake-formation/latest/dg/change-settings.html)\.  
*Required*: No  
*Type*: [CreateDatabaseDefaultPermissions](aws-properties-lakeformation-datalakesettings-createdatabasedefaultpermissions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreateTableDefaultPermissions`  <a name="cfn-lakeformation-datalakesettings-createtabledefaultpermissions"></a>
Specifies whether access control on a newly created table is managed by Lake Formation permissions or exclusively by IAM permissions\.  
A null value indicates that the access is controlled by Lake Formation permissions\. `ALL` permissions assigned to `IAM_ALLOWED_PRINCIPALS` group indicate that the user's IAM permissions determine the access to the table\. This is referred to as the setting "Use only IAM access control," and is to support the backward compatibility with the AWS Glue permission model implemented by IAM permissions\.  
The only permitted values are an empty array or an array that contains a single JSON object that grants `ALL` permissions to `IAM_ALLOWED_PRINCIPALS`\.  
For more information, see [Changing the default security settings for your data lake](https://docs.aws.amazon.com/lake-formation/latest/dg/change-settings.html)\.  
*Required*: No  
*Type*: [CreateTableDefaultPermissions](aws-properties-lakeformation-datalakesettings-createtabledefaultpermissions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExternalDataFilteringAllowList`  <a name="cfn-lakeformation-datalakesettings-externaldatafilteringallowlist"></a>
A list of the account IDs of AWS accounts with Amazon EMR clusters or third\-party engines that are allwed to perform data filtering\.  
*Required*: No  
*Type*: [ExternalDataFilteringAllowList](aws-properties-lakeformation-datalakesettings-externaldatafilteringallowlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MutationType`  <a name="cfn-lakeformation-datalakesettings-mutationtype"></a>
 Specifies whether the data lake settings are updated by adding new values to the current settings \(`append`\) or by replacing the current settings with new settings \( `Replace`\)\.   
If you choose `Replace`, your current data lake settings will be replaced with the new values in your template\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-lakeformation-datalakesettings-parameters"></a>
A key\-value map that provides an additional configuration on your data lake\. `CrossAccountVersion` is the key you can configure in the `Parameters` field\. Accepted values for the `CrossAccountVersion` key are 1, 2, and 3\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustedResourceOwners`  <a name="cfn-lakeformation-datalakesettings-trustedresourceowners"></a>
 An array of UTF\-8 strings\.  
A list of the resource\-owning account IDs that the caller's account can use to share their user access details \(user ARNs\)\. The user ARNs can be logged in the resource owner's CloudTrail log\. You may want to specify this property when you are in a high\-trust boundary, such as the same team or company\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-lakeformation-datalakesettings--examples"></a>

### Input format for DataLakeSettings with AllowExternalDataFiltering set to false<a name="aws-resource-lakeformation-datalakesettings--examples--Input_format_for_DataLakeSettings_with_AllowExternalDataFiltering_set_to_false"></a>

In this example the value of `AllowExternalDataFiltering` is set to `false`\. When `AllowExternalDataFiltering` is set to false, the value for `ExternalDataFilteringAllowList` property is not applicable\. This example does not include `CreateDatabaseDefaultPermissions` and `CreateTableDefaultPermissions` properties\. Null values for these properties indicate that the permissions are controlled by Lake Formation permissions\. When these values are provided, you need to assign `ALL` permissions to `IAM_ALLOWED_PRINCIPALS` parameter\. 

#### <a name="aws-resource-lakeformation-datalakesettings--examples--Input_format_for_DataLakeSettings_with_AllowExternalDataFiltering_set_to_false--Json"></a>

```
{
  "Description": "DataLakeSettings_Example1",
  "Resources": {
    "DataLakeSettings": {
      "Type": "AWS::LakeFormation::DataLakeSettings",
      "Properties": {
        "Admins": [
          {
            "DataLakePrincipalIdentifier": "arn:aws:iam::012345678910:role/sample-role1"
          },
          {
            "DataLakePrincipalIdentifier": "arn:aws:iam::012345678910:role/sample-role2"
          }
        ],
        "AllowFullTableExternalDataAccess": false,
        "AllowExternalDataFiltering": false,
        "AuthorizedSessionTagValueList": [
          "sample_val1",
          "sample_val2"
        ],
        "MutationType": "REPLACE"
        "Parameters": {
          "CROSS_ACCOUNT_VERSION": "2"
        },
        "TrustedResourceOwners": [
          "012345678910",
          "109876543210"
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-lakeformation-datalakesettings--examples--Input_format_for_DataLakeSettings_with_AllowExternalDataFiltering_set_to_false--yaml"></a>

```
Description: "DataLakeSettings_Example1"
Resources:
  DataLakeSettings:
    Type: "AWS::LakeFormation::DataLakeSettings"
    Properties:
      Admins:
        - DataLakePrincipalIdentifier: "arn:aws:iam::012345678910:role/sample-role1"
        - DataLakePrincipalIdentifier: "arn:aws:iam::012345678910:role/sample-role2"
      AllowFullTableExternalDataAccess: false
      AllowExternalDataFiltering: false
      AuthorizedSessionTagValueList:
        - "sample_val1"
        - "sample_val2"
      MutationType": "REPLACE"
      Parameters:
        "CROSS_ACCOUNT_VERSION": "2"
      TrustedResourceOwners:
        - "012345678910"
        - "109876543210"
```

### Input format for DataLakeSettings with AllowExternalDataFiltering set to true<a name="aws-resource-lakeformation-datalakesettings--examples--Input_format_for_DataLakeSettings_with_AllowExternalDataFiltering_set_to_true"></a>

In this example, the `AllowExternalDataFiltering` property is set to true, and includes a value for the `ExternalDataFilteringAllowList` property\. Also, in this example, `ALL` permissions is granted to `IAM_ALLOWED_PRINCIPALS`\. If `AllowExternalDataFiltering` is set to true, the `ExternalDataFilteringAllowList` property must include at least one account id\. 

#### JSON<a name="aws-resource-lakeformation-datalakesettings--examples--Input_format_for_DataLakeSettings_with_AllowExternalDataFiltering_set_to_true--json"></a>

```
{
  "Description": "DataLakeSettings_Example2",
  "Resources": {
    "DataLakeSettings": {
      "Type": "AWS::LakeFormation::DataLakeSettings",
      "Properties": {
        "Admins": [
          {
            "DataLakePrincipalIdentifier": "arn:aws:iam::012345678910:role/sample-role1"
          },
          {
            "DataLakePrincipalIdentifier": "arn:aws:iam::012345678910:role/sample-role2"
          }
        ],
        "AllowFullTableExternalDataAccess": true
        "AllowExternalDataFiltering": true,
        "AuthorizedSessionTagValueList": [
          "sample_val1",
          "sample_val2"
        ],
        "CreateDatabaseDefaultPermissions": [
          {
            "Principal": {
              "DataLakePrincipalIdentifier": "IAM_ALLOWED_PRINCIPALS"
            },
            "Permissions": [
              "ALL"
            ]
          }
        ],
        "CreateTableDefaultPermissions": [
          {
            "Principal": {
              "DataLakePrincipalIdentifier": "IAM_ALLOWED_PRINCIPALS"
            },
            "Permissions": [
              "ALL"
            ]
          }
        ],
        "ExternalDataFilteringAllowList": [
          {
            "DataLakePrincipalIdentifier": "333333333333"
          }
        ],
        "MutationType": "APPEND"
        "Parameters": {
          "CROSS_ACCOUNT_VERSION": "3"
        },
        "TrustedResourceOwners": [
          "012345678910",
          "109876543210"
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-lakeformation-datalakesettings--examples--Input_format_for_DataLakeSettings_with_AllowExternalDataFiltering_set_to_true--yaml"></a>

```
Description: "DataLakeSettings_Example2"
Resources:
  DataLakeSettings:
    Type: AWS::LakeFormation::DataLakeSettings
    Properties:
      Admins:
        - DataLakePrincipalIdentifier: "arn:aws:iam::012345678910:role/sample-role1"
        - DataLakePrincipalIdentifier: "arn:aws:iam::012345678910:role/sample-role2"

      AllowFullTableExternalDataAccess: true
      AllowExternalDataFiltering: true
      AuthorizedSessionTagValueList:
        - "sample_val1"
        - "sample_val2"
      CreateDatabaseDefaultPermissions:
        - Principal:
            DataLakePrincipalIdentifier: "IAM_ALLOWED_PRINCIPALS"
          Permissions:
            - "ALL"
      CreateTableDefaultPermissions:
        - Principal:
            DataLakePrincipalIdentifier: "IAM_ALLOWED_PRINCIPALS"
          Permissions:
            - "ALL"
      ExternalDataFilteringAllowList:
        - DataLakePrincipalIdentifier: "333333333333"
      MutationType: "APPEND"
      Parameters:
        "CROSS_ACCOUNT_VERSION": "3"
      TrustedResourceOwners:
        - "012345678910"
        - "109876543210"
```