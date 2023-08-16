# AWS::IoT::DomainConfiguration TlsConfig<a name="aws-properties-iot-domainconfiguration-tlsconfig"></a>

An object that specifies the TLS configuration for a domain\.

## Syntax<a name="aws-properties-iot-domainconfiguration-tlsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-domainconfiguration-tlsconfig-syntax.json"></a>

```
{
  "[SecurityPolicy](#cfn-iot-domainconfiguration-tlsconfig-securitypolicy)" : String
}
```

### YAML<a name="aws-properties-iot-domainconfiguration-tlsconfig-syntax.yaml"></a>

```
  [SecurityPolicy](#cfn-iot-domainconfiguration-tlsconfig-securitypolicy): String
```

## Properties<a name="aws-properties-iot-domainconfiguration-tlsconfig-properties"></a>

`SecurityPolicy`  <a name="cfn-iot-domainconfiguration-tlsconfig-securitypolicy"></a>
The security policy for a domain configuration\. For more information, see [Security policies ](https://docs.aws.amazon.com/iot/latest/developerguide/transport-security.html#tls-policy-table) in the *AWS IoT Core developer guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)