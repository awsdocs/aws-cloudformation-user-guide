# AWS::QuickSight::DataSet RowLevelPermissionDataSet<a name="aws-properties-quicksight-dataset-rowlevelpermissiondataset"></a>

Information about a dataset that contains permissions for row\-level security \(RLS\)\. The permissions dataset maps fields to users or groups\. For more information, see [Using Row\-Level Security \(RLS\) to Restrict Access to a Dataset](https://docs.aws.amazon.com/quicksight/latest/user/restrict-access-to-a-data-set-using-row-level-security.html) in the *Amazon QuickSight User Guide*\.

The option to deny permissions by setting `PermissionPolicy` to `DENY_ACCESS` is not supported for new RLS datasets\.

## Syntax<a name="aws-properties-quicksight-dataset-rowlevelpermissiondataset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-rowlevelpermissiondataset-syntax.json"></a>

```
{
  "[Arn](#cfn-quicksight-dataset-rowlevelpermissiondataset-arn)" : String,
  "[Namespace](#cfn-quicksight-dataset-rowlevelpermissiondataset-namespace)" : String,
  "[PermissionPolicy](#cfn-quicksight-dataset-rowlevelpermissiondataset-permissionpolicy)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-rowlevelpermissiondataset-syntax.yaml"></a>

```
  [Arn](#cfn-quicksight-dataset-rowlevelpermissiondataset-arn): String
  [Namespace](#cfn-quicksight-dataset-rowlevelpermissiondataset-namespace): String
  [PermissionPolicy](#cfn-quicksight-dataset-rowlevelpermissiondataset-permissionpolicy): String
```

## Properties<a name="aws-properties-quicksight-dataset-rowlevelpermissiondataset-properties"></a>

`Arn`  <a name="cfn-quicksight-dataset-rowlevelpermissiondataset-arn"></a>
The Amazon Resource Name \(ARN\) of the dataset that contains permissions for RLS\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-quicksight-dataset-rowlevelpermissiondataset-namespace"></a>
The namespace associated with the dataset that contains permissions for RLS\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `^[a-zA-Z0-9._-]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PermissionPolicy`  <a name="cfn-quicksight-dataset-rowlevelpermissiondataset-permissionpolicy"></a>
The type of permissions to use when interpretting the permissions for RLS\. `DENY_ACCESS` is included for backward compatibility only\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DENY_ACCESS | GRANT_ACCESS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)