# AWS::LakeFormation::Permissions<a name="aws-resource-lakeformation-permissions"></a>

The AWS::LakeFormation::Permissions resource is an AWS Lake Formation resource type that grants or revokes AWS Lake Formation permissions\.

## Syntax<a name="aws-resource-lakeformation-permissions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-permissions-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::Permissions",
  "Properties" : {
      "[DataLakePrincipal](#cfn-lakeformation-permissions-datalakeprincipal)" : [DataLakePrincipal](aws-properties-lakeformation-permissions-datalakeprincipal.md),
      "[Permissions](#cfn-lakeformation-permissions-permissions)" : [ String, ... ],
      "[PermissionsWithGrantOption](#cfn-lakeformation-permissions-permissionswithgrantoption)" : [ String, ... ],
      "[Resource](#cfn-lakeformation-permissions-resource)" : [Resource](aws-properties-lakeformation-permissions-resource.md)
    }
}
```

### YAML<a name="aws-resource-lakeformation-permissions-syntax.yaml"></a>

```
Type: AWS::LakeFormation::Permissions
Properties: 
  [DataLakePrincipal](#cfn-lakeformation-permissions-datalakeprincipal): 
    [DataLakePrincipal](aws-properties-lakeformation-permissions-datalakeprincipal.md)
  [Permissions](#cfn-lakeformation-permissions-permissions): 
    - String
  [PermissionsWithGrantOption](#cfn-lakeformation-permissions-permissionswithgrantoption): 
    - String
  [Resource](#cfn-lakeformation-permissions-resource): 
    [Resource](aws-properties-lakeformation-permissions-resource.md)
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