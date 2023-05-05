# AWS::Connect::EvaluationForm EvaluationFormSection<a name="aws-properties-connect-evaluationform-evaluationformsection"></a>

Information about a section from an evaluation form\. A section can contain sections and/or questions\. Evaluation forms can only contain sections and subsections \(two level nesting\)\.

## Syntax<a name="aws-properties-connect-evaluationform-evaluationformsection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-evaluationformsection-syntax.json"></a>

```
{
  "[Instructions](#cfn-connect-evaluationform-evaluationformsection-instructions)" : String,
  "[Items](#cfn-connect-evaluationform-evaluationformsection-items)" : [ EvaluationFormItem, ... ],
  "[RefId](#cfn-connect-evaluationform-evaluationformsection-refid)" : String,
  "[Title](#cfn-connect-evaluationform-evaluationformsection-title)" : String,
  "[Weight](#cfn-connect-evaluationform-evaluationformsection-weight)" : Double
}
```

### YAML<a name="aws-properties-connect-evaluationform-evaluationformsection-syntax.yaml"></a>

```
  [Instructions](#cfn-connect-evaluationform-evaluationformsection-instructions): String
  [Items](#cfn-connect-evaluationform-evaluationformsection-items): 
    - EvaluationFormItem
  [RefId](#cfn-connect-evaluationform-evaluationformsection-refid): String
  [Title](#cfn-connect-evaluationform-evaluationformsection-title): String
  [Weight](#cfn-connect-evaluationform-evaluationformsection-weight): Double
```

## Properties<a name="aws-properties-connect-evaluationform-evaluationformsection-properties"></a>

`Instructions`  <a name="cfn-connect-evaluationform-evaluationformsection-instructions"></a>
The instructions of the section\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Items`  <a name="cfn-connect-evaluationform-evaluationformsection-items"></a>
The items of the section\.  
*Minimum*: 1  
*Required*: No  
*Type*: List of [EvaluationFormItem](aws-properties-connect-evaluationform-evaluationformitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefId`  <a name="cfn-connect-evaluationform-evaluationformsection-refid"></a>
The identifier of the section\. An identifier must be unique within the evaluation form\.  
*Length Constraints*: Minimum length of 1\. Maximum length of 40\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-connect-evaluationform-evaluationformsection-title"></a>
The title of the section\.  
*Length Constraints*: Minimum length of 1\. Maximum length of 128\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-connect-evaluationform-evaluationformsection-weight"></a>
The scoring weight of the section\.  
*Minimum*: 0   
*Maximum*: 100  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)