# AWS::Config::ConfigRule EvaluationModeConfiguration<a name="aws-properties-config-configrule-evaluationmodeconfiguration"></a>

The configuration object for AWS Config rule evaluation mode\. The supported valid values are Detective or Proactive\.

## Syntax<a name="aws-properties-config-configrule-evaluationmodeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configrule-evaluationmodeconfiguration-syntax.json"></a>

```
{
  "[Mode](#cfn-config-configrule-evaluationmodeconfiguration-mode)" : String
}
```

### YAML<a name="aws-properties-config-configrule-evaluationmodeconfiguration-syntax.yaml"></a>

```
  [Mode](#cfn-config-configrule-evaluationmodeconfiguration-mode): String
```

## Properties<a name="aws-properties-config-configrule-evaluationmodeconfiguration-properties"></a>

`Mode`  <a name="cfn-config-configrule-evaluationmodeconfiguration-mode"></a>
The mode of an evaluation\. The valid values are Detective or Proactive\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DETECTIVE | PROACTIVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)