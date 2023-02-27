# AWS::IoT::AccountAuditConfiguration AuditCheckConfigurations<a name="aws-properties-iot-accountauditconfiguration-auditcheckconfigurations"></a>

The types of audit checks that can be performed\.

## Syntax<a name="aws-properties-iot-accountauditconfiguration-auditcheckconfigurations-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-accountauditconfiguration-auditcheckconfigurations-syntax.json"></a>

```
{
  "[AuthenticatedCognitoRoleOverlyPermissiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-authenticatedcognitoroleoverlypermissivecheck)" : AuditCheckConfiguration,
  "[CaCertificateExpiringCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-cacertificateexpiringcheck)" : AuditCheckConfiguration,
  "[CaCertificateKeyQualityCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-cacertificatekeyqualitycheck)" : AuditCheckConfiguration,
  "[ConflictingClientIdsCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-conflictingclientidscheck)" : AuditCheckConfiguration,
  "[DeviceCertificateExpiringCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-devicecertificateexpiringcheck)" : AuditCheckConfiguration,
  "[DeviceCertificateKeyQualityCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-devicecertificatekeyqualitycheck)" : AuditCheckConfiguration,
  "[DeviceCertificateSharedCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-devicecertificatesharedcheck)" : AuditCheckConfiguration,
  "[IntermediateCaRevokedForActiveDeviceCertificatesCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-intermediatecarevokedforactivedevicecertificatescheck)" : AuditCheckConfiguration,
  "[IotPolicyOverlyPermissiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotpolicyoverlypermissivecheck)" : AuditCheckConfiguration,
  "[IoTPolicyPotentialMisConfigurationCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotpolicypotentialmisconfigurationcheck)" : AuditCheckConfiguration,
  "[IotRoleAliasAllowsAccessToUnusedServicesCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotrolealiasallowsaccesstounusedservicescheck)" : AuditCheckConfiguration,
  "[IotRoleAliasOverlyPermissiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotrolealiasoverlypermissivecheck)" : AuditCheckConfiguration,
  "[LoggingDisabledCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-loggingdisabledcheck)" : AuditCheckConfiguration,
  "[RevokedCaCertificateStillActiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-revokedcacertificatestillactivecheck)" : AuditCheckConfiguration,
  "[RevokedDeviceCertificateStillActiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-revokeddevicecertificatestillactivecheck)" : AuditCheckConfiguration,
  "[UnauthenticatedCognitoRoleOverlyPermissiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-unauthenticatedcognitoroleoverlypermissivecheck)" : AuditCheckConfiguration
}
```

### YAML<a name="aws-properties-iot-accountauditconfiguration-auditcheckconfigurations-syntax.yaml"></a>

```
  [AuthenticatedCognitoRoleOverlyPermissiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-authenticatedcognitoroleoverlypermissivecheck): 
    AuditCheckConfiguration
  [CaCertificateExpiringCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-cacertificateexpiringcheck): 
    AuditCheckConfiguration
  [CaCertificateKeyQualityCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-cacertificatekeyqualitycheck): 
    AuditCheckConfiguration
  [ConflictingClientIdsCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-conflictingclientidscheck): 
    AuditCheckConfiguration
  [DeviceCertificateExpiringCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-devicecertificateexpiringcheck): 
    AuditCheckConfiguration
  [DeviceCertificateKeyQualityCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-devicecertificatekeyqualitycheck): 
    AuditCheckConfiguration
  [DeviceCertificateSharedCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-devicecertificatesharedcheck): 
    AuditCheckConfiguration
  [IntermediateCaRevokedForActiveDeviceCertificatesCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-intermediatecarevokedforactivedevicecertificatescheck): 
    AuditCheckConfiguration
  [IotPolicyOverlyPermissiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotpolicyoverlypermissivecheck): 
    AuditCheckConfiguration
  [IoTPolicyPotentialMisConfigurationCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotpolicypotentialmisconfigurationcheck): 
    AuditCheckConfiguration
  [IotRoleAliasAllowsAccessToUnusedServicesCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotrolealiasallowsaccesstounusedservicescheck): 
    AuditCheckConfiguration
  [IotRoleAliasOverlyPermissiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotrolealiasoverlypermissivecheck): 
    AuditCheckConfiguration
  [LoggingDisabledCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-loggingdisabledcheck): 
    AuditCheckConfiguration
  [RevokedCaCertificateStillActiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-revokedcacertificatestillactivecheck): 
    AuditCheckConfiguration
  [RevokedDeviceCertificateStillActiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-revokeddevicecertificatestillactivecheck): 
    AuditCheckConfiguration
  [UnauthenticatedCognitoRoleOverlyPermissiveCheck](#cfn-iot-accountauditconfiguration-auditcheckconfigurations-unauthenticatedcognitoroleoverlypermissivecheck): 
    AuditCheckConfiguration
```

## Properties<a name="aws-properties-iot-accountauditconfiguration-auditcheckconfigurations-properties"></a>

`AuthenticatedCognitoRoleOverlyPermissiveCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-authenticatedcognitoroleoverlypermissivecheck"></a>
Checks the permissiveness of an authenticated Amazon Cognito identity pool role\. For this check, AWS IoT Device Defender audits all Amazon Cognito identity pools that have been used to connect to the AWS IoT message broker during the 31 days before the audit is performed\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaCertificateExpiringCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-cacertificateexpiringcheck"></a>
Checks if a CA certificate is expiring\. This check applies to CA certificates expiring within 30 days or that have expired\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaCertificateKeyQualityCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-cacertificatekeyqualitycheck"></a>
Checks the quality of the CA certificate key\. The quality checks if the key is in a valid format, not expired, and if the key meets a minimum required size\. This check applies to CA certificates that are `ACTIVE` or `PENDING_TRANSFER`\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConflictingClientIdsCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-conflictingclientidscheck"></a>
Checks if multiple devices connect using the same client ID\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceCertificateExpiringCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-devicecertificateexpiringcheck"></a>
Checks if a device certificate is expiring\. This check applies to device certificates expiring within 30 days or that have expired\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceCertificateKeyQualityCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-devicecertificatekeyqualitycheck"></a>
Checks the quality of the device certificate key\. The quality checks if the key is in a valid format, not expired, signed by a registered certificate authority, and if the key meets a minimum required size\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceCertificateSharedCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-devicecertificatesharedcheck"></a>
Checks if multiple concurrent connections use the same X\.509 certificate to authenticate with AWS IoT\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntermediateCaRevokedForActiveDeviceCertificatesCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-intermediatecarevokedforactivedevicecertificatescheck"></a>
  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotPolicyOverlyPermissiveCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotpolicyoverlypermissivecheck"></a>
Checks the permissiveness of a policy attached to an authenticated Amazon Cognito identity pool role\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IoTPolicyPotentialMisConfigurationCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotpolicypotentialmisconfigurationcheck"></a>
  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotRoleAliasAllowsAccessToUnusedServicesCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotrolealiasallowsaccesstounusedservicescheck"></a>
Checks if a role alias has access to services that haven't been used for the AWS IoT device in the last year\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotRoleAliasOverlyPermissiveCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-iotrolealiasoverlypermissivecheck"></a>
Checks if the temporary credentials provided by AWS IoT role aliases are overly permissive\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingDisabledCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-loggingdisabledcheck"></a>
Checks if AWS IoT logs are disabled\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RevokedCaCertificateStillActiveCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-revokedcacertificatestillactivecheck"></a>
Checks if a revoked CA certificate is still active\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RevokedDeviceCertificateStillActiveCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-revokeddevicecertificatestillactivecheck"></a>
Checks if a revoked device certificate is still active\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnauthenticatedCognitoRoleOverlyPermissiveCheck`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations-unauthenticatedcognitoroleoverlypermissivecheck"></a>
Checks if policy attached to an unauthenticated Amazon Cognito identity pool role is too permissive\.  
*Required*: No  
*Type*: [AuditCheckConfiguration](aws-properties-iot-accountauditconfiguration-auditcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)