# AWS::DataBrew::Recipe<a name="aws-resource-databrew-recipe"></a>

Creates a new DataBrew recipe\.

## Syntax<a name="aws-resource-databrew-recipe-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-databrew-recipe-syntax.json"></a>

```
{
  "Type" : "AWS::DataBrew::Recipe",
  "Properties" : {
      "[Description](#cfn-databrew-recipe-description)" : String,
      "[Name](#cfn-databrew-recipe-name)" : String,
      "[ProjectName](#cfn-databrew-recipe-projectname)" : String,
      "[Steps](#cfn-databrew-recipe-steps)" : [ RecipeStep, ... ],
      "[Tags](#cfn-databrew-recipe-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Version](#cfn-databrew-recipe-version)" : String
    }
}
```

### YAML<a name="aws-resource-databrew-recipe-syntax.yaml"></a>

```
Type: AWS::DataBrew::Recipe
Properties: 
  [Description](#cfn-databrew-recipe-description): String
  [Name](#cfn-databrew-recipe-name): String
  [ProjectName](#cfn-databrew-recipe-projectname): String
  [Steps](#cfn-databrew-recipe-steps): 
    - RecipeStep
  [Tags](#cfn-databrew-recipe-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Version](#cfn-databrew-recipe-version): String
```

## Properties<a name="aws-resource-databrew-recipe-properties"></a>

`Description`  <a name="cfn-databrew-recipe-description"></a>
The description of the recipe\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-databrew-recipe-name"></a>
The unique name for the recipe\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProjectName`  <a name="cfn-databrew-recipe-projectname"></a>
The name of the project that the recipe is associated with\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Steps`  <a name="cfn-databrew-recipe-steps"></a>
A list of steps that are defined by the recipe\.  
*Required*: Yes  
*Type*: List of [RecipeStep](aws-properties-databrew-recipe-recipestep.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-databrew-recipe-tags"></a>
Metadata tags that have been applied to the recipe\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-databrew-recipe-version"></a>
The identifier for a particular version of the recipe\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-databrew-recipe-return-values"></a>

### Ref<a name="aws-resource-databrew-recipe-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myDataset" }` 

For the AWS Glue DataBrew dataset `myDataset`, `Ref` returns the name of the dataset\.