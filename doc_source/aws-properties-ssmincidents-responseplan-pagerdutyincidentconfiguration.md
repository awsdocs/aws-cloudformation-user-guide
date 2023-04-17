# AWS::SSMIncidents::ResponsePlan PagerDutyIncidentConfiguration<a name="aws-properties-ssmincidents-responseplan-pagerdutyincidentconfiguration"></a>

Details about the PagerDuty service where the response plan creates an incident\.

## Syntax<a name="aws-properties-ssmincidents-responseplan-pagerdutyincidentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmincidents-responseplan-pagerdutyincidentconfiguration-syntax.json"></a>

```
{
  "[ServiceId](#cfn-ssmincidents-responseplan-pagerdutyincidentconfiguration-serviceid)" : String
}
```

### YAML<a name="aws-properties-ssmincidents-responseplan-pagerdutyincidentconfiguration-syntax.yaml"></a>

```
  [ServiceId](#cfn-ssmincidents-responseplan-pagerdutyincidentconfiguration-serviceid): String
```

## Properties<a name="aws-properties-ssmincidents-responseplan-pagerdutyincidentconfiguration-properties"></a>

`ServiceId`  <a name="cfn-ssmincidents-responseplan-pagerdutyincidentconfiguration-serviceid"></a>
The ID of the PagerDuty service that the response plan associates with an incident when it launches\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)