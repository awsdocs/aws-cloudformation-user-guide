# AWS::LakeFormation::PrincipalPermissions LFTagKeyResource<a name="aws-properties-lakeformation-principalpermissions-lftagkeyresource"></a>

A structure containing an LF\-tag key and values for a resource\.

## Syntax<a name="aws-properties-lakeformation-principalpermissions-lftagkeyresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-principalpermissions-lftagkeyresource-syntax.json"></a>

```
{
  "[CatalogId](#cfn-lakeformation-principalpermissions-lftagkeyresource-catalogid)" : String,
  "[TagKey](#cfn-lakeformation-principalpermissions-lftagkeyresource-tagkey)" : String,
  "[TagValues](#cfn-lakeformation-principalpermissions-lftagkeyresource-tagvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lakeformation-principalpermissions-lftagkeyresource-syntax.yaml"></a>

```
  [CatalogId](#cfn-lakeformation-principalpermissions-lftagkeyresource-catalogid): String
  [TagKey](#cfn-lakeformation-principalpermissions-lftagkeyresource-tagkey): String
  [TagValues](#cfn-lakeformation-principalpermissions-lftagkeyresource-tagvalues): 
    - String
```

## Properties<a name="aws-properties-lakeformation-principalpermissions-lftagkeyresource-properties"></a>

`CatalogId`  <a name="cfn-lakeformation-principalpermissions-lftagkeyresource-catalogid"></a>
The identifier for the Data Catalog where the location is registered with Data Catalog\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagKey`  <a name="cfn-lakeformation-principalpermissions-lftagkeyresource-tagkey"></a>
The key\-name for the LF\-tag\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagValues`  <a name="cfn-lakeformation-principalpermissions-lftagkeyresource-tagvalues"></a>
 A list of possible values for the corresponding `TagKey` of an LF\-tag key\-value pair\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)