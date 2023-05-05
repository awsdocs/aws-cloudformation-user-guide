# AWS::Connect::EvaluationForm ScoringStrategy<a name="aws-properties-connect-evaluationform-scoringstrategy"></a>

A scoring strategy of the evaluation form\.

## Syntax<a name="aws-properties-connect-evaluationform-scoringstrategy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-scoringstrategy-syntax.json"></a>

```
{
  "[Mode](#cfn-connect-evaluationform-scoringstrategy-mode)" : String,
  "[Status](#cfn-connect-evaluationform-scoringstrategy-status)" : String
}
```

### YAML<a name="aws-properties-connect-evaluationform-scoringstrategy-syntax.yaml"></a>

```
  [Mode](#cfn-connect-evaluationform-scoringstrategy-mode): String
  [Status](#cfn-connect-evaluationform-scoringstrategy-status): String
```

## Properties<a name="aws-properties-connect-evaluationform-scoringstrategy-properties"></a>

`Mode`  <a name="cfn-connect-evaluationform-scoringstrategy-mode"></a>
The scoring mode of the evaluation form\.  
*Allowed values*: `QUESTION_ONLY` \| `SECTION_ONLY`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-connect-evaluationform-scoringstrategy-status"></a>
The scoring status of the evaluation form\.  
*Allowed values*: `ENABLED` \| `DISABLED`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)