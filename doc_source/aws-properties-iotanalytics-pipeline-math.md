# AWS::IoTAnalytics::Pipeline Math<a name="aws-properties-iotanalytics-pipeline-math"></a>

An activity that computes an arithmetic expression using the message's attributes\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-math-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-math-syntax.json"></a>

```
{
  "[Attribute](#cfn-iotanalytics-pipeline-math-attribute)" : String,
  "[Math](#cfn-iotanalytics-pipeline-math-math)" : String,
  "[Name](#cfn-iotanalytics-pipeline-math-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-math-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-math-syntax.yaml"></a>

```
  [Attribute](#cfn-iotanalytics-pipeline-math-attribute): String
  [Math](#cfn-iotanalytics-pipeline-math-math): String
  [Name](#cfn-iotanalytics-pipeline-math-name): String
  [Next](#cfn-iotanalytics-pipeline-math-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-math-properties"></a>

`Attribute`  <a name="cfn-iotanalytics-pipeline-math-attribute"></a>
The name of the attribute that contains the result of the math operation\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Math`  <a name="cfn-iotanalytics-pipeline-math-math"></a>
An expression that uses one or more existing attributes and must return an integer value\.  
*Required*: No  
*Type*: [String](#aws-properties-iotanalytics-pipeline-math)  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotanalytics-pipeline-math-name"></a>
The name of the 'math' activity\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Next`  <a name="cfn-iotanalytics-pipeline-math-next"></a>
The next activity in the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)