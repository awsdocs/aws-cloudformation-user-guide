# AWS::LakeFormation::Permissions<a name="aws-resource-lakeformation-permissions"></a>

The `AWS::LakeFormation::Permissions` resource represents the permissions that a principal has on an AWS Glue Data Catalog resource \(such as AWS Glue database or AWS Glue tables\)\. When you upload a permissions stack, the permissions are granted to the principal and when you remove the stack, the permissions are revoked from the principal\. If you remove a stack, and the principal does not have the permissions referenced in the stack then AWS Lake Formation will throw an error because you can’t call revoke on non\-existing permissions\. To successfully remove the stack, you’ll need to regrant those permissions and then remove the stack\. 

## Syntax<a name="aws-resource-lakeformation-permissions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-permissions-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::Permissions",
  "Properties" : {
      "[DataLakePrincipal](#cfn-lakeformation-permissions-datalakeprincipal)" : DataLakePrincipal,
      "[Permissions](#cfn-lakeformation-permissions-permissions)" : [ String, ... ],
      "[PermissionsWithGrantOption](#cfn-lakeformation-permissions-permissionswithgrantoption)" : [ String, ... ],
      "[Resource](#cfn-lakeformation-permissions-resource)" : Resource
    }
}
```

### YAML<a name="aws-resource-lakeformation-permissions-syntax.yaml"></a>

```
Type: AWS::LakeFormation::Permissions
Properties: 
  [DataLakePrincipal](#cfn-lakeformation-permissions-datalakeprincipal): 
    DataLakePrincipal
  [Permissions](#cfn-lakeformation-permissions-permissions): 
    - String
  [PermissionsWithGrantOption](#cfn-lakeformation-permissions-permissionswithgrantoption): 
    - String
  [Resource](#cfn-lakeformation-permissions-resource): 
    Resource
```

## Properties<a name="aws-resource-lakeformation-permissions-properties"></a>

`DataLakePrincipal`  <a name="cfn-lakeformation-permissions-datalakeprincipal"></a>
The AWS Lake Formation principal\.  
*Required*: Yes  
*Type*: [DataLakePrincipal](aws-properties-lakeformation-permissions-datalakeprincipal.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permissions`  <a name="cfn-lakeformation-permissions-permissions"></a>
The permissions granted or revoked\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PermissionsWithGrantOption`  <a name="cfn-lakeformation-permissions-permissionswithgrantoption"></a>
Indicates whether to grant the ability to grant permissions \(as a subset of permissions granted\)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Resource`  <a name="cfn-lakeformation-permissions-resource"></a>
A structure for the resource\.  
*Required*: Yes  
*Type*: [Resource](aws-properties-lakeformation-permissions-resource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)