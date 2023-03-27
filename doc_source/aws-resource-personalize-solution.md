# AWS::Personalize::Solution<a name="aws-resource-personalize-solution"></a>

An object that provides information about a solution\. A solution is a trained model that can be deployed as a campaign\.

## Syntax<a name="aws-resource-personalize-solution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-personalize-solution-syntax.json"></a>

```
{
  "Type" : "AWS::Personalize::Solution",
  "Properties" : {
      "[DatasetGroupArn](#cfn-personalize-solution-datasetgrouparn)" : String,
      "[EventType](#cfn-personalize-solution-eventtype)" : String,
      "[Name](#cfn-personalize-solution-name)" : String,
      "[PerformAutoML](#cfn-personalize-solution-performautoml)" : Boolean,
      "[PerformHPO](#cfn-personalize-solution-performhpo)" : Boolean,
      "[RecipeArn](#cfn-personalize-solution-recipearn)" : String,
      "[SolutionConfig](#cfn-personalize-solution-solutionconfig)" : SolutionConfig
    }
}
```

### YAML<a name="aws-resource-personalize-solution-syntax.yaml"></a>

```
Type: AWS::Personalize::Solution
Properties: 
  [DatasetGroupArn](#cfn-personalize-solution-datasetgrouparn): String
  [EventType](#cfn-personalize-solution-eventtype): String
  [Name](#cfn-personalize-solution-name): String
  [PerformAutoML](#cfn-personalize-solution-performautoml): Boolean
  [PerformHPO](#cfn-personalize-solution-performhpo): Boolean
  [RecipeArn](#cfn-personalize-solution-recipearn): String
  [SolutionConfig](#cfn-personalize-solution-solutionconfig): 
    SolutionConfig
```

## Properties<a name="aws-resource-personalize-solution-properties"></a>

`DatasetGroupArn`  <a name="cfn-personalize-solution-datasetgrouparn"></a>
The Amazon Resource Name \(ARN\) of the dataset group that provides the training data\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `arn:([a-z\d-]+):personalize:.*:.*:.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EventType`  <a name="cfn-personalize-solution-eventtype"></a>
The event type \(for example, 'click' or 'like'\) that is used for training the model\. If no `eventType` is provided, Amazon Personalize uses all interactions for training with equal weight regardless of type\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-personalize-solution-name"></a>
The name of the solution\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\-_]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PerformAutoML`  <a name="cfn-personalize-solution-performautoml"></a>
We don't recommend enabling automated machine learning\. Instead, match your use case to the available Amazon Personalize recipes\. For more information, see [Determining your use case\.](https://docs.aws.amazon.com/personalize/latest/dg/determining-use-case.html) 
When true, Amazon Personalize performs a search for the best USER\_PERSONALIZATION recipe from the list specified in the solution configuration \(`recipeArn` must not be specified\)\. When false \(the default\), Amazon Personalize uses `recipeArn` for training\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PerformHPO`  <a name="cfn-personalize-solution-performhpo"></a>
Whether to perform hyperparameter optimization \(HPO\) on the chosen recipe\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RecipeArn`  <a name="cfn-personalize-solution-recipearn"></a>
The ARN of the recipe used to create the solution\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `arn:([a-z\d-]+):personalize:.*:.*:.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SolutionConfig`  <a name="cfn-personalize-solution-solutionconfig"></a>
Describes the configuration properties for the solution\.  
*Required*: No  
*Type*: [SolutionConfig](aws-properties-personalize-solution-solutionconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-personalize-solution-return-values"></a>

### Ref<a name="aws-resource-personalize-solution-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the resource\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-personalize-solution-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-personalize-solution-return-values-fn--getatt-fn--getatt"></a>

`SolutionArn`  <a name="SolutionArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the solution\.