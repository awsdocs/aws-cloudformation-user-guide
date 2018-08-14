# AWS::ServiceCatalog::TagOptionAssociation<a name="aws-resource-servicecatalog-tagoptionassociation"></a>

Associates the specified TagOption with the specified AWS Service Catalog resource\. For more information, see [AWS Service Catalog TagOptionLibrary](http://docs.aws.amazon.com/servicecatalog/latest/adminguide/tagoptions.html) in the *AWS Service Catalog Administrator Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-tagoptionassociation-syntax)
+ [Properties](#aws-resource-servicecatalog-tagoptionassociation-properties)
+ [Return Values](#aws-resource-servicecatalog-tagoptionassociation-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-tagoptionassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-tagoptionassociation-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::TagOptionAssociation",
  "Properties" : {
    "[TagOptionId](#cfn-servicecatalog-tagoptionassociation-tagoptionid)" : String,
    "[ResourceId](#cfn-servicecatalog-tagoptionassociation-resourceid)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-tagoptionassociation-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::TagOptionAssociation"
Properties:
  [TagOptionId](#cfn-servicecatalog-tagoptionassociation-tagoptionid): String
  [ResourceId](#cfn-servicecatalog-tagoptionassociation-resourceid): String
```

## Properties<a name="aws-resource-servicecatalog-tagoptionassociation-properties"></a>

`ResourceId`  <a name="cfn-servicecatalog-tagoptionassociation-resourceid"></a>
The resource identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TagOptionId`  <a name="cfn-servicecatalog-tagoptionassociation-tagoptionid"></a>
The TagOption identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicecatalog-tagoptionassociation-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-tagoptionassociation-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::TagOptionAssociation` resource to the intrinsic `Ref` function, the function returns an identifier for the association\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.