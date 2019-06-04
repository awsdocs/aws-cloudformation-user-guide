# AWS::OpsWorks::Layer Recipes<a name="aws-properties-opsworks-layer-recipes"></a>

AWS OpsWorks Stacks supports five lifecycle events: **setup**, **configuration**, **deploy**, **undeploy**, and **shutdown**\. For each layer, AWS OpsWorks Stacks runs a set of standard recipes for each event\. In addition, you can provide custom recipes for any or all layers and events\. AWS OpsWorks Stacks runs custom event recipes after the standard recipes\. `LayerCustomRecipes` specifies the custom recipes for a particular layer to be run in response to each of the five events\. 

To specify a recipe, use the cookbook's directory name in the repository followed by two colons and the recipe name, which is the recipe's file name without the \.rb extension\. For example: phpapp2::dbsetup specifies the dbsetup\.rb recipe in the repository's phpapp2 folder\.

## Syntax<a name="aws-properties-opsworks-layer-recipes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-layer-recipes-syntax.json"></a>

```
{
  "[Configure](#cfn-opsworks-layer-customrecipes-configure)" : [ String, ... ],
  "[Deploy](#cfn-opsworks-layer-customrecipes-deploy)" : [ String, ... ],
  "[Setup](#cfn-opsworks-layer-customrecipes-setup)" : [ String, ... ],
  "[Shutdown](#cfn-opsworks-layer-customrecipes-shutdown)" : [ String, ... ],
  "[Undeploy](#cfn-opsworks-layer-customrecipes-undeploy)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-opsworks-layer-recipes-syntax.yaml"></a>

```
  [Configure](#cfn-opsworks-layer-customrecipes-configure): 
    - String
  [Deploy](#cfn-opsworks-layer-customrecipes-deploy): 
    - String
  [Setup](#cfn-opsworks-layer-customrecipes-setup): 
    - String
  [Shutdown](#cfn-opsworks-layer-customrecipes-shutdown): 
    - String
  [Undeploy](#cfn-opsworks-layer-customrecipes-undeploy): 
    - String
```

## Properties<a name="aws-properties-opsworks-layer-recipes-properties"></a>

`Configure`  <a name="cfn-opsworks-layer-customrecipes-configure"></a>
An array of custom recipe names to be run following a `configure` event\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Deploy`  <a name="cfn-opsworks-layer-customrecipes-deploy"></a>
An array of custom recipe names to be run following a `deploy` event\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Setup`  <a name="cfn-opsworks-layer-customrecipes-setup"></a>
An array of custom recipe names to be run following a `setup` event\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Shutdown`  <a name="cfn-opsworks-layer-customrecipes-shutdown"></a>
An array of custom recipe names to be run following a `shutdown` event\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Undeploy`  <a name="cfn-opsworks-layer-customrecipes-undeploy"></a>
An array of custom recipe names to be run following a `undeploy` event\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)