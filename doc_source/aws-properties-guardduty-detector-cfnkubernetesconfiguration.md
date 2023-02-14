# AWS::GuardDuty::Detector CFNKubernetesConfiguration<a name="aws-properties-guardduty-detector-cfnkubernetesconfiguration"></a>

Describes which Kubernetes protection data sources are enabled for the detector\.

## Syntax<a name="aws-properties-guardduty-detector-cfnkubernetesconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-detector-cfnkubernetesconfiguration-syntax.json"></a>

```
{
  "[AuditLogs](#cfn-guardduty-detector-cfnkubernetesconfiguration-auditlogs)" : CFNKubernetesAuditLogsConfiguration
}
```

### YAML<a name="aws-properties-guardduty-detector-cfnkubernetesconfiguration-syntax.yaml"></a>

```
  [AuditLogs](#cfn-guardduty-detector-cfnkubernetesconfiguration-auditlogs): 
    CFNKubernetesAuditLogsConfiguration
```

## Properties<a name="aws-properties-guardduty-detector-cfnkubernetesconfiguration-properties"></a>

`AuditLogs`  <a name="cfn-guardduty-detector-cfnkubernetesconfiguration-auditlogs"></a>
Describes whether Kubernetes audit logs are enabled as a data source for the detector\.  
*Required*: No  
*Type*: [CFNKubernetesAuditLogsConfiguration](aws-properties-guardduty-detector-cfnkubernetesauditlogsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)