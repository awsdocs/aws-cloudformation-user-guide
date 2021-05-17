# AWS::LookoutMetrics::AnomalyDetector SubnetIdList<a name="aws-properties-lookoutmetrics-anomalydetector-subnetidlist"></a>

An array of strings containing the Amazon VPC subnet IDs \(e\.g\., `subnet-0bb1c79de3EXAMPLE`\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-subnetidlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-subnetidlist-syntax.json"></a>

```
{
  "[SubnetIdList](#cfn-lookoutmetrics-anomalydetector-subnetidlist-subnetidlist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-subnetidlist-syntax.yaml"></a>

```
  [SubnetIdList](#cfn-lookoutmetrics-anomalydetector-subnetidlist-subnetidlist): 
    - String
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-subnetidlist-properties"></a>

`SubnetIdList`  <a name="cfn-lookoutmetrics-anomalydetector-subnetidlist-subnetidlist"></a>
An array of strings containing the Amazon VPC subnet IDs \(e\.g\., `subnet-0bb1c79de3EXAMPLE`\.  
*Required*: No  
*Type*: [List](#aws-properties-lookoutmetrics-anomalydetector-subnetidlist) of [String](#aws-properties-lookoutmetrics-anomalydetector-subnetidlist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)