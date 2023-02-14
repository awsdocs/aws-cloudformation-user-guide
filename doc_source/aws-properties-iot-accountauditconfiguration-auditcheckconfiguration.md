# AWS::IoT::AccountAuditConfiguration AuditCheckConfiguration<a name="aws-properties-iot-accountauditconfiguration-auditcheckconfiguration"></a>

Which audit checks are enabled and disabled for this account\.

## Syntax<a name="aws-properties-iot-accountauditconfiguration-auditcheckconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-accountauditconfiguration-auditcheckconfiguration-syntax.json"></a>

```
{
  "[Enabled](#cfn-iot-accountauditconfiguration-auditcheckconfiguration-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-iot-accountauditconfiguration-auditcheckconfiguration-syntax.yaml"></a>

```
  [Enabled](#cfn-iot-accountauditconfiguration-auditcheckconfiguration-enabled): Boolean
```

## Properties<a name="aws-properties-iot-accountauditconfiguration-auditcheckconfiguration-properties"></a>

`Enabled`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfiguration-enabled"></a>
True if this audit check is enabled for this account\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)