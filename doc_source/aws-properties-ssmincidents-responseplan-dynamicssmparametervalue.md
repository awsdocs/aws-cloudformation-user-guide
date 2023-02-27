# AWS::SSMIncidents::ResponsePlan DynamicSsmParameterValue<a name="aws-properties-ssmincidents-responseplan-dynamicssmparametervalue"></a>

The dynamic parameter value\.

## Syntax<a name="aws-properties-ssmincidents-responseplan-dynamicssmparametervalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmincidents-responseplan-dynamicssmparametervalue-syntax.json"></a>

```
{
  "[Variable](#cfn-ssmincidents-responseplan-dynamicssmparametervalue-variable)" : String
}
```

### YAML<a name="aws-properties-ssmincidents-responseplan-dynamicssmparametervalue-syntax.yaml"></a>

```
  [Variable](#cfn-ssmincidents-responseplan-dynamicssmparametervalue-variable): String
```

## Properties<a name="aws-properties-ssmincidents-responseplan-dynamicssmparametervalue-properties"></a>

`Variable`  <a name="cfn-ssmincidents-responseplan-dynamicssmparametervalue-variable"></a>
Variable dynamic parameters\. A parameter value is determined when an incident is created\.  
*Required*: No  
*Type*: String  
*Allowed values*: `INCIDENT_RECORD_ARN | INVOLVED_RESOURCES`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)