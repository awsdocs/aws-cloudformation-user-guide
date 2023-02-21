# AWS::SSMIncidents::ResponsePlan DynamicSsmParameter<a name="aws-properties-ssmincidents-responseplan-dynamicssmparameter"></a>

When you add a runbook to a response plan, you can specify the parameters the runbook should use at runtime\. Response plans support parameters with both static and dynamic values\. For static values, you enter the value when you define the parameter in the response plan\. For dynamic values, the system determines the correct parameter value by collecting information from the incident\. Incident Manager supports the following dynamic parameters:

**Incident ARN**

When Incident Manager creates an incident, the system captures the Amazon Resource Name \(ARN\) of the corresponding incident record and enters it for this parameter in the runbook\.

**Note**  
This value can only be assigned to parameters of type `String`\. If assigned to a parameter of any other type, the runbook fails to run\. 

**Involved resources**

When Incident Manager creates an incident, the system captures the ARNs of the resources involved in the incident\. These resource ARNs are then assigned to this parameter in the runbook\. 

**Note**  
This value can only be assigned to parameters of type `StringList`\. If assigned to a parameter of any other type, the runbook fails to run\.

## Syntax<a name="aws-properties-ssmincidents-responseplan-dynamicssmparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmincidents-responseplan-dynamicssmparameter-syntax.json"></a>

```
{
  "[Key](#cfn-ssmincidents-responseplan-dynamicssmparameter-key)" : String,
  "[Value](#cfn-ssmincidents-responseplan-dynamicssmparameter-value)" : DynamicSsmParameterValue
}
```

### YAML<a name="aws-properties-ssmincidents-responseplan-dynamicssmparameter-syntax.yaml"></a>

```
  [Key](#cfn-ssmincidents-responseplan-dynamicssmparameter-key): String
  [Value](#cfn-ssmincidents-responseplan-dynamicssmparameter-value): 
    DynamicSsmParameterValue
```

## Properties<a name="aws-properties-ssmincidents-responseplan-dynamicssmparameter-properties"></a>

`Key`  <a name="cfn-ssmincidents-responseplan-dynamicssmparameter-key"></a>
The key parameter to use when running the Systems Manager Automation runbook\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-ssmincidents-responseplan-dynamicssmparameter-value"></a>
The dynamic parameter value\.  
*Required*: Yes  
*Type*: [DynamicSsmParameterValue](aws-properties-ssmincidents-responseplan-dynamicssmparametervalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)