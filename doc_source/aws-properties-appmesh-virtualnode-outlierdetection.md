# AWS::AppMesh::VirtualNode OutlierDetection<a name="aws-properties-appmesh-virtualnode-outlierdetection"></a>

An object that represents the outlier detection for a virtual node's listener\.

## Syntax<a name="aws-properties-appmesh-virtualnode-outlierdetection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-outlierdetection-syntax.json"></a>

```
{
  "[BaseEjectionDuration](#cfn-appmesh-virtualnode-outlierdetection-baseejectionduration)" : Duration,
  "[Interval](#cfn-appmesh-virtualnode-outlierdetection-interval)" : Duration,
  "[MaxEjectionPercent](#cfn-appmesh-virtualnode-outlierdetection-maxejectionpercent)" : Integer,
  "[MaxServerErrors](#cfn-appmesh-virtualnode-outlierdetection-maxservererrors)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-outlierdetection-syntax.yaml"></a>

```
  [BaseEjectionDuration](#cfn-appmesh-virtualnode-outlierdetection-baseejectionduration): 
    Duration
  [Interval](#cfn-appmesh-virtualnode-outlierdetection-interval): 
    Duration
  [MaxEjectionPercent](#cfn-appmesh-virtualnode-outlierdetection-maxejectionpercent): Integer
  [MaxServerErrors](#cfn-appmesh-virtualnode-outlierdetection-maxservererrors): Integer
```

## Properties<a name="aws-properties-appmesh-virtualnode-outlierdetection-properties"></a>

`BaseEjectionDuration`  <a name="cfn-appmesh-virtualnode-outlierdetection-baseejectionduration"></a>
The base amount of time for which a host is ejected\.  
*Required*: Yes  
*Type*: [Duration](aws-properties-appmesh-virtualnode-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Interval`  <a name="cfn-appmesh-virtualnode-outlierdetection-interval"></a>
The time interval between ejection sweep analysis\.  
*Required*: Yes  
*Type*: [Duration](aws-properties-appmesh-virtualnode-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxEjectionPercent`  <a name="cfn-appmesh-virtualnode-outlierdetection-maxejectionpercent"></a>
Maximum percentage of hosts in load balancing pool for upstream service that can be ejected\. Will eject at least one host regardless of the value\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxServerErrors`  <a name="cfn-appmesh-virtualnode-outlierdetection-maxservererrors"></a>
Number of consecutive `5xx` errors required for ejection\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)