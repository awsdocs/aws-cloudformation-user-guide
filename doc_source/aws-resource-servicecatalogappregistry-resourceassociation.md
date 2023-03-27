# AWS::ServiceCatalogAppRegistry::ResourceAssociation<a name="aws-resource-servicecatalogappregistry-resourceassociation"></a>

The `AWS::ServiceCatalogAppRegistry::ResourceAssociation` resource for `ServiceCatalogAppRegistry`\.

## Syntax<a name="aws-resource-servicecatalogappregistry-resourceassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalogappregistry-resourceassociation-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalogAppRegistry::ResourceAssociation",
  "Properties" : {
      "[Application](#cfn-servicecatalogappregistry-resourceassociation-application)" : String,
      "[Resource](#cfn-servicecatalogappregistry-resourceassociation-resource)" : String,
      "[ResourceType](#cfn-servicecatalogappregistry-resourceassociation-resourcetype)" : String
    }
}
```

### YAML<a name="aws-resource-servicecatalogappregistry-resourceassociation-syntax.yaml"></a>

```
Type: AWS::ServiceCatalogAppRegistry::ResourceAssociation
Properties: 
  [Application](#cfn-servicecatalogappregistry-resourceassociation-application): String
  [Resource](#cfn-servicecatalogappregistry-resourceassociation-resource): String
  [ResourceType](#cfn-servicecatalogappregistry-resourceassociation-resourcetype): String
```

## Properties<a name="aws-resource-servicecatalogappregistry-resourceassociation-properties"></a>

`Application`  <a name="cfn-servicecatalogappregistry-resourceassociation-application"></a>
The name or ID of the application\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Resource`  <a name="cfn-servicecatalogappregistry-resourceassociation-resource"></a>
The name or ID of the resource of which the application will be associated\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-servicecatalogappregistry-resourceassociation-resourcetype"></a>
The type of resource of which the application will be associated\. Possible values: CFN\_STACK\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-servicecatalogappregistry-resourceassociation-return-values"></a>

### Ref<a name="aws-resource-servicecatalogappregistry-resourceassociation-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-servicecatalogappregistry-resourceassociation-return-values-fn--getatt"></a>

#### <a name="aws-resource-servicecatalogappregistry-resourceassociation-return-values-fn--getatt-fn--getatt"></a>

`ApplicationArn`  <a name="ApplicationArn-fn::getatt"></a>
Property description not available\.

`Id`  <a name="Id-fn::getatt"></a>
The Id of the Association\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

`ResourceArn`  <a name="ResourceArn-fn::getatt"></a>
Property description not available\.