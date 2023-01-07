# AWS::SSMIncidents::ResponsePlan Action<a name="aws-properties-ssmincidents-responseplan-action"></a>

The `Action` property type specifies the configuration to launch\.

## Syntax<a name="aws-properties-ssmincidents-responseplan-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmincidents-responseplan-action-syntax.json"></a>

```
{
  "[SsmAutomation](#cfn-ssmincidents-responseplan-action-ssmautomation)" : SsmAutomation
}
```

### YAML<a name="aws-properties-ssmincidents-responseplan-action-syntax.yaml"></a>

```
  [SsmAutomation](#cfn-ssmincidents-responseplan-action-ssmautomation): 
    SsmAutomation
```

## Properties<a name="aws-properties-ssmincidents-responseplan-action-properties"></a>

`SsmAutomation`  <a name="cfn-ssmincidents-responseplan-action-ssmautomation"></a>
Details about the Systems Manager automation document that will be used as a runbook during an incident\.  
*Required*: No  
*Type*: [SsmAutomation](aws-properties-ssmincidents-responseplan-ssmautomation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)