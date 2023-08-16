# AWS::ServiceCatalogAppRegistry::AttributeGroup<a name="aws-resource-servicecatalogappregistry-attributegroup"></a>

Creates a new attribute group as a container for user\-defined attributes\. This feature enables users to have full control over their cloud application's metadata in a rich machine\-readable format to facilitate integration with automated workflows and third\-party tools\.

## Syntax<a name="aws-resource-servicecatalogappregistry-attributegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalogappregistry-attributegroup-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalogAppRegistry::AttributeGroup",
  "Properties" : {
      "[Attributes](#cfn-servicecatalogappregistry-attributegroup-attributes)" : Json,
      "[Description](#cfn-servicecatalogappregistry-attributegroup-description)" : String,
      "[Name](#cfn-servicecatalogappregistry-attributegroup-name)" : String,
      "[Tags](#cfn-servicecatalogappregistry-attributegroup-tags)" : {Key: Value, ...}
    }
}
```

### YAML<a name="aws-resource-servicecatalogappregistry-attributegroup-syntax.yaml"></a>

```
Type: AWS::ServiceCatalogAppRegistry::AttributeGroup
Properties: 
  [Attributes](#cfn-servicecatalogappregistry-attributegroup-attributes): Json
  [Description](#cfn-servicecatalogappregistry-attributegroup-description): String
  [Name](#cfn-servicecatalogappregistry-attributegroup-name): String
  [Tags](#cfn-servicecatalogappregistry-attributegroup-tags): 
    Key: Value
```

## Properties<a name="aws-resource-servicecatalogappregistry-attributegroup-properties"></a>

`Attributes`  <a name="cfn-servicecatalogappregistry-attributegroup-attributes"></a>
 A nested object in a JSON or YAML template that supports arbitrary definitions\. Represents the attributes in an attribute group that describes an application and its components\.   
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-servicecatalogappregistry-attributegroup-description"></a>
The description of the attribute group that the user provides\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-servicecatalogappregistry-attributegroup-name"></a>
The name of the attribute group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[-.\w]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-servicecatalogappregistry-attributegroup-tags"></a>
Key\-value pairs you can use to associate with the attribute group\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-servicecatalogappregistry-attributegroup-return-values"></a>

### Ref<a name="aws-resource-servicecatalogappregistry-attributegroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the id\.

 



For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-servicecatalogappregistry-attributegroup-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-servicecatalogappregistry-attributegroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 The Amazon resource name \(ARN\) that specifies the attribute group across services\. 

`Id`  <a name="Id-fn::getatt"></a>
 The globally unique attribute group identifier of the attribute group\. 