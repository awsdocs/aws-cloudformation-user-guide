# AWS::ServiceCatalog::LaunchTemplateConstraint<a name="aws-resource-servicecatalog-launchtemplateconstraint"></a>

Specifies a template constraint\.

## Syntax<a name="aws-resource-servicecatalog-launchtemplateconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-launchtemplateconstraint-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::LaunchTemplateConstraint",
  "Properties" : {
      "[AcceptLanguage](#cfn-servicecatalog-launchtemplateconstraint-acceptlanguage)" : String,
      "[Description](#cfn-servicecatalog-launchtemplateconstraint-description)" : String,
      "[PortfolioId](#cfn-servicecatalog-launchtemplateconstraint-portfolioid)" : String,
      "[ProductId](#cfn-servicecatalog-launchtemplateconstraint-productid)" : String,
      "[Rules](#cfn-servicecatalog-launchtemplateconstraint-rules)" : String
    }
}
```

### YAML<a name="aws-resource-servicecatalog-launchtemplateconstraint-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::LaunchTemplateConstraint
Properties: 
  [AcceptLanguage](#cfn-servicecatalog-launchtemplateconstraint-acceptlanguage): String
  [Description](#cfn-servicecatalog-launchtemplateconstraint-description): String
  [PortfolioId](#cfn-servicecatalog-launchtemplateconstraint-portfolioid): String
  [ProductId](#cfn-servicecatalog-launchtemplateconstraint-productid): String
  [Rules](#cfn-servicecatalog-launchtemplateconstraint-rules): String
```

## Properties<a name="aws-resource-servicecatalog-launchtemplateconstraint-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-launchtemplateconstraint-acceptlanguage"></a>
The language code\.  
+  `en` \- English \(default\)
+  `jp` \- Japanese
+  `zh` \- Chinese
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-servicecatalog-launchtemplateconstraint-description"></a>
The description of the constraint\.  
*Required*: No  
*Type*: String  
*Maximum*: `2000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortfolioId`  <a name="cfn-servicecatalog-launchtemplateconstraint-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProductId`  <a name="cfn-servicecatalog-launchtemplateconstraint-productid"></a>
The product identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Rules`  <a name="cfn-servicecatalog-launchtemplateconstraint-rules"></a>
The constraint rules\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-servicecatalog-launchtemplateconstraint-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-launchtemplateconstraint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the identifier of the constraint\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Remarks<a name="aws-resource-servicecatalog-launchtemplateconstraint--remarks"></a>

 *Using AWS CloudFormation constraint rules* 

Administrators can create and apply rules to create template contraints in an AWS Service Catalog portfolio\. The rules prevent end users from entering incorrect values in the AWS CloudFormation template the administrator used to create the product\. 

For more information about template constraint rules and how to create them, see [Template Constraint Rules](https://docs.aws.amazon.com/servicecatalog/latest/adminguide/reference-template_constraint_rules.html) in the *AWS Service Catalog Admin Guide*\. 

## See also<a name="aws-resource-servicecatalog-launchtemplateconstraint--seealso"></a>
+ [CreateConstraint](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateConstraint.html) in the *AWS Service Catalog API Reference*

