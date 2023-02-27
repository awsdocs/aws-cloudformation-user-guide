# AWS::ServiceCatalogAppRegistry::AttributeGroupAssociation<a name="aws-resource-servicecatalogappregistry-attributegroupassociation"></a>

The `AWS::ServiceCatalogAppRegistry::AttributeGroupAssociation` resource for `ServiceCatalogAppRegistry`\.

## Syntax<a name="aws-resource-servicecatalogappregistry-attributegroupassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalogappregistry-attributegroupassociation-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalogAppRegistry::AttributeGroupAssociation",
  "Properties" : {
      "[Application](#cfn-servicecatalogappregistry-attributegroupassociation-application)" : String,
      "[AttributeGroup](#cfn-servicecatalogappregistry-attributegroupassociation-attributegroup)" : String
    }
}
```

### YAML<a name="aws-resource-servicecatalogappregistry-attributegroupassociation-syntax.yaml"></a>

```
Type: AWS::ServiceCatalogAppRegistry::AttributeGroupAssociation
Properties: 
  [Application](#cfn-servicecatalogappregistry-attributegroupassociation-application): String
  [AttributeGroup](#cfn-servicecatalogappregistry-attributegroupassociation-attributegroup): String
```

## Properties<a name="aws-resource-servicecatalogappregistry-attributegroupassociation-properties"></a>

`Application`  <a name="cfn-servicecatalogappregistry-attributegroupassociation-application"></a>
The name or ID of the application\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AttributeGroup`  <a name="cfn-servicecatalogappregistry-attributegroupassociation-attributegroup"></a>
The name or ID of the attribute group that holds the attributes to describe the application\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-servicecatalogappregistry-attributegroupassociation-return-values"></a>

### Ref<a name="aws-resource-servicecatalogappregistry-attributegroupassociation-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-servicecatalogappregistry-attributegroupassociation-return-values-fn--getatt"></a>

#### <a name="aws-resource-servicecatalogappregistry-attributegroupassociation-return-values-fn--getatt-fn--getatt"></a>

`ApplicationArn`  <a name="ApplicationArn-fn::getatt"></a>
Property description not available\.

`AttributeGroupArn`  <a name="AttributeGroupArn-fn::getatt"></a>
Property description not available\.

`Id`  <a name="Id-fn::getatt"></a>
The Id of the Association\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.