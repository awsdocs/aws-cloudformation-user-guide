# AWS::ServiceCatalog::ServiceAction<a name="aws-resource-servicecatalog-serviceaction"></a>

Creates a self\-service action\.

## Syntax<a name="aws-resource-servicecatalog-serviceaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-serviceaction-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::ServiceAction",
  "Properties" : {
      "[AcceptLanguage](#cfn-servicecatalog-serviceaction-acceptlanguage)" : String,
      "[Definition](#cfn-servicecatalog-serviceaction-definition)" : [ DefinitionParameter, ... ],
      "[DefinitionType](#cfn-servicecatalog-serviceaction-definitiontype)" : String,
      "[Description](#cfn-servicecatalog-serviceaction-description)" : String,
      "[Name](#cfn-servicecatalog-serviceaction-name)" : String
    }
}
```

### YAML<a name="aws-resource-servicecatalog-serviceaction-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::ServiceAction
Properties: 
  [AcceptLanguage](#cfn-servicecatalog-serviceaction-acceptlanguage): String
  [Definition](#cfn-servicecatalog-serviceaction-definition): 
    - DefinitionParameter
  [DefinitionType](#cfn-servicecatalog-serviceaction-definitiontype): String
  [Description](#cfn-servicecatalog-serviceaction-description): String
  [Name](#cfn-servicecatalog-serviceaction-name): String
```

## Properties<a name="aws-resource-servicecatalog-serviceaction-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-serviceaction-acceptlanguage"></a>
The language code\.  
+ `en` \- English \(default\)
+ `jp` \- Japanese
+ `zh` \- Chinese
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Definition`  <a name="cfn-servicecatalog-serviceaction-definition"></a>
A map that defines the self\-service action\.  
*Required*: Yes  
*Type*: List of [DefinitionParameter](aws-properties-servicecatalog-serviceaction-definitionparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefinitionType`  <a name="cfn-servicecatalog-serviceaction-definitiontype"></a>
The self\-service action definition type\. For example, `SSM_AUTOMATION`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SSM_AUTOMATION`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-servicecatalog-serviceaction-description"></a>
The self\-service action description\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-servicecatalog-serviceaction-name"></a>
The self\-service action name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9_\-.]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-servicecatalog-serviceaction-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-serviceaction-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-servicecatalog-serviceaction-return-values-fn--getatt"></a>

#### <a name="aws-resource-servicecatalog-serviceaction-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The self\-service action identifier\. For example, `act-fs7abcd89wxyz`\.