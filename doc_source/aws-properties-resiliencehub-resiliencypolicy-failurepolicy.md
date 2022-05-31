# AWS::ResilienceHub::ResiliencyPolicy FailurePolicy<a name="aws-properties-resiliencehub-resiliencypolicy-failurepolicy"></a>

Defines a failure policy\.

## Syntax<a name="aws-properties-resiliencehub-resiliencypolicy-failurepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-resiliencehub-resiliencypolicy-failurepolicy-syntax.json"></a>

```
{
  "[RpoInSecs](#cfn-resiliencehub-resiliencypolicy-failurepolicy-rpoinsecs)" : Integer,
  "[RtoInSecs](#cfn-resiliencehub-resiliencypolicy-failurepolicy-rtoinsecs)" : Integer
}
```

### YAML<a name="aws-properties-resiliencehub-resiliencypolicy-failurepolicy-syntax.yaml"></a>

```
  [RpoInSecs](#cfn-resiliencehub-resiliencypolicy-failurepolicy-rpoinsecs): Integer
  [RtoInSecs](#cfn-resiliencehub-resiliencypolicy-failurepolicy-rtoinsecs): Integer
```

## Properties<a name="aws-properties-resiliencehub-resiliencypolicy-failurepolicy-properties"></a>

`RpoInSecs`  <a name="cfn-resiliencehub-resiliencypolicy-failurepolicy-rpoinsecs"></a>
The Recovery Point Objective \(RPO\), in seconds\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RtoInSecs`  <a name="cfn-resiliencehub-resiliencypolicy-failurepolicy-rtoinsecs"></a>
The Recovery Time Objective \(RTO\), in seconds\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)