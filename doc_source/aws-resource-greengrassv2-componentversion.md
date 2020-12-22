# AWS::GreengrassV2::ComponentVersion<a name="aws-resource-greengrassv2-componentversion"></a>

Creates a component\. Components are software that run on Greengrass core devices\. After you develop and test a component on your core device, you can use this operation to upload your component to AWS IoT Greengrass\. Then, you can deploy the component to other core devices\.

You can use this operation to do the following:
+ **Create components from recipes**

  Create a component from a recipe, which is a file that defines the component's metadata, parameters, dependencies, lifecycle, artifacts, and platform capability\. For more information, see [AWS IoT Greengrass component recipe reference](https://docs.aws.amazon.com/greengrass/v2/developerguide/component-recipe-reference.html) in the *AWS IoT Greengrass V2 Developer Guide*\.

  To create a component from a recipe, specify `inlineRecipe` when you call this operation\.
+ **Create components from Lambda functions**

  Create a component from an AWS Lambda function that runs on AWS IoT Greengrass\. This creates a recipe and artifacts from the Lambda function's deployment package\. You can use this operation to migrate Lambda functions from AWS IoT Greengrass V1 to AWS IoT Greengrass V2\.

  This function only accepts Lambda functions that use the following runtimes:
  + Python 2\.7 – `python2.7`
  + Python 3\.7 – `python3.7`
  + Python 3\.8 – `python3.8`
  + Java 8 – `java8`
  + Node\.js 10 – `nodejs10.x`
  + Node\.js 12 – `nodejs12.x`

  To create a component from a Lambda function, specify `lambdaFunction` when you call this operation\.

## Syntax<a name="aws-resource-greengrassv2-componentversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrassv2-componentversion-syntax.json"></a>

```
{
  "Type" : "AWS::GreengrassV2::ComponentVersion",
  "Properties" : {
      "[InlineRecipe](#cfn-greengrassv2-componentversion-inlinerecipe)" : String,
      "[LambdaFunction](#cfn-greengrassv2-componentversion-lambdafunction)" : LambdaFunctionRecipeSource,
      "[Tags](#cfn-greengrassv2-componentversion-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-greengrassv2-componentversion-syntax.yaml"></a>

```
Type: AWS::GreengrassV2::ComponentVersion
Properties: 
  [InlineRecipe](#cfn-greengrassv2-componentversion-inlinerecipe): String
  [LambdaFunction](#cfn-greengrassv2-componentversion-lambdafunction): 
    LambdaFunctionRecipeSource
  [Tags](#cfn-greengrassv2-componentversion-tags): 
    Key : Value
```

## Properties<a name="aws-resource-greengrassv2-componentversion-properties"></a>

`InlineRecipe`  <a name="cfn-greengrassv2-componentversion-inlinerecipe"></a>
The recipe to use to create the component\. The recipe defines the component's metadata, parameters, dependencies, lifecycle, artifacts, and platform compatibility\.  
You must specify either `InlineRecipe` or `LambdaFunction`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LambdaFunction`  <a name="cfn-greengrassv2-componentversion-lambdafunction"></a>
The parameters to create a component from a Lambda function\.  
You must specify either `InlineRecipe` or `LambdaFunction`\.  
*Required*: No  
*Type*: [LambdaFunctionRecipeSource](aws-properties-greengrassv2-componentversion-lambdafunctionrecipesource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-greengrassv2-componentversion-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-greengrassv2-componentversion-return-values"></a>

### Ref<a name="aws-resource-greengrassv2-componentversion-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `Arn`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-greengrassv2-componentversion-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-greengrassv2-componentversion-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the component version\.

`ComponentName`  <a name="ComponentName-fn::getatt"></a>
The name of the component\.

`ComponentVersion`  <a name="ComponentVersion-fn::getatt"></a>
The version of the component\.