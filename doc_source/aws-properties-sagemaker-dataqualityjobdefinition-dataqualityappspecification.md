# AWS::SageMaker::DataQualityJobDefinition DataQualityAppSpecification<a name="aws-properties-sagemaker-dataqualityjobdefinition-dataqualityappspecification"></a>

Information about the container that a data quality monitoring job runs\.

## Syntax<a name="aws-properties-sagemaker-dataqualityjobdefinition-dataqualityappspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-dataqualityjobdefinition-dataqualityappspecification-syntax.json"></a>

```
{
  "[ContainerArguments](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-containerarguments)" : [ String, ... ],
  "[ContainerEntrypoint](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-containerentrypoint)" : [ String, ... ],
  "[Environment](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-environment)" : {Key : Value, ...},
  "[ImageUri](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-imageuri)" : String,
  "[PostAnalyticsProcessorSourceUri](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-postanalyticsprocessorsourceuri)" : String,
  "[RecordPreprocessorSourceUri](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-recordpreprocessorsourceuri)" : String
}
```

### YAML<a name="aws-properties-sagemaker-dataqualityjobdefinition-dataqualityappspecification-syntax.yaml"></a>

```
  [ContainerArguments](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-containerarguments): 
    - String
  [ContainerEntrypoint](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-containerentrypoint): 
    - String
  [Environment](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-environment): 
    Key : Value
  [ImageUri](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-imageuri): String
  [PostAnalyticsProcessorSourceUri](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-postanalyticsprocessorsourceuri): String
  [RecordPreprocessorSourceUri](#cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-recordpreprocessorsourceuri): String
```

## Properties<a name="aws-properties-sagemaker-dataqualityjobdefinition-dataqualityappspecification-properties"></a>

`ContainerArguments`  <a name="cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-containerarguments"></a>
The arguments to send to the container that the monitoring job runs\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContainerEntrypoint`  <a name="cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-containerentrypoint"></a>
The entrypoint for a container used to run a monitoring job\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Environment`  <a name="cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-environment"></a>
Sets the environment variables in the container that the monitoring job runs\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageUri`  <a name="cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-imageuri"></a>
The container image that the data quality monitoring job runs\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PostAnalyticsProcessorSourceUri`  <a name="cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-postanalyticsprocessorsourceuri"></a>
An Amazon S3 URI to a script that is called after analysis has been performed\. Applicable only for the built\-in \(first party\) containers\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RecordPreprocessorSourceUri`  <a name="cfn-sagemaker-dataqualityjobdefinition-dataqualityappspecification-recordpreprocessorsourceuri"></a>
An Amazon S3 URI to a script that is called per row prior to running analysis\. It can base64 decode the payload and convert it into a flatted json so that the built\-in container can use the converted data\. Applicable only for the built\-in \(first party\) containers\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)