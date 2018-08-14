# AWS::ServiceCatalog::LaunchRoleConstraint<a name="aws-resource-servicecatalog-launchroleconstraint"></a>

Creates a launch constraint for AWS Service Catalog\. For more information, see [CreateConstraint](http://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateConstraint.html) in the *AWS Service Catalog Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-launchroleconstraint-syntax)
+ [Properties](#aws-resource-servicecatalog-launchroleconstraint-properties)
+ [Return Values](#aws-resource-servicecatalog-launchroleconstraint-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-launchroleconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-launchroleconstraint-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::LaunchRoleConstraint",
  "Properties" : {
    "[Description](#cfn-servicecatalog-launchroleconstraint-description)" : String,
    "[AcceptLanguage](#cfn-servicecatalog-launchroleconstraint-acceptlanguage)" : String,
    "[PortfolioId](#cfn-servicecatalog-launchroleconstraint-portfolioid)" : String,
    "[ProductId](#cfn-servicecatalog-launchroleconstraint-productid)" : String,
    "[RoleArn](#cfn-servicecatalog-launchroleconstraint-rolearn)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-launchroleconstraint-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::LaunchRoleConstraint"
Properties:
  [Description](#cfn-servicecatalog-launchroleconstraint-description): String
  [AcceptLanguage](#cfn-servicecatalog-launchroleconstraint-acceptlanguage): String
  [PortfolioId](#cfn-servicecatalog-launchroleconstraint-portfolioid): String
  [ProductId](#cfn-servicecatalog-launchroleconstraint-productid): String
  [RoleArn](#cfn-servicecatalog-launchroleconstraint-rolearn): String
```

## Properties<a name="aws-resource-servicecatalog-launchroleconstraint-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-launchroleconstraint-acceptlanguage"></a>
The language code\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-servicecatalog-launchroleconstraint-description"></a>
The description of the constraint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PortfolioId`  <a name="cfn-servicecatalog-launchroleconstraint-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ProductId`  <a name="cfn-servicecatalog-launchroleconstraint-productid"></a>
The product identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RoleArn`  <a name="cfn-servicecatalog-launchroleconstraint-rolearn"></a>
The ARN of the launch role\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicecatalog-launchroleconstraint-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-launchroleconstraint-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::LaunchRoleConstraint` resource to the intrinsic `Ref` function, the function returns the identifier of the constraint\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.