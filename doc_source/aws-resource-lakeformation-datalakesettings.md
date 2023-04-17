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
Whether to allow Amazon EMR clusters to access data managed by Lake Formation\.   
If true, you allow Amazon EMR clusters to access data in Amazon S3 locations that are registered with Lake Formation\.  
If false or null, no Amazon EMR clusters will be able to access data in Amazon S3 locations that are registered with Lake Formation\.  
For more information, see [\(Optional\) Allow Data Filtering on Amazon EMR](https://docs-aws.amazon.com/lake-formation/latest/dg/getting-started-setup.html#emr-switch)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizedSessionTagValueList`  <a name="cfn-lakeformation-datalakesettings-authorizedsessiontagvaluelist"></a>
Lake Formation relies on a privileged process secured by Amazon EMR or the third party integrator to tag the user's role while assuming it\. Lake Formation will publish the acceptable key\-value pair, for example key = "LakeFormationTrustedCaller" and value = "TRUE" and the third party integrator must properly tag the temporary security credentials that will be used to call Lake Formation's administrative APIs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreateDatabaseDefaultPermissions`  <a name="cfn-lakeformation-datalakesettings-createdatabasedefaultpermissions"></a>
Specifies whether access control on newly created database is managed by Lake Formation permissions or exclusively by IAM permissions\.  
A null value indicates access control by Lake Formation permissions\. A value that assigns ALL to IAM\_ALLOWED\_PRINCIPALS indicates access control by IAM permissions\. This is referred to as the setting "Use only IAM access control," and is for backward compatibility with the AWS Glue permission model implemented by IAM permissions\.  
The only permitted values are an empty array or an array that contains a single JSON object that grants ALL to IAM\_ALLOWED\_PRINCIPALS\.  
For more information, see [Changing the Default Security Settings for Your Data Lake](https://docs.aws.amazon.com/lake-formation/latest/dg/change-settings.html)\.  
*Required*: No  
*Type*: [CreateDatabaseDefaultPermissions](aws-properties-lakeformation-datalakesettings-createdatabasedefaultpermissions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreateTableDefaultPermissions`  <a name="cfn-lakeformation-datalakesettings-createtabledefaultpermissions"></a>
Specifies whether access control on newly created table is managed by Lake Formation permissions or exclusively by IAM permissions\.  
A null value indicates access control by Lake Formation permissions\. A value that assigns ALL to IAM\_ALLOWED\_PRINCIPALS indicates access control by IAM permissions\. This is referred to as the setting "Use only IAM access control," and is for backward compatibility with the AWS Glue permission model implemented by IAM permissions\.  
The only permitted values are an empty array or an array that contains a single JSON object that grants ALL to IAM\_ALLOWED\_PRINCIPALS\.  
For more information, see [Changing the Default Security Settings for Your Data Lake](https://docs.aws.amazon.com/lake-formation/latest/dg/change-settings.html)\.  
*Required*: No  
*Type*: [CreateTableDefaultPermissions](aws-properties-lakeformation-datalakesettings-createtabledefaultpermissions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExternalDataFilteringAllowList`  <a name="cfn-lakeformation-datalakesettings-externaldatafilteringallowlist"></a>
A list of the account IDs of AWS accounts with Amazon EMR clusters that are to perform data filtering\.>  
*Required*: No  
*Type*: [ExternalDataFilteringAllowList](aws-properties-lakeformation-datalakesettings-externaldatafilteringallowlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-lakeformation-datalakesettings-parameters"></a>
A key\-value map that provides an additional configuration on your data lake\. CrossAccountVersion is the key you can configure in the Parameters field\. Accepted values for the CrossAccountVersion key are 1, 2, and 3\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustedResourceOwners`  <a name="cfn-lakeformation-datalakesettings-trustedresourceowners"></a>
 An array of UTF\-8 strings\.  
A list of the resource\-owning account IDs that the caller's account can use to share their user access details \(user ARNs\)\. The user ARNs can be logged in the resource owner's CloudTrail log\. You may want to specify this property when you are in a high\-trust boundary, such as the same team or company\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)