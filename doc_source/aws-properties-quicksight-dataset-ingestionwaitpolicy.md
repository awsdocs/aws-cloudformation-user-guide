# AWS::QuickSight::DataSet IngestionWaitPolicy<a name="aws-properties-quicksight-dataset-ingestionwaitpolicy"></a>

The wait policy to use when creating or updating a Dataset\. The default is to wait for SPICE ingestion to finish with timeout of 36 hours\.

## Syntax<a name="aws-properties-quicksight-dataset-ingestionwaitpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-ingestionwaitpolicy-syntax.json"></a>

```
{
  "[IngestionWaitTimeInHours](#cfn-quicksight-dataset-ingestionwaitpolicy-ingestionwaittimeinhours)" : Double,
  "[WaitForSpiceIngestion](#cfn-quicksight-dataset-ingestionwaitpolicy-waitforspiceingestion)" : Boolean
}
```

### YAML<a name="aws-properties-quicksight-dataset-ingestionwaitpolicy-syntax.yaml"></a>

```
  [IngestionWaitTimeInHours](#cfn-quicksight-dataset-ingestionwaitpolicy-ingestionwaittimeinhours): Double
  [WaitForSpiceIngestion](#cfn-quicksight-dataset-ingestionwaitpolicy-waitforspiceingestion): Boolean
```

## Properties<a name="aws-properties-quicksight-dataset-ingestionwaitpolicy-properties"></a>

`IngestionWaitTimeInHours`  <a name="cfn-quicksight-dataset-ingestionwaitpolicy-ingestionwaittimeinhours"></a>
The maximum time \(in hours\) to wait for Ingestion to complete\. Default timeout is 36 hours\. Applicable only when `DataSetImportMode` mode is set to SPICE and `WaitForSpiceIngestion` is set to true\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaitForSpiceIngestion`  <a name="cfn-quicksight-dataset-ingestionwaitpolicy-waitforspiceingestion"></a>
Wait for SPICE ingestion to finish to mark dataset creation or update as successful\. Default \(true\)\. Applicable only when `DataSetImportMode` mode is set to SPICE\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)