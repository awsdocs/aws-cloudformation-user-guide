# AWS::Connect::EvaluationForm EvaluationFormBaseItem<a name="aws-properties-connect-evaluationform-evaluationformbaseitem"></a>

An item at the root level\. All items must be sections\.

## Syntax<a name="aws-properties-connect-evaluationform-evaluationformbaseitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-evaluationformbaseitem-syntax.json"></a>

```
{
  "[Section](#cfn-connect-evaluationform-evaluationformbaseitem-section)" : EvaluationFormSection
}
```

### YAML<a name="aws-properties-connect-evaluationform-evaluationformbaseitem-syntax.yaml"></a>

```
  [Section](#cfn-connect-evaluationform-evaluationformbaseitem-section): 
    EvaluationFormSection
```

## Properties<a name="aws-properties-connect-evaluationform-evaluationformbaseitem-properties"></a>

`Section`  <a name="cfn-connect-evaluationform-evaluationformbaseitem-section"></a>
A subsection or inner section of an item\.  
*Required*: Yes  
*Type*: [EvaluationFormSection](aws-properties-connect-evaluationform-evaluationformsection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)