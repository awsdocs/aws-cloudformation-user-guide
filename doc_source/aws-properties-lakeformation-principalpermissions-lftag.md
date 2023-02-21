# AWS::LakeFormation::PrincipalPermissions LFTag<a name="aws-properties-lakeformation-principalpermissions-lftag"></a>

The LF\-tag key and values attached to a resource\.

## Syntax<a name="aws-properties-lakeformation-principalpermissions-lftag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-principalpermissions-lftag-syntax.json"></a>

```
{
  "[TagKey](#cfn-lakeformation-principalpermissions-lftag-tagkey)" : String,
  "[TagValues](#cfn-lakeformation-principalpermissions-lftag-tagvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lakeformation-principalpermissions-lftag-syntax.yaml"></a>

```
  [TagKey](#cfn-lakeformation-principalpermissions-lftag-tagkey): String
  [TagValues](#cfn-lakeformation-principalpermissions-lftag-tagvalues): 
    - String
```

## Properties<a name="aws-properties-lakeformation-principalpermissions-lftag-properties"></a>

`TagKey`  <a name="cfn-lakeformation-principalpermissions-lftag-tagkey"></a>
The key\-name for the LF\-tag\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagValues`  <a name="cfn-lakeformation-principalpermissions-lftag-tagvalues"></a>
 A list of possible values of the corresponding `TagKey` of an LF\-tag key\-value pair\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-properties-lakeformation-principalpermissions-lftag--examples"></a>

### Permissons on an LF\-tag<a name="aws-properties-lakeformation-principalpermissions-lftag--examples--Permissons_on_an_LF-tag"></a>

The following example demonstrates how to grant permissions on a `LFTag` resource:

#### JSON<a name="aws-properties-lakeformation-principalpermissions-lftag--examples--Permissons_on_an_LF-tag--json"></a>

```
{
    "SamplePermission": {
        "LFTag": {
            "CatalogId": "12345678910",
            "TagKey": "sample_key",
            "TagValues": ["sample_value"]
        }
    },
    "Permissions": ["DESCRIBE"],
    "PermissionsWithGrantOption": ["DESCRIBE"]
}
```

#### YAML<a name="aws-properties-lakeformation-principalpermissions-lftag--examples--Permissons_on_an_LF-tag--yaml"></a>

```
SamplePermission:
  Type: AWS::LakeFormation::PrincipalPermissions
  Properties:
    Principal:
      DataLakePrincipalIdentifier: "arn:sample_principal"
    Resource:
      LFTag:
        CatalogId: "12345678910"
        TagKey: "sample_key"
        TagValues: 
           - "sample_value"
    Permissions: 
          - "DESCRIBE"
    PermissionsWithGrantOption: 
         - "DESCRIBE"
```