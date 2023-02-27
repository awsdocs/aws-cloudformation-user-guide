# AWS::SageMaker::NotebookInstance InstanceMetadataServiceConfiguration<a name="aws-properties-sagemaker-notebookinstance-instancemetadataserviceconfiguration"></a>

Information on the IMDS configuration of the notebook instance

## Syntax<a name="aws-properties-sagemaker-notebookinstance-instancemetadataserviceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-notebookinstance-instancemetadataserviceconfiguration-syntax.json"></a>

```
{
  "[MinimumInstanceMetadataServiceVersion](#cfn-sagemaker-notebookinstance-instancemetadataserviceconfiguration-minimuminstancemetadataserviceversion)" : String
}
```

### YAML<a name="aws-properties-sagemaker-notebookinstance-instancemetadataserviceconfiguration-syntax.yaml"></a>

```
  [MinimumInstanceMetadataServiceVersion](#cfn-sagemaker-notebookinstance-instancemetadataserviceconfiguration-minimuminstancemetadataserviceversion): String
```

## Properties<a name="aws-properties-sagemaker-notebookinstance-instancemetadataserviceconfiguration-properties"></a>

`MinimumInstanceMetadataServiceVersion`  <a name="cfn-sagemaker-notebookinstance-instancemetadataserviceconfiguration-minimuminstancemetadataserviceversion"></a>
Indicates the minimum IMDS version that the notebook instance supports\. When passed as part of `CreateNotebookInstance`, if no value is selected, then it defaults to IMDSv1\. This means that both IMDSv1 and IMDSv2 are supported\. If passed as part of `UpdateNotebookInstance`, there is no default\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1`  
*Pattern*: `1|2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)