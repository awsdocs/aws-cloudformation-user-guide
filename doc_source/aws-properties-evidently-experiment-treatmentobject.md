# AWS::Evidently::Experiment TreatmentObject<a name="aws-properties-evidently-experiment-treatmentobject"></a>

A structure that defines one treatment in an experiment\. A treatment is a variation of the feature that you are including in the experiment\.

## Syntax<a name="aws-properties-evidently-experiment-treatmentobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-experiment-treatmentobject-syntax.json"></a>

```
{
  "[Description](#cfn-evidently-experiment-treatmentobject-description)" : String,
  "[Feature](#cfn-evidently-experiment-treatmentobject-feature)" : String,
  "[TreatmentName](#cfn-evidently-experiment-treatmentobject-treatmentname)" : String,
  "[Variation](#cfn-evidently-experiment-treatmentobject-variation)" : String
}
```

### YAML<a name="aws-properties-evidently-experiment-treatmentobject-syntax.yaml"></a>

```
  [Description](#cfn-evidently-experiment-treatmentobject-description): String
  [Feature](#cfn-evidently-experiment-treatmentobject-feature): String
  [TreatmentName](#cfn-evidently-experiment-treatmentobject-treatmentname): String
  [Variation](#cfn-evidently-experiment-treatmentobject-variation): String
```

## Properties<a name="aws-properties-evidently-experiment-treatmentobject-properties"></a>

`Description`  <a name="cfn-evidently-experiment-treatmentobject-description"></a>
The description of the treatment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Feature`  <a name="cfn-evidently-experiment-treatmentobject-feature"></a>
The name of the feature for this experiment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreatmentName`  <a name="cfn-evidently-experiment-treatmentobject-treatmentname"></a>
A name for this treatment\. It can include up to 127 characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Variation`  <a name="cfn-evidently-experiment-treatmentobject-variation"></a>
The name of the variation to use for this treatment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)