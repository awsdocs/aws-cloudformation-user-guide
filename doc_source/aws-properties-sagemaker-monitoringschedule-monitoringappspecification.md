# AWS::SageMaker::MonitoringSchedule MonitoringAppSpecification<a name="aws-properties-sagemaker-monitoringschedule-monitoringappspecification"></a>

Container image configuration object for the monitoring job\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-monitoringappspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-monitoringappspecification-syntax.json"></a>

```
{
  "[ContainerArguments](#cfn-sagemaker-monitoringschedule-monitoringappspecification-containerarguments)" : [ String, ... ],
  "[ContainerEntrypoint](#cfn-sagemaker-monitoringschedule-monitoringappspecification-containerentrypoint)" : [ String, ... ],
  "[ImageUri](#cfn-sagemaker-monitoringschedule-monitoringappspecification-imageuri)" : String,
  "[PostAnalyticsProcessorSourceUri](#cfn-sagemaker-monitoringschedule-monitoringappspecification-postanalyticsprocessorsourceuri)" : String,
  "[RecordPreprocessorSourceUri](#cfn-sagemaker-monitoringschedule-monitoringappspecification-recordpreprocessorsourceuri)" : String
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-monitoringappspecification-syntax.yaml"></a>

```
  [ContainerArguments](#cfn-sagemaker-monitoringschedule-monitoringappspecification-containerarguments): 
    - String
  [ContainerEntrypoint](#cfn-sagemaker-monitoringschedule-monitoringappspecification-containerentrypoint): 
    - String
  [ImageUri](#cfn-sagemaker-monitoringschedule-monitoringappspecification-imageuri): String
  [PostAnalyticsProcessorSourceUri](#cfn-sagemaker-monitoringschedule-monitoringappspecification-postanalyticsprocessorsourceuri): String
  [RecordPreprocessorSourceUri](#cfn-sagemaker-monitoringschedule-monitoringappspecification-recordpreprocessorsourceuri): String
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-monitoringappspecification-properties"></a>

`ContainerArguments`  <a name="cfn-sagemaker-monitoringschedule-monitoringappspecification-containerarguments"></a>
An array of arguments for the container used to run the monitoring job\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContainerEntrypoint`  <a name="cfn-sagemaker-monitoringschedule-monitoringappspecification-containerentrypoint"></a>
Specifies the entrypoint for a container used to run the monitoring job\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageUri`  <a name="cfn-sagemaker-monitoringschedule-monitoringappspecification-imageuri"></a>
The container image to be run by the monitoring job\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PostAnalyticsProcessorSourceUri`  <a name="cfn-sagemaker-monitoringschedule-monitoringappspecification-postanalyticsprocessorsourceuri"></a>
An Amazon S3 URI to a script that is called after analysis has been performed\. Applicable only for the built\-in \(first party\) containers\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordPreprocessorSourceUri`  <a name="cfn-sagemaker-monitoringschedule-monitoringappspecification-recordpreprocessorsourceuri"></a>
An Amazon S3 URI to a script that is called per row prior to running analysis\. It can base64 decode the payload and convert it into a flatted json so that the built\-in container can use the converted data\. Applicable only for the built\-in \(first party\) containers\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)