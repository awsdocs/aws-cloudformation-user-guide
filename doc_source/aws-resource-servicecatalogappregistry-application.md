# AWS::ServiceCatalogAppRegistry::Application<a name="aws-resource-servicecatalogappregistry-application"></a>

Represents a AWS Service Catalog AppRegistry application that is the top\-level node in a hierarchy of related cloud resource abstractions\.

## Syntax<a name="aws-resource-servicecatalogappregistry-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalogappregistry-application-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalogAppRegistry::Application",
  "Properties" : {
      "[Description](#cfn-servicecatalogappregistry-application-description)" : String,
      "[Name](#cfn-servicecatalogappregistry-application-name)" : String,
      "[Tags](#cfn-servicecatalogappregistry-application-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-servicecatalogappregistry-application-syntax.yaml"></a>

```
Type: AWS::ServiceCatalogAppRegistry::Application
Properties: 
  [Description](#cfn-servicecatalogappregistry-application-description): String
  [Name](#cfn-servicecatalogappregistry-application-name): String
  [Tags](#cfn-servicecatalogappregistry-application-tags): 
    Key : Value
```

## Properties<a name="aws-resource-servicecatalogappregistry-application-properties"></a>

`Description`  <a name="cfn-servicecatalogappregistry-application-description"></a>
The description of the application\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-servicecatalogappregistry-application-name"></a>
The name of the application\. The name must be unique in the region in which you are creating the application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[-.\w]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-servicecatalogappregistry-application-tags"></a>
Key\-value pairs you can use to associate with the application\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-servicecatalogappregistry-application-return-values"></a>

### Ref<a name="aws-resource-servicecatalogappregistry-application-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Id\.

 



For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-servicecatalogappregistry-application-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-servicecatalogappregistry-application-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 The Amazon resource name \(ARN\) that specifies the application across services\. 

`Id`  <a name="Id-fn::getatt"></a>
 The identifier of the application\. 