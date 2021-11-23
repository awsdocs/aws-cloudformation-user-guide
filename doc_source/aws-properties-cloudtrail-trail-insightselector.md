# AWS::CloudTrail::Trail InsightSelector<a name="aws-properties-cloudtrail-trail-insightselector"></a>

A JSON string that contains a list of insight types that are logged on a trail\.

## Syntax<a name="aws-properties-cloudtrail-trail-insightselector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudtrail-trail-insightselector-syntax.json"></a>

```
{
  "[InsightType](#cfn-cloudtrail-trail-insightselector-insighttype)" : String
}
```

### YAML<a name="aws-properties-cloudtrail-trail-insightselector-syntax.yaml"></a>

```
  [InsightType](#cfn-cloudtrail-trail-insightselector-insighttype): String
```

## Properties<a name="aws-properties-cloudtrail-trail-insightselector-properties"></a>

`InsightType`  <a name="cfn-cloudtrail-trail-insightselector-insighttype"></a>
The type of Insights events to log on a trail\. The valid Insights type in this release is `ApiCallRateInsight`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ApiCallRateInsight | ApiErrorRateInsight`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)