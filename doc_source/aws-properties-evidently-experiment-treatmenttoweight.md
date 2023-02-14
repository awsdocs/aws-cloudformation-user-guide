# AWS::Evidently::Experiment TreatmentToWeight<a name="aws-properties-evidently-experiment-treatmenttoweight"></a>

This structure defines how much experiment traffic to allocate to one treatment used in the experiment\.

## Syntax<a name="aws-properties-evidently-experiment-treatmenttoweight-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-experiment-treatmenttoweight-syntax.json"></a>

```
{
  "[SplitWeight](#cfn-evidently-experiment-treatmenttoweight-splitweight)" : Integer,
  "[Treatment](#cfn-evidently-experiment-treatmenttoweight-treatment)" : String
}
```

### YAML<a name="aws-properties-evidently-experiment-treatmenttoweight-syntax.yaml"></a>

```
  [SplitWeight](#cfn-evidently-experiment-treatmenttoweight-splitweight): Integer
  [Treatment](#cfn-evidently-experiment-treatmenttoweight-treatment): String
```

## Properties<a name="aws-properties-evidently-experiment-treatmenttoweight-properties"></a>

`SplitWeight`  <a name="cfn-evidently-experiment-treatmenttoweight-splitweight"></a>
The portion of experiment traffic to allocate to this treatment\. Specify the traffic portion in thousandths of a percent, so 20,000 allocated to a treatment would allocate 20% of the experiment traffic to that treatment\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Treatment`  <a name="cfn-evidently-experiment-treatmenttoweight-treatment"></a>
The name of the treatment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)