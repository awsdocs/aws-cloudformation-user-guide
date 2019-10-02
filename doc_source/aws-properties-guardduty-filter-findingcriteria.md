# AWS::GuardDuty::Filter FindingCriteria<a name="aws-properties-guardduty-filter-findingcriteria"></a>

Represents a map of finding properties that match specified conditions and values when querying findings\.

## Syntax<a name="aws-properties-guardduty-filter-findingcriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-filter-findingcriteria-syntax.json"></a>

```
{
  "[Criterion](#cfn-guardduty-filter-findingcriteria-criterion)" : Json,
  "[ItemType](#cfn-guardduty-filter-findingcriteria-itemtype)" : [Condition](aws-properties-guardduty-filter-condition.md)
}
```

### YAML<a name="aws-properties-guardduty-filter-findingcriteria-syntax.yaml"></a>

```
  [Criterion](#cfn-guardduty-filter-findingcriteria-criterion): Json
  [ItemType](#cfn-guardduty-filter-findingcriteria-itemtype): 
    [Condition](aws-properties-guardduty-filter-condition.md)
```

## Properties<a name="aws-properties-guardduty-filter-findingcriteria-properties"></a>

`Criterion`  <a name="cfn-guardduty-filter-findingcriteria-criterion"></a>
Represents a map of finding properties that match specified conditions and values when querying findings\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ItemType`  <a name="cfn-guardduty-filter-findingcriteria-itemtype"></a>
Specifies the condition to be applied to a single field when filtering through findings\.  
*Required*: No  
*Type*: [Condition](aws-properties-guardduty-filter-condition.md)  
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
