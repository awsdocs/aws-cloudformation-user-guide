# AWS::Connect::EvaluationForm<a name="aws-resource-connect-evaluationform"></a>

Creates an evaluation form for the specified Amazon Connect instance\.

## Syntax<a name="aws-resource-connect-evaluationform-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-evaluationform-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::EvaluationForm",
  "Properties" : {
      "[Description](#cfn-connect-evaluationform-description)" : String,
      "[InstanceArn](#cfn-connect-evaluationform-instancearn)" : String,
      "[Items](#cfn-connect-evaluationform-items)" : [ EvaluationFormBaseItem, ... ],
      "[ScoringStrategy](#cfn-connect-evaluationform-scoringstrategy)" : ScoringStrategy,
      "[Status](#cfn-connect-evaluationform-status)" : String,
      "[Tags](#cfn-connect-evaluationform-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Title](#cfn-connect-evaluationform-title)" : String
    }
}
```

### YAML<a name="aws-resource-connect-evaluationform-syntax.yaml"></a>

```
Type: AWS::Connect::EvaluationForm
Properties: 
  [Description](#cfn-connect-evaluationform-description): String
  [InstanceArn](#cfn-connect-evaluationform-instancearn): String
  [Items](#cfn-connect-evaluationform-items): 
    - EvaluationFormBaseItem
  [ScoringStrategy](#cfn-connect-evaluationform-scoringstrategy): 
    ScoringStrategy
  [Status](#cfn-connect-evaluationform-status): String
  [Tags](#cfn-connect-evaluationform-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Title](#cfn-connect-evaluationform-title): String
```

## Properties<a name="aws-resource-connect-evaluationform-properties"></a>

`Description`  <a name="cfn-connect-evaluationform-description"></a>
The description of the evaluation form\.  
*Length Constraints*: Minimum length of 0\. Maximum length of 1024\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-connect-evaluationform-instancearn"></a>
The identifier of the Amazon Connect instance\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Items`  <a name="cfn-connect-evaluationform-items"></a>
Items that are part of the evaluation form\. The total number of sections and questions must not exceed 100 each\. Questions must be contained in a section\.  
*Minimum size*: 1  
*Maximum size*: 100  
*Required*: Yes  
*Type*: List of [EvaluationFormBaseItem](aws-properties-connect-evaluationform-evaluationformbaseitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScoringStrategy`  <a name="cfn-connect-evaluationform-scoringstrategy"></a>
A scoring strategy of the evaluation form\.  
*Required*: No  
*Type*: [ScoringStrategy](aws-properties-connect-evaluationform-scoringstrategy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-connect-evaluationform-status"></a>
The status of the evaluation form\.  
*Allowed values*: `DRAFT` \| `ACTIVE`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-connect-evaluationform-tags"></a>
The tags used to organize, track, or control access for this resource\. For example, \{ "tags": \{"key1":"value1", "key2":"value2"\} \}\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-connect-evaluationform-title"></a>
A title of the evaluation form\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-connect-evaluationform-return-values"></a>

### Ref<a name="aws-resource-connect-evaluationform-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the evaluation form name\. For example:

`{ "Ref": "myEvaluationFormName" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-connect-evaluationform-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-connect-evaluationform-return-values-fn--getatt-fn--getatt"></a>

`EvaluationFormArn`  <a name="EvaluationFormArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the evaluation form\.