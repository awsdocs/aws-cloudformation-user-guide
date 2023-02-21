# AWS::LakeFormation::TagAssociation<a name="aws-resource-lakeformation-tagassociation"></a>

 The `AWS::LakeFormation::TagAssociation` resource represents an assignment of an LF\-tag to a Data Catalog resource \(database, table, or column\)\. During a stack operation, CloudFormation calls AWS Lake Formation `AddLFTagsToResource` API to create a `TagAssociation` resource and calls the `RemoveLFTagsToResource` API to delete it\.

## Syntax<a name="aws-resource-lakeformation-tagassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-tagassociation-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::TagAssociation",
  "Properties" : {
      "[LFTags](#cfn-lakeformation-tagassociation-lftags)" : [ LFTagPair, ... ],
      "[Resource](#cfn-lakeformation-tagassociation-resource)" : Resource
    }
}
```

### YAML<a name="aws-resource-lakeformation-tagassociation-syntax.yaml"></a>

```
Type: AWS::LakeFormation::TagAssociation
Properties: 
  [LFTags](#cfn-lakeformation-tagassociation-lftags): 
    - LFTagPair
  [Resource](#cfn-lakeformation-tagassociation-resource): 
    Resource
```

## Properties<a name="aws-resource-lakeformation-tagassociation-properties"></a>

`LFTags`  <a name="cfn-lakeformation-tagassociation-lftags"></a>
 A structure containing an LF\-tag key\-value pair\.   
*Required*: Yes  
*Type*: List of [LFTagPair](aws-properties-lakeformation-tagassociation-lftagpair.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Resource`  <a name="cfn-lakeformation-tagassociation-resource"></a>
UTF\-8 string \(valid values: `DATABASE | TABLE`\)\.  
The resource for which the LF\-tag policy applies\.  
*Required*: Yes  
*Type*: [Resource](aws-properties-lakeformation-tagassociation-resource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-lakeformation-tagassociation-return-values"></a>

### Ref<a name="aws-resource-lakeformation-tagassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a combination of the `ResourceIdentifier` and `TagsIdentifier` seperated with a pipe\. 

For example: `{"Catalog":null,"Database":{"CatalogId":null,"Name":"ExampleDbName"},"Table":null,"TableWithColumns":null}|[{"CatalogId":null,"TagKey":"tagKey1","TagValues":null}]`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-lakeformation-tagassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lakeformation-tagassociation-return-values-fn--getatt-fn--getatt"></a>

`ResourceIdentifier`  <a name="ResourceIdentifier-fn::getatt"></a>
Json encoding of the input resource\.  

**Examples**
+ Database:`{"Catalog":null,"Database":{"CatalogId":"123456789012","Name":"ExampleDbName"},"Table":null,"TableWithColumns":null}`
+ Table: `{"Catalog":null,"Database":null,"Table":{"CatalogId":"123456789012","DatabaseName":"ExampleDbName","Name":"ExampleTableName","TableWildcard":null},"TableWithColumns":null}`
+ Columns: `{"Catalog":null,"Database":null,"Table":null,"TableWithColumns":{"CatalogId":"123456789012","DatabaseName":"ExampleDbName","Name":"ExampleTableName","ColumnNames":["ExampleColName1","ExampleColName2"]}}`

`TagsIdentifier`  <a name="TagsIdentifier-fn::getatt"></a>
Json encoding of the input LFTags list\.  
For example: `[{"CatalogId":null,"TagKey":"tagKey1","TagValues":null},{"CatalogId":null,"TagKey":"tagKey2","TagValues":null}]` 

## Remarks<a name="aws-resource-lakeformation-tagassociation--remarks"></a>

Note that for a valid `TagAssociation` to be created, a database or table or column\(s\) must be specified\. 

## Examples<a name="aws-resource-lakeformation-tagassociation--examples"></a>

### Examples for creating an LF\-tag for a database<a name="aws-resource-lakeformation-tagassociation--examples--Examples_for_creating_an_LF-tag_for_a_database"></a>

The following example demonstrates how to create an LF\-tag on a database\.

#### JSON<a name="aws-resource-lakeformation-tagassociation--examples--Examples_for_creating_an_LF-tag_for_a_database--json"></a>

```
{
    "SampleTagOnDatabase": {
        "Type": "AWS::LakeFormation::TagAssociation",
        "Properties": {
            "Resource": {
                "Database": {
                    "CatalogId": "12345678910",
                    "Name": "sample_db"
                }
            },
            "LFTags": [
                {
                    "CatalogId": "12345678910",
                    "TagKey": "sample_tag_key",
                    "TagValues": ["sample_tag_value1"]
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-lakeformation-tagassociation--examples--Examples_for_creating_an_LF-tag_for_a_database--yaml"></a>

```
SampleTagOnDatabase:
    Type: AWS::LakeFormation::TagAssociation
    Properties:
      Resource:
        Database:
          CatalogId: "12345678910"
          Name: "sample_db"
      LFTags:
        - CatalogId: "12345678910"
          TagKey: "sample_tag_key"
          TagValues:
            - "sample_tag_value1"
```

### Examples for creating and LF\-tag for a table<a name="aws-resource-lakeformation-tagassociation--examples--Examples_for_creating_and_LF-tag_for_a_table"></a>

The following example demonstrates how to create an LF\-tag on a table\.

#### JSON<a name="aws-resource-lakeformation-tagassociation--examples--Examples_for_creating_and_LF-tag_for_a_table--json"></a>

```
{
    "SampleTagOnTable": {
        "Type": "AWS::LakeFormation::TagAssociation",
        "Properties": {
            "Resource": {
                "Table": {
                    "CatalogId": "12345678910",
                    "DatabaseName": "sample_db",
                    "Name": "sample_tbl"
                }
            },
            "LFTags": [
                {
                    "CatalogId": "12345678910",
                    "TagKey": "sample_tag_key",
                    "TagValues": ["sample_tag_value1"]
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-lakeformation-tagassociation--examples--Examples_for_creating_and_LF-tag_for_a_table--yaml"></a>

```
SampleTagOnTable:
    Type: AWS::LakeFormation::TagAssociation
    Properties:
      Resource:
        Table:
          CatalogId: "12345678910"
          DatabaseName: "sample_db"
          Name: "sample_tbl"
      LFTags:
        - CatalogId: "12345678910"
          TagKey: "sample_tag_key"
          TagValues:
            - "sample_tag_value1"
```

### Examples for creating an LF\-tag for columns<a name="aws-resource-lakeformation-tagassociation--examples--Examples_for_creating_an_LF-tag_for_columns"></a>

The following example demonstrates how to create LF\-tags on columns\.

#### <a name="aws-resource-lakeformation-tagassociation--examples--Examples_for_creating_an_LF-tag_for_columns--jason"></a>

```
{
    "SampleTagOnColumn": {
        "Type": "AWS::LakeFormation::TagAssociation",
        "Properties": {
            "Resource": {
                "TableWithColumns": {
                    "CatalogId": "12345678910",
                    "DatabaseName": "sample_db",
                    "Name": "sample_tbl",
                    "ColumnNames": ["sample_col1", "sample_col2"]
                }
            },
            "LFTags": [
                {
                    "CatalogId": "12345678910",
                    "TagKey": "sample_tag_key",
                    "TagValues": ["sample_tag_value1"]
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-lakeformation-tagassociation--examples--Examples_for_creating_an_LF-tag_for_columns--yaml"></a>

```
TestTagAssociation:
    Type: AWS::LakeFormation::TagAssociation
    Properties:
      Resource:
        TableWithColumns:
          CatalogId: "12345678910"
          DatabaseName: "sample_db"
          Name: "sample_tbl"
          ColumnNames:
            - "sample_col1"
            - "sample_col2"
      LFTags:
        - CatalogId: "12345678910"
          TagKey: "sample_tag_key"
          TagValues:
            - "sample_tag_value1"
```

## See also<a name="aws-resource-lakeformation-tagassociation--seealso"></a>

[Permission requirements for tag assignments\.](https://docs.aws.amazon.com/lake-formation/latest/dg/TBAC-assigning-tags.html)