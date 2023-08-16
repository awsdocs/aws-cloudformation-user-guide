# AWS::SSMIncidents::ResponsePlan Integration<a name="aws-properties-ssmincidents-responseplan-integration"></a>

Information about third\-party services integrated into a response plan\.

## Syntax<a name="aws-properties-ssmincidents-responseplan-integration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmincidents-responseplan-integration-syntax.json"></a>

```
{
  "[PagerDutyConfiguration](#cfn-ssmincidents-responseplan-integration-pagerdutyconfiguration)" : PagerDutyConfiguration
}
```

### YAML<a name="aws-properties-ssmincidents-responseplan-integration-syntax.yaml"></a>

```
  [PagerDutyConfiguration](#cfn-ssmincidents-responseplan-integration-pagerdutyconfiguration): 
    PagerDutyConfiguration
```

## Properties<a name="aws-properties-ssmincidents-responseplan-integration-properties"></a>

`PagerDutyConfiguration`  <a name="cfn-ssmincidents-responseplan-integration-pagerdutyconfiguration"></a>
Information about the PagerDuty service where the response plan creates an incident\.  
*Required*: Yes  
*Type*: [PagerDutyConfiguration](aws-properties-ssmincidents-responseplan-pagerdutyconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)