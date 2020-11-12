# AWS::SageMaker::MonitoringSchedule MonitoringResources<a name="aws-properties-sagemaker-monitoringschedule-monitoringresources"></a>

Identifies the resources to deploy for a monitoring job\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-monitoringresources-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-monitoringresources-syntax.json"></a>

```
{
  "[ClusterConfig](#cfn-sagemaker-monitoringschedule-monitoringresources-clusterconfig)" : ClusterConfig
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-monitoringresources-syntax.yaml"></a>

```
  [ClusterConfig](#cfn-sagemaker-monitoringschedule-monitoringresources-clusterconfig): 
    ClusterConfig
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-monitoringresources-properties"></a>

`ClusterConfig`  <a name="cfn-sagemaker-monitoringschedule-monitoringresources-clusterconfig"></a>
The configuration for the cluster resources used to run the processing job\.  
*Required*: Yes  
*Type*: [ClusterConfig](aws-properties-sagemaker-monitoringschedule-clusterconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)