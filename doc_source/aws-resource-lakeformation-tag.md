# AWS::LakeFormation::Tag<a name="aws-resource-lakeformation-tag"></a>

The `AWS::LakeFormation::Tag` resource represents an LF\-tag, which consists of a key and one or more possible values for the key\. During a stack operation, AWS CloudFormation calls the AWS Lake Formation `CreateLFTag` API to create a tag, and `UpdateLFTag` API to update a tag resource, and a `DeleteLFTag` to delete it\. 

## Syntax<a name="aws-resource-lakeformation-tag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-tag-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::Tag",
  "Properties" : {
      "[CatalogId](#cfn-lakeformation-tag-catalogid)" : String,
      "[TagKey](#cfn-lakeformation-tag-tagkey)" : String,
      "[TagValues](#cfn-lakeformation-tag-tagvalues)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-lakeformation-tag-syntax.yaml"></a>

```
Type: AWS::LakeFormation::Tag
Properties: 
  [CatalogId](#cfn-lakeformation-tag-catalogid): String
  [TagKey](#cfn-lakeformation-tag-tagkey): String
  [TagValues](#cfn-lakeformation-tag-tagvalues): 
    - String
```

## Properties<a name="aws-resource-lakeformation-tag-properties"></a>

`CatalogId`  <a name="cfn-lakeformation-tag-catalogid"></a>
Catalog id string, not less than 1 or more than 255 bytes long, matching the [single\-line string pattern](lake-formation/latest/dg/aws-lake-formation-api-aws-lake-formation-api-common.html#aws-glue-api-regex-oneLine)\.  
The identifier for the Data Catalog\. By default, the account ID\. The Data Catalog is the persistent metadata store\. It contains database definitions, table definitions, and other control information to manage your AWS Lake Formation environment\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagKey`  <a name="cfn-lakeformation-tag-tagkey"></a>
 UTF\-8 string, not less than 1 or more than 255 bytes long, matching the [single\-line string pattern](lake-formation/latest/dg/aws-lake-formation-api-aws-lake-formation-api-common.html#aws-glue-api-regex-oneLine)\.  
The key\-name for the LF\-tag\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagValues`  <a name="cfn-lakeformation-tag-tagvalues"></a>
 An array of UTF\-8 strings, not less than 1 or more than 50 strings\.  
 A list of possible values of the corresponding `TagKey` of an LF\-tag key\-value pair\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lakeformation-tag-return-values"></a>

### Ref<a name="aws-resource-lakeformation-tag-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Tag’s `TagKey` property value\.

For example: `tagKeyName`

## Remarks<a name="aws-resource-lakeformation-tag--remarks"></a>

 *Note the following:* 

 Only data lake administrators can create LF\-tags\.

An `LF-tag` can be assigned to Data Catalog resources \(databases, tables, and columns\) via [AWS::LakeFormation::TagAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lakeformation-tag.html) to implement tag\-based access control\.

## Examples<a name="aws-resource-lakeformation-tag--examples"></a>

### Creating a tag resource in a template<a name="aws-resource-lakeformation-tag--examples--Creating_a_tag_resource_in_a_template"></a>

The following example demonstrates how to define a tag resource in a template\.

#### JSON<a name="aws-resource-lakeformation-tag--examples--Creating_a_tag_resource_in_a_template--json"></a>

```
{
    "SampleTag": {
        "Type": "AWS::LakeFormation::Tag",
        "Properties": {
            "TagKey": "sample_tag_key",
            "TagValues": ["sample_tag_value1", "sample_tag_value2"]
        }
    }
}
```

#### YAML<a name="aws-resource-lakeformation-tag--examples--Creating_a_tag_resource_in_a_template--yaml"></a>

```
SampleTag:
    Type: AWS::LakeFormation::Tag
    Properties:
      TagKey: "sample_tag_key"
      TagValues:
        - "sample_tag_value1"
        - "sample_tag_value2"
```

## See also<a name="aws-resource-lakeformation-tag--seealso"></a>

[Assign an `LF-tag` to a Data Catalog resource \- AWS::LakeFormation::TagAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lakeformation-tagassociation-resource.html)\.