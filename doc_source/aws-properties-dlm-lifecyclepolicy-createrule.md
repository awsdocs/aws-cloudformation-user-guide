# AWS::DLM::LifecyclePolicy CreateRule<a name="aws-properties-dlm-lifecyclepolicy-createrule"></a>

Specifies when to create snapshots of EBS volumes\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax.json"></a>

```
{
  "[Interval](#cfn-dlm-lifecyclepolicy-createrule-interval)" : Integer,
  "[IntervalUnit](#cfn-dlm-lifecyclepolicy-createrule-intervalunit)" : String,
  "[Times](#cfn-dlm-lifecyclepolicy-createrule-times)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax.yaml"></a>

```
  [Interval](#cfn-dlm-lifecyclepolicy-createrule-interval): Integer
  [IntervalUnit](#cfn-dlm-lifecyclepolicy-createrule-intervalunit): String
  [Times](#cfn-dlm-lifecyclepolicy-createrule-times): 
    - String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-createrule-properties"></a>

`Interval`  <a name="cfn-dlm-lifecyclepolicy-createrule-interval"></a>
The interval between snapshots\. The supported values are 2, 3, 4, 6, 8, 12, and 24\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntervalUnit`  <a name="cfn-dlm-lifecyclepolicy-createrule-intervalunit"></a>
The interval unit\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `HOURS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Times`  <a name="cfn-dlm-lifecyclepolicy-createrule-times"></a>
The time, in UTC, to start the operation\. The supported format is hh:mm\.  
The operation occurs within a one\-hour window following the specified time\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
