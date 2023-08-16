# AWS::LakeFormation::PrincipalPermissions LFTagPolicyResource<a name="aws-properties-lakeformation-principalpermissions-lftagpolicyresource"></a>

A list of LF\-tag conditions that define a resource's LF\-tag policy\.

A structure that allows an admin to grant user permissions on certain conditions\. For example, granting a role access to all columns that do not have the LF\-tag 'PII' in tables that have the LF\-tag 'Prod'\.

## Syntax<a name="aws-properties-lakeformation-principalpermissions-lftagpolicyresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-principalpermissions-lftagpolicyresource-syntax.json"></a>

```
{
  "[CatalogId](#cfn-lakeformation-principalpermissions-lftagpolicyresource-catalogid)" : String,
  "[Expression](#cfn-lakeformation-principalpermissions-lftagpolicyresource-expression)" : [ LFTag, ... ],
  "[ResourceType](#cfn-lakeformation-principalpermissions-lftagpolicyresource-resourcetype)" : String
}
```

### YAML<a name="aws-properties-lakeformation-principalpermissions-lftagpolicyresource-syntax.yaml"></a>

```
  [CatalogId](#cfn-lakeformation-principalpermissions-lftagpolicyresource-catalogid): String
  [Expression](#cfn-lakeformation-principalpermissions-lftagpolicyresource-expression): 
    - LFTag
  [ResourceType](#cfn-lakeformation-principalpermissions-lftagpolicyresource-resourcetype): String
```

## Properties<a name="aws-properties-lakeformation-principalpermissions-lftagpolicyresource-properties"></a>

`CatalogId`  <a name="cfn-lakeformation-principalpermissions-lftagpolicyresource-catalogid"></a>
The identifier for the Data Catalog\. The Data Catalog is the persistent metadata store\. It contains database definitions, table definitions, and other control information to manage your AWS Lake Formation environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Expression`  <a name="cfn-lakeformation-principalpermissions-lftagpolicyresource-expression"></a>
A list of LF\-tag conditions that apply to the resource's LF\-tag policy\.  
*Required*: Yes  
*Type*: List of [LFTag](aws-properties-lakeformation-principalpermissions-lftag.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceType`  <a name="cfn-lakeformation-principalpermissions-lftagpolicyresource-resourcetype"></a>
The resource type for which the LF\-tag policy applies\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-properties-lakeformation-principalpermissions-lftagpolicyresource--examples"></a>

### Permissions on LF\-tag policy resource<a name="aws-properties-lakeformation-principalpermissions-lftagpolicyresource--examples--Permissions_on_LF-tag_policy_resource"></a>

The following example demonstrates how to grant permissions on a `LFTagPolicy` resource\.

#### JSON<a name="aws-properties-lakeformation-principalpermissions-lftagpolicyresource--examples--Permissions_on_LF-tag_policy_resource--json"></a>

```
{    
  "SamplePermission": {
      "LFTagPolicy": {
          "CatalogId": "12345678910",
          "ResourceType": "TABLE",
          "Expression": [
              {
                  "TagKey": "sample_key",
                  "TagValues": ["sample_value"]
              }
          ]
      }
    },
    "Permissions": ["DESCRIBE"],
    "PermissionsWithGrantOption": ["DESCRIBE"]
}
```

#### YAML<a name="aws-properties-lakeformation-principalpermissions-lftagpolicyresource--examples--Permissions_on_LF-tag_policy_resource--yaml"></a>

```
SamplePermission:
  Type: AWS::LakeFormation::PrincipalPermissions
  Properties:
    Principal:
      DataLakePrincipalIdentifier: "arn:sample_principal"
    Resource:
      LFTagPolicy:
        CatalogId: "12345678910"
        ResourceType: "TABLE"
        Expression:
          - TagKey: "sample_key"
            TagValues: "sample_value"
    Permissions: 
          - "DESCRIBE"
    PermissionsWithGrantOption: 
         - "DESCRIBE"
```