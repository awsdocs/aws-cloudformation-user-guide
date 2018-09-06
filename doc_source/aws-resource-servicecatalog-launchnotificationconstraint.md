# AWS::ServiceCatalog::LaunchNotificationConstraint<a name="aws-resource-servicecatalog-launchnotificationconstraint"></a>

Creates a notification constraint for AWS Service Catalog\. For more information, see [CreateConstraint](http://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateConstraint.html) in the *AWS Service Catalog Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-launchnotificationconstraint-syntax)
+ [Properties](#aws-resource-servicecatalog-launchnotificationconstraint-properties)
+ [Return Values](#aws-resource-servicecatalog-launchnotificationconstraint-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-launchnotificationconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-launchnotificationconstraint-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::LaunchNotificationConstraint",
  "Properties" : {
    "[Description](#cfn-servicecatalog-launchnotificationconstraint-description)" : String,
    "[NotificationArns](#cfn-servicecatalog-launchnotificationconstraint-notificationarns)" : [ String, ... ],
    "[AcceptLanguage](#cfn-servicecatalog-launchnotificationconstraint-acceptlanguage)" : String,
    "[PortfolioId](#cfn-servicecatalog-launchnotificationconstraint-portfolioid)" : String,
    "[ProductId](#cfn-servicecatalog-launchnotificationconstraint-productid)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-launchnotificationconstraint-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::LaunchNotificationConstraint"
Properties:
  [Description](#cfn-servicecatalog-launchnotificationconstraint-description): String
  [NotificationArns](#cfn-servicecatalog-launchnotificationconstraint-notificationarns): 
    - String
  [AcceptLanguage](#cfn-servicecatalog-launchnotificationconstraint-acceptlanguage): String
  [PortfolioId](#cfn-servicecatalog-launchnotificationconstraint-portfolioid): String
  [ProductId](#cfn-servicecatalog-launchnotificationconstraint-productid): String
```

## Properties<a name="aws-resource-servicecatalog-launchnotificationconstraint-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-launchnotificationconstraint-acceptlanguage"></a>
The language code\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-servicecatalog-launchnotificationconstraint-description"></a>
The description of the constraint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NotificationArns`  <a name="cfn-servicecatalog-launchnotificationconstraint-notificationarns"></a>
The notification ARNs\.  
*Required*: Yes  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PortfolioId`  <a name="cfn-servicecatalog-launchnotificationconstraint-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ProductId`  <a name="cfn-servicecatalog-launchnotificationconstraint-productid"></a>
The product identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicecatalog-launchnotificationconstraint-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-launchnotificationconstraint-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::LaunchNotificationConstraint` resource to the intrinsic `Ref` function, the function returns the identifier of the constraint\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.