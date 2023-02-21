# AWS::LakeFormation::TagAssociation LFTagPair<a name="aws-properties-lakeformation-tagassociation-lftagpair"></a>

 A structure containing the catalog ID, tag key, and tag values of an LF\-tag key\-value pair\. 

## Syntax<a name="aws-properties-lakeformation-tagassociation-lftagpair-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-tagassociation-lftagpair-syntax.json"></a>

```
{
  "[CatalogId](#cfn-lakeformation-tagassociation-lftagpair-catalogid)" : String,
  "[TagKey](#cfn-lakeformation-tagassociation-lftagpair-tagkey)" : String,
  "[TagValues](#cfn-lakeformation-tagassociation-lftagpair-tagvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lakeformation-tagassociation-lftagpair-syntax.yaml"></a>

```
  [CatalogId](#cfn-lakeformation-tagassociation-lftagpair-catalogid): String
  [TagKey](#cfn-lakeformation-tagassociation-lftagpair-tagkey): String
  [TagValues](#cfn-lakeformation-tagassociation-lftagpair-tagvalues): 
    - String
```

## Properties<a name="aws-properties-lakeformation-tagassociation-lftagpair-properties"></a>

`CatalogId`  <a name="cfn-lakeformation-tagassociation-lftagpair-catalogid"></a>
The identifier for the Data Catalog\. By default, it is the account ID of the caller\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagKey`  <a name="cfn-lakeformation-tagassociation-lftagpair-tagkey"></a>
The key\-name for the LF\-tag\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagValues`  <a name="cfn-lakeformation-tagassociation-lftagpair-tagvalues"></a>
 A list of possible values of the corresponding `TagKey` of an LF\-tag key\-value pair\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)