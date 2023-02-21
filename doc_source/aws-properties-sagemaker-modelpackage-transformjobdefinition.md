# AWS::SageMaker::ModelPackage TransformJobDefinition<a name="aws-properties-sagemaker-modelpackage-transformjobdefinition"></a>

Defines the input needed to run a transform job using the inference specification specified in the algorithm\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-transformjobdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-transformjobdefinition-syntax.json"></a>

```
{
  "[BatchStrategy](#cfn-sagemaker-modelpackage-transformjobdefinition-batchstrategy)" : String,
  "[Environment](#cfn-sagemaker-modelpackage-transformjobdefinition-environment)" : {Key : Value, ...},
  "[MaxConcurrentTransforms](#cfn-sagemaker-modelpackage-transformjobdefinition-maxconcurrenttransforms)" : Integer,
  "[MaxPayloadInMB](#cfn-sagemaker-modelpackage-transformjobdefinition-maxpayloadinmb)" : Integer,
  "[TransformInput](#cfn-sagemaker-modelpackage-transformjobdefinition-transforminput)" : TransformInput,
  "[TransformOutput](#cfn-sagemaker-modelpackage-transformjobdefinition-transformoutput)" : TransformOutput,
  "[TransformResources](#cfn-sagemaker-modelpackage-transformjobdefinition-transformresources)" : TransformResources
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-transformjobdefinition-syntax.yaml"></a>

```
  [BatchStrategy](#cfn-sagemaker-modelpackage-transformjobdefinition-batchstrategy): String
  [Environment](#cfn-sagemaker-modelpackage-transformjobdefinition-environment): 
    Key : Value
  [MaxConcurrentTransforms](#cfn-sagemaker-modelpackage-transformjobdefinition-maxconcurrenttransforms): Integer
  [MaxPayloadInMB](#cfn-sagemaker-modelpackage-transformjobdefinition-maxpayloadinmb): Integer
  [TransformInput](#cfn-sagemaker-modelpackage-transformjobdefinition-transforminput): 
    TransformInput
  [TransformOutput](#cfn-sagemaker-modelpackage-transformjobdefinition-transformoutput): 
    TransformOutput
  [TransformResources](#cfn-sagemaker-modelpackage-transformjobdefinition-transformresources): 
    TransformResources
```

## Properties<a name="aws-properties-sagemaker-modelpackage-transformjobdefinition-properties"></a>

`BatchStrategy`  <a name="cfn-sagemaker-modelpackage-transformjobdefinition-batchstrategy"></a>
A string that determines the number of records included in a single mini\-batch\.  
 `SingleRecord` means only one record is used per mini\-batch\. `MultiRecord` means a mini\-batch is set to contain as many records that can fit within the `MaxPayloadInMB` limit\.  
*Required*: No  
*Type*: String  
*Allowed values*: `MultiRecord | SingleRecord`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Environment`  <a name="cfn-sagemaker-modelpackage-transformjobdefinition-environment"></a>
The environment variables to set in the Docker container\. We support up to 16 key and values entries in the map\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxConcurrentTransforms`  <a name="cfn-sagemaker-modelpackage-transformjobdefinition-maxconcurrenttransforms"></a>
The maximum number of parallel requests that can be sent to each instance in a transform job\. The default value is 1\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxPayloadInMB`  <a name="cfn-sagemaker-modelpackage-transformjobdefinition-maxpayloadinmb"></a>
The maximum payload size allowed, in MB\. A payload is the data portion of a record \(without metadata\)\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransformInput`  <a name="cfn-sagemaker-modelpackage-transformjobdefinition-transforminput"></a>
A description of the input source and the way the transform job consumes it\.  
*Required*: Yes  
*Type*: [TransformInput](aws-properties-sagemaker-modelpackage-transforminput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransformOutput`  <a name="cfn-sagemaker-modelpackage-transformjobdefinition-transformoutput"></a>
Identifies the Amazon S3 location where you want Amazon SageMaker to save the results from the transform job\.  
*Required*: Yes  
*Type*: [TransformOutput](aws-properties-sagemaker-modelpackage-transformoutput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransformResources`  <a name="cfn-sagemaker-modelpackage-transformjobdefinition-transformresources"></a>
Identifies the ML compute instances for the transform job\.  
*Required*: Yes  
*Type*: [TransformResources](aws-properties-sagemaker-modelpackage-transformresources.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)