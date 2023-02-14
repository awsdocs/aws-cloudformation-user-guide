# AWS::LookoutMetrics::AnomalyDetector AppFlowConfig<a name="aws-properties-lookoutmetrics-anomalydetector-appflowconfig"></a>

Details about an Amazon AppFlow flow datasource\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-appflowconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-appflowconfig-syntax.json"></a>

```
{
  "[FlowName](#cfn-lookoutmetrics-anomalydetector-appflowconfig-flowname)" : String,
  "[RoleArn](#cfn-lookoutmetrics-anomalydetector-appflowconfig-rolearn)" : String
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-appflowconfig-syntax.yaml"></a>

```
  [FlowName](#cfn-lookoutmetrics-anomalydetector-appflowconfig-flowname): String
  [RoleArn](#cfn-lookoutmetrics-anomalydetector-appflowconfig-rolearn): String
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-appflowconfig-properties"></a>

`FlowName`  <a name="cfn-lookoutmetrics-anomalydetector-appflowconfig-flowname"></a>
 name of the flow\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-lookoutmetrics-anomalydetector-appflowconfig-rolearn"></a>
An IAM role that gives Amazon Lookout for Metrics permission to access the flow\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)