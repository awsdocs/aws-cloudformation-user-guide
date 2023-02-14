# AWS::Evidently::Experiment OnlineAbConfigObject<a name="aws-properties-evidently-experiment-onlineabconfigobject"></a>

A structure that contains the configuration of which variation to use as the "control" version\. The "control" version is used for comparison with other variations\. This structure also specifies how much experiment traffic is allocated to each variation\.

## Syntax<a name="aws-properties-evidently-experiment-onlineabconfigobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-experiment-onlineabconfigobject-syntax.json"></a>

```
{
  "[ControlTreatmentName](#cfn-evidently-experiment-onlineabconfigobject-controltreatmentname)" : String,
  "[TreatmentWeights](#cfn-evidently-experiment-onlineabconfigobject-treatmentweights)" : [ TreatmentToWeight, ... ]
}
```

### YAML<a name="aws-properties-evidently-experiment-onlineabconfigobject-syntax.yaml"></a>

```
  [ControlTreatmentName](#cfn-evidently-experiment-onlineabconfigobject-controltreatmentname): String
  [TreatmentWeights](#cfn-evidently-experiment-onlineabconfigobject-treatmentweights): 
    - TreatmentToWeight
```

## Properties<a name="aws-properties-evidently-experiment-onlineabconfigobject-properties"></a>

`ControlTreatmentName`  <a name="cfn-evidently-experiment-onlineabconfigobject-controltreatmentname"></a>
The name of the variation that is to be the default variation that the other variations are compared to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreatmentWeights`  <a name="cfn-evidently-experiment-onlineabconfigobject-treatmentweights"></a>
A set of key\-value pairs\. The keys are treatment names, and the values are the portion of experiment traffic to be assigned to that treatment\. Specify the traffic portion in thousandths of a percent, so 20,000 for a variation would allocate 20% of the experiment traffic to that variation\.  
*Required*: No  
*Type*: List of [TreatmentToWeight](aws-properties-evidently-experiment-treatmenttoweight.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)