# AWS::SageMaker::ModelExplainabilityJobDefinition MonitoringResources<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-monitoringresources"></a>

Identifies the resources to deploy for a monitoring job\.

## Syntax<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-monitoringresources-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-monitoringresources-syntax.json"></a>

```
{
  "[ClusterConfig](#cfn-sagemaker-modelexplainabilityjobdefinition-monitoringresources-clusterconfig)" : ClusterConfig
}
```

### YAML<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-monitoringresources-syntax.yaml"></a>

```
  [ClusterConfig](#cfn-sagemaker-modelexplainabilityjobdefinition-monitoringresources-clusterconfig): 
    ClusterConfig
```

## Properties<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-monitoringresources-properties"></a>

`ClusterConfig`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-monitoringresources-clusterconfig"></a>
The configuration for the cluster resources used to run the processing job\.  
*Required*: Yes  
*Type*: [ClusterConfig](aws-properties-sagemaker-modelexplainabilityjobdefinition-clusterconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)