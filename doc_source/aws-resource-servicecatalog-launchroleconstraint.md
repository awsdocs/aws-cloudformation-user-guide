# AWS::ServiceCatalog::LaunchRoleConstraint<a name="aws-resource-servicecatalog-launchroleconstraint"></a>

Specifies a launch constraint\.

## Syntax<a name="aws-resource-servicecatalog-launchroleconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-launchroleconstraint-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::LaunchRoleConstraint",
  "Properties" : {
      "[AcceptLanguage](#cfn-servicecatalog-launchroleconstraint-acceptlanguage)" : String,
      "[Description](#cfn-servicecatalog-launchroleconstraint-description)" : String,
      "[PortfolioId](#cfn-servicecatalog-launchroleconstraint-portfolioid)" : String,
      "[ProductId](#cfn-servicecatalog-launchroleconstraint-productid)" : String,
      "[RoleArn](#cfn-servicecatalog-launchroleconstraint-rolearn)" : String
    }
}
```

### YAML<a name="aws-resource-servicecatalog-launchroleconstraint-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::LaunchRoleConstraint
Properties: 
  [AcceptLanguage](#cfn-servicecatalog-launchroleconstraint-acceptlanguage): String
  [Description](#cfn-servicecatalog-launchroleconstraint-description): String
  [PortfolioId](#cfn-servicecatalog-launchroleconstraint-portfolioid): String
  [ProductId](#cfn-servicecatalog-launchroleconstraint-productid): String
  [RoleArn](#cfn-servicecatalog-launchroleconstraint-rolearn): String
```

## Properties<a name="aws-resource-servicecatalog-launchroleconstraint-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-launchroleconstraint-acceptlanguage"></a>
The language code\.  
+  `en` \- English \(default\)
+  `jp` \- Japanese
+  `zh` \- Chinese
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-servicecatalog-launchroleconstraint-description"></a>
The description of the constraint\.  
*Required*: No  
*Type*: String  
*Maximum*: `2000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortfolioId`  <a name="cfn-servicecatalog-launchroleconstraint-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProductId`  <a name="cfn-servicecatalog-launchroleconstraint-productid"></a>
The product identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-servicecatalog-launchroleconstraint-rolearn"></a>
The ARN of the launch role\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-servicecatalog-launchroleconstraint-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-launchroleconstraint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns identifier of the constraint\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-resource-servicecatalog-launchroleconstraint--seealso"></a>
+ [CreateConstraint](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateConstraint.html) in the *AWS Service Catalog API Reference*