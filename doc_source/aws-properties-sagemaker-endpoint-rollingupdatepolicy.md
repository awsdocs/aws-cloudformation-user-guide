# AWS::SageMaker::Endpoint RollingUpdatePolicy<a name="aws-properties-sagemaker-endpoint-rollingupdatepolicy"></a>

Specifies a rolling deployment strategy for updating a SageMaker endpoint\.

## Syntax<a name="aws-properties-sagemaker-endpoint-rollingupdatepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpoint-rollingupdatepolicy-syntax.json"></a>

```
{
  "[MaximumBatchSize](#cfn-sagemaker-endpoint-rollingupdatepolicy-maximumbatchsize)" : CapacitySize,
  "[MaximumExecutionTimeoutInSeconds](#cfn-sagemaker-endpoint-rollingupdatepolicy-maximumexecutiontimeoutinseconds)" : Integer,
  "[RollbackMaximumBatchSize](#cfn-sagemaker-endpoint-rollingupdatepolicy-rollbackmaximumbatchsize)" : CapacitySize,
  "[WaitIntervalInSeconds](#cfn-sagemaker-endpoint-rollingupdatepolicy-waitintervalinseconds)" : Integer
}
```

### YAML<a name="aws-properties-sagemaker-endpoint-rollingupdatepolicy-syntax.yaml"></a>

```
  [MaximumBatchSize](#cfn-sagemaker-endpoint-rollingupdatepolicy-maximumbatchsize): 
    CapacitySize
  [MaximumExecutionTimeoutInSeconds](#cfn-sagemaker-endpoint-rollingupdatepolicy-maximumexecutiontimeoutinseconds): Integer
  [RollbackMaximumBatchSize](#cfn-sagemaker-endpoint-rollingupdatepolicy-rollbackmaximumbatchsize): 
    CapacitySize
  [WaitIntervalInSeconds](#cfn-sagemaker-endpoint-rollingupdatepolicy-waitintervalinseconds): Integer
```

## Properties<a name="aws-properties-sagemaker-endpoint-rollingupdatepolicy-properties"></a>

`MaximumBatchSize`  <a name="cfn-sagemaker-endpoint-rollingupdatepolicy-maximumbatchsize"></a>
Batch size for each rolling step to provision capacity and turn on traffic on the new endpoint fleet, and terminate capacity on the old endpoint fleet\. Value must be between 5% to 50% of the variant's total instance count\.  
*Required*: Yes  
*Type*: [CapacitySize](aws-properties-sagemaker-endpoint-capacitysize.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumExecutionTimeoutInSeconds`  <a name="cfn-sagemaker-endpoint-rollingupdatepolicy-maximumexecutiontimeoutinseconds"></a>
The time limit for the total deployment\. Exceeding this limit causes a timeout\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `600`  
*Maximum*: `28800`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RollbackMaximumBatchSize`  <a name="cfn-sagemaker-endpoint-rollingupdatepolicy-rollbackmaximumbatchsize"></a>
Batch size for rollback to the old endpoint fleet\. Each rolling step to provision capacity and turn on traffic on the old endpoint fleet, and terminate capacity on the new endpoint fleet\. If this field is absent, the default value will be set to 100% of total capacity which means to bring up the whole capacity of the old fleet at once during rollback\.  
*Required*: No  
*Type*: [CapacitySize](aws-properties-sagemaker-endpoint-capacitysize.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaitIntervalInSeconds`  <a name="cfn-sagemaker-endpoint-rollingupdatepolicy-waitintervalinseconds"></a>
The length of the baking period, during which SageMaker monitors alarms for each batch on the new fleet\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `3600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)