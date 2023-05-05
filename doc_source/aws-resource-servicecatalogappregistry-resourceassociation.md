# AWS::ServiceCatalogAppRegistry::ResourceAssociation<a name="aws-resource-servicecatalogappregistry-resourceassociation"></a>

 Associates a resource with an application\. Both the resource and the application can be specified either by ID or name\. 

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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Resource`  <a name="cfn-servicecatalogappregistry-resourceassociation-resource"></a>
 The name or ID of the resource of which the application will be associated\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceType`  <a name="cfn-servicecatalogappregistry-resourceassociation-resourcetype"></a>
 The type of resource of which the application will be associated\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-servicecatalogappregistry-resourceassociation-return-values"></a>

### Ref<a name="aws-resource-servicecatalogappregistry-resourceassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the id\.

 



For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-servicecatalogappregistry-resourceassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-servicecatalogappregistry-resourceassociation-return-values-fn--getatt-fn--getatt"></a>

`ApplicationArn`  <a name="ApplicationArn-fn::getatt"></a>
 The Amazon resource name \(ARN\) that specifies the application\. 

`Id`  <a name="Id-fn::getatt"></a>
 The Id of the Association\. 

`ResourceArn`  <a name="ResourceArn-fn::getatt"></a>
 The Amazon resource name \(ARN\) that specifies the resource\. 