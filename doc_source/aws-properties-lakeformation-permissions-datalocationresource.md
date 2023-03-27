# AWS::LakeFormation::Permissions DataLocationResource<a name="aws-properties-lakeformation-permissions-datalocationresource"></a>

A structure for a data location object where permissions are granted or revoked\. 

## Syntax<a name="aws-properties-lakeformation-permissions-datalocationresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-permissions-datalocationresource-syntax.json"></a>

```
{
  "[CatalogId](#cfn-lakeformation-permissions-datalocationresource-catalogid)" : String,
  "[S3Resource](#cfn-lakeformation-permissions-datalocationresource-s3resource)" : String
}
```

### YAML<a name="aws-properties-lakeformation-permissions-datalocationresource-syntax.yaml"></a>

```
  [CatalogId](#cfn-lakeformation-permissions-datalocationresource-catalogid): String
  [S3Resource](#cfn-lakeformation-permissions-datalocationresource-s3resource): String
```

## Properties<a name="aws-properties-lakeformation-permissions-datalocationresource-properties"></a>

`CatalogId`  <a name="cfn-lakeformation-permissions-datalocationresource-catalogid"></a>
The identifier for the Data Catalog\. By default, it is the account ID of the caller\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Resource`  <a name="cfn-lakeformation-permissions-datalocationresource-s3resource"></a>
The Amazon Resource Name \(ARN\) that uniquely identifies the data location resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)