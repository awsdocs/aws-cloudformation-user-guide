# AWS::LookoutMetrics::AnomalyDetector VpcConfiguration<a name="aws-properties-lookoutmetrics-anomalydetector-vpcconfiguration"></a>

Contains configuration information about the Amazon Virtual Private Cloud \(VPC\)\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-vpcconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-vpcconfiguration-syntax.json"></a>

```
{
  "[SecurityGroupIdList](#cfn-lookoutmetrics-anomalydetector-vpcconfiguration-securitygroupidlist)" : [ String, ... ],
  "[SubnetIdList](#cfn-lookoutmetrics-anomalydetector-vpcconfiguration-subnetidlist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-vpcconfiguration-syntax.yaml"></a>

```
  [SecurityGroupIdList](#cfn-lookoutmetrics-anomalydetector-vpcconfiguration-securitygroupidlist): 
    - String
  [SubnetIdList](#cfn-lookoutmetrics-anomalydetector-vpcconfiguration-subnetidlist): 
    - String
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-vpcconfiguration-properties"></a>

`SecurityGroupIdList`  <a name="cfn-lookoutmetrics-anomalydetector-vpcconfiguration-securitygroupidlist"></a>
An array of strings containing the list of security groups\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIdList`  <a name="cfn-lookoutmetrics-anomalydetector-vpcconfiguration-subnetidlist"></a>
An array of strings containing the Amazon VPC subnet IDs \(e\.g\., `subnet-0bb1c79de3EXAMPLE`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)