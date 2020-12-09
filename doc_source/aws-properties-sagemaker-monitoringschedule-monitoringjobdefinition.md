# AWS::SageMaker::MonitoringSchedule MonitoringJobDefinition<a name="aws-properties-sagemaker-monitoringschedule-monitoringjobdefinition"></a>

Defines the monitoring job\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-monitoringjobdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-monitoringjobdefinition-syntax.json"></a>

```
{
  "[BaselineConfig](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-baselineconfig)" : BaselineConfig,
  "[Environment](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-environment)" : Environment,
  "[MonitoringAppSpecification](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringappspecification)" : MonitoringAppSpecification,
  "[MonitoringInputs](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringinputs)" : MonitoringInputs,
  "[MonitoringOutputConfig](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringoutputconfig)" : MonitoringOutputConfig,
  "[MonitoringResources](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringresources)" : MonitoringResources,
  "[NetworkConfig](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-networkconfig)" : NetworkConfig,
  "[RoleArn](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-rolearn)" : String,
  "[StoppingCondition](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-stoppingcondition)" : StoppingCondition
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-monitoringjobdefinition-syntax.yaml"></a>

```
  [BaselineConfig](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-baselineconfig): 
    BaselineConfig
  [Environment](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-environment): 
    Environment
  [MonitoringAppSpecification](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringappspecification): 
    MonitoringAppSpecification
  [MonitoringInputs](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringinputs): 
    MonitoringInputs
  [MonitoringOutputConfig](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringoutputconfig): 
    MonitoringOutputConfig
  [MonitoringResources](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringresources): 
    MonitoringResources
  [NetworkConfig](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-networkconfig): 
    NetworkConfig
  [RoleArn](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-rolearn): String
  [StoppingCondition](#cfn-sagemaker-monitoringschedule-monitoringjobdefinition-stoppingcondition): 
    StoppingCondition
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-monitoringjobdefinition-properties"></a>

`BaselineConfig`  <a name="cfn-sagemaker-monitoringschedule-monitoringjobdefinition-baselineconfig"></a>
Baseline configuration used to validate that the data conforms to the specified constraints and statistics  
*Required*: No  
*Type*: [BaselineConfig](aws-properties-sagemaker-monitoringschedule-baselineconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Environment`  <a name="cfn-sagemaker-monitoringschedule-monitoringjobdefinition-environment"></a>
Sets the environment variables in the Docker container\.  
*Required*: No  
*Type*: [Environment](aws-properties-sagemaker-monitoringschedule-environment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringAppSpecification`  <a name="cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringappspecification"></a>
Configures the monitoring job to run a specified Docker container image\.  
*Required*: Yes  
*Type*: [MonitoringAppSpecification](aws-properties-sagemaker-monitoringschedule-monitoringappspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringInputs`  <a name="cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringinputs"></a>
The array of inputs for the monitoring job\. Currently we support monitoring an Amazon SageMaker Endpoint\.  
*Required*: Yes  
*Type*: [MonitoringInputs](aws-properties-sagemaker-monitoringschedule-monitoringinputs.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringOutputConfig`  <a name="cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringoutputconfig"></a>
The array of outputs from the monitoring job to be uploaded to Amazon Simple Storage Service \(Amazon S3\)\.  
*Required*: Yes  
*Type*: [MonitoringOutputConfig](aws-properties-sagemaker-monitoringschedule-monitoringoutputconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringResources`  <a name="cfn-sagemaker-monitoringschedule-monitoringjobdefinition-monitoringresources"></a>
Identifies the resources, ML compute instances, and ML storage volumes to deploy for a monitoring job\. In distributed processing, you specify more than one instance\.  
*Required*: Yes  
*Type*: [MonitoringResources](aws-properties-sagemaker-monitoringschedule-monitoringresources.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkConfig`  <a name="cfn-sagemaker-monitoringschedule-monitoringjobdefinition-networkconfig"></a>
Specifies networking options for an monitoring job\.  
*Required*: No  
*Type*: [NetworkConfig](aws-properties-sagemaker-monitoringschedule-networkconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-sagemaker-monitoringschedule-monitoringjobdefinition-rolearn"></a>
The Amazon Resource Name \(ARN\) of an IAM role that Amazon SageMaker can assume to perform tasks on your behalf\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StoppingCondition`  <a name="cfn-sagemaker-monitoringschedule-monitoringjobdefinition-stoppingcondition"></a>
Specifies a time limit for how long the monitoring job is allowed to run\.  
*Required*: No  
*Type*: [StoppingCondition](aws-properties-sagemaker-monitoringschedule-stoppingcondition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)