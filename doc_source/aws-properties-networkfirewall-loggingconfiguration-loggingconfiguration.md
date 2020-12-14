# AWS::NetworkFirewall::LoggingConfiguration LoggingConfiguration<a name="aws-properties-networkfirewall-loggingconfiguration-loggingconfiguration"></a>

Defines how AWS Network Firewall performs logging for a [AWS::NetworkFirewall::Firewall](aws-resource-networkfirewall-firewall.md)\. 

## Syntax<a name="aws-properties-networkfirewall-loggingconfiguration-loggingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-loggingconfiguration-loggingconfiguration-syntax.json"></a>

```
{
  "[LogDestinationConfigs](#cfn-networkfirewall-loggingconfiguration-loggingconfiguration-logdestinationconfigs)" : LogDestinationConfigs
}
```

### YAML<a name="aws-properties-networkfirewall-loggingconfiguration-loggingconfiguration-syntax.yaml"></a>

```
  [LogDestinationConfigs](#cfn-networkfirewall-loggingconfiguration-loggingconfiguration-logdestinationconfigs): 
    LogDestinationConfigs
```

## Properties<a name="aws-properties-networkfirewall-loggingconfiguration-loggingconfiguration-properties"></a>

`LogDestinationConfigs`  <a name="cfn-networkfirewall-loggingconfiguration-loggingconfiguration-logdestinationconfigs"></a>
Defines the logging destinations for the logs for a firewall\. Network Firewall generates logs for stateful rule groups\.   
*Required*: Yes  
*Type*: [LogDestinationConfigs](aws-properties-networkfirewall-loggingconfiguration-logdestinationconfigs.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)