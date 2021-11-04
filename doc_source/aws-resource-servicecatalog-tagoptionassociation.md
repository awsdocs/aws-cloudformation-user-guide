# AWS::ServiceCatalog::TagOptionAssociation<a name="aws-resource-servicecatalog-tagoptionassociation"></a>

Associate the specified TagOption with the specified portfolio or product\.

## Syntax<a name="aws-resource-servicecatalog-tagoptionassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-tagoptionassociation-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::TagOptionAssociation",
  "Properties" : {
      "[ResourceId](#cfn-servicecatalog-tagoptionassociation-resourceid)" : String,
      "[TagOptionId](#cfn-servicecatalog-tagoptionassociation-tagoptionid)" : String
    }
}
```

### YAML<a name="aws-resource-servicecatalog-tagoptionassociation-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::TagOptionAssociation
Properties: 
  [ResourceId](#cfn-servicecatalog-tagoptionassociation-resourceid): String
  [TagOptionId](#cfn-servicecatalog-tagoptionassociation-tagoptionid): String
```

## Properties<a name="aws-resource-servicecatalog-tagoptionassociation-properties"></a>

`ResourceId`  <a name="cfn-servicecatalog-tagoptionassociation-resourceid"></a>
The resource identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagOptionId`  <a name="cfn-servicecatalog-tagoptionassociation-tagoptionid"></a>
The TagOption identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-servicecatalog-tagoptionassociation-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-tagoptionassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns an identifier for the association\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-servicecatalog-tagoptionassociation--seealso"></a>
+ [AssociateTagOptionWithResource](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_AssociateTagOptionWithResource.html) in the *AWS Service Catalog API Reference*

