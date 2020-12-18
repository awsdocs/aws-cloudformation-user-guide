# AWS::NetworkFirewall::LoggingConfiguration LogDestinationConfigs<a name="aws-properties-networkfirewall-loggingconfiguration-logdestinationconfigs"></a>

Defines the logging destinations for the logs for a firewall\. Network Firewall generates logs for stateful rule groups\. 

## Syntax<a name="aws-properties-networkfirewall-loggingconfiguration-logdestinationconfigs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-loggingconfiguration-logdestinationconfigs-syntax.json"></a>

```
{
  "[LogDestinationConfigs](#cfn-networkfirewall-loggingconfiguration-logdestinationconfigs-logdestinationconfigs)" : [ LogDestinationConfig, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-loggingconfiguration-logdestinationconfigs-syntax.yaml"></a>

```
  [LogDestinationConfigs](#cfn-networkfirewall-loggingconfiguration-logdestinationconfigs-logdestinationconfigs): 
    - LogDestinationConfig
```

## Properties<a name="aws-properties-networkfirewall-loggingconfiguration-logdestinationconfigs-properties"></a>

`LogDestinationConfigs`  <a name="cfn-networkfirewall-loggingconfiguration-logdestinationconfigs-logdestinationconfigs"></a>
Defines the logging destinations for the logs for a firewall\. Network Firewall generates logs for stateful rule groups\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-loggingconfiguration-logdestinationconfigs) of [LogDestinationConfig](aws-properties-networkfirewall-loggingconfiguration-logdestinationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)