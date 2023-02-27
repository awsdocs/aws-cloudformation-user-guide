# AWS::GuardDuty::Detector CFNDataSourceConfigurations<a name="aws-properties-guardduty-detector-cfndatasourceconfigurations"></a>

Describes whether S3 data event logs, Kubernetes audit logs, or Malware Protection will be enabled as a data source when the detector is created\.

## Syntax<a name="aws-properties-guardduty-detector-cfndatasourceconfigurations-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-detector-cfndatasourceconfigurations-syntax.json"></a>

```
{
  "[Kubernetes](#cfn-guardduty-detector-cfndatasourceconfigurations-kubernetes)" : CFNKubernetesConfiguration,
  "[MalwareProtection](#cfn-guardduty-detector-cfndatasourceconfigurations-malwareprotection)" : CFNMalwareProtectionConfiguration,
  "[S3Logs](#cfn-guardduty-detector-cfndatasourceconfigurations-s3logs)" : CFNS3LogsConfiguration
}
```

### YAML<a name="aws-properties-guardduty-detector-cfndatasourceconfigurations-syntax.yaml"></a>

```
  [Kubernetes](#cfn-guardduty-detector-cfndatasourceconfigurations-kubernetes): 
    CFNKubernetesConfiguration
  [MalwareProtection](#cfn-guardduty-detector-cfndatasourceconfigurations-malwareprotection): 
    CFNMalwareProtectionConfiguration
  [S3Logs](#cfn-guardduty-detector-cfndatasourceconfigurations-s3logs): 
    CFNS3LogsConfiguration
```

## Properties<a name="aws-properties-guardduty-detector-cfndatasourceconfigurations-properties"></a>

`Kubernetes`  <a name="cfn-guardduty-detector-cfndatasourceconfigurations-kubernetes"></a>
Describes which Kuberentes data sources are enabled for a detector\.  
*Required*: No  
*Type*: [CFNKubernetesConfiguration](aws-properties-guardduty-detector-cfnkubernetesconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MalwareProtection`  <a name="cfn-guardduty-detector-cfndatasourceconfigurations-malwareprotection"></a>
Describes whether Malware Protection will be enabled as a data source\.  
*Required*: No  
*Type*: [CFNMalwareProtectionConfiguration](aws-properties-guardduty-detector-cfnmalwareprotectionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Logs`  <a name="cfn-guardduty-detector-cfndatasourceconfigurations-s3logs"></a>
Describes whether S3 data event logs are enabled as a data source\.  
*Required*: No  
*Type*: [CFNS3LogsConfiguration](aws-properties-guardduty-detector-cfns3logsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)