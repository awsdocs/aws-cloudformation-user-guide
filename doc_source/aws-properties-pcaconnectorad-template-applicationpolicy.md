# AWS::PCAConnectorAD::Template ApplicationPolicy<a name="aws-properties-pcaconnectorad-template-applicationpolicy"></a>

Application policies describe what the certificate can be used for\.

## Syntax<a name="aws-properties-pcaconnectorad-template-applicationpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-applicationpolicy-syntax.json"></a>

```
{
  "[PolicyObjectIdentifier](#cfn-pcaconnectorad-template-applicationpolicy-policyobjectidentifier)" : String,
  "[PolicyType](#cfn-pcaconnectorad-template-applicationpolicy-policytype)" : String
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-applicationpolicy-syntax.yaml"></a>

```
  [PolicyObjectIdentifier](#cfn-pcaconnectorad-template-applicationpolicy-policyobjectidentifier): String
  [PolicyType](#cfn-pcaconnectorad-template-applicationpolicy-policytype): String
```

## Properties<a name="aws-properties-pcaconnectorad-template-applicationpolicy-properties"></a>

`PolicyObjectIdentifier`  <a name="cfn-pcaconnectorad-template-applicationpolicy-policyobjectidentifier"></a>
The object identifier \(OID\) of an application policy\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `([0-2])\.([0-9]|([0-3][0-9]))(\.([0-9]+)){0,126}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyType`  <a name="cfn-pcaconnectorad-template-applicationpolicy-policytype"></a>
The type of application policy  
*Required*: No  
*Type*: String  
*Allowed values*: `ALL_APPLICATION_POLICIES | ANY_PURPOSE | ATTESTATION_IDENTITY_KEY_CERTIFICATE | CERTIFICATE_REQUEST_AGENT | CLIENT_AUTHENTICATION | CODE_SIGNING | CTL_USAGE | DIGITAL_RIGHTS | DIRECTORY_SERVICE_EMAIL_REPLICATION | DISALLOWED_LIST | DNS_SERVER_TRUST | DOCUMENT_ENCRYPTION | DOCUMENT_SIGNING | DYNAMIC_CODE_GENERATOR | EARLY_LAUNCH_ANTIMALWARE_DRIVER | EMBEDDED_WINDOWS_SYSTEM_COMPONENT_VERIFICATION | ENCLAVE | ENCRYPTING_FILE_SYSTEM | ENDORSEMENT_KEY_CERTIFICATE | FILE_RECOVERY | HAL_EXTENSION | IP_SECURITY_END_SYSTEM | IP_SECURITY_IKE_INTERMEDIATE | IP_SECURITY_TUNNEL_TERMINATION | IP_SECURITY_USER | ISOLATED_USER_MODE | KDC_AUTHENTICATION | KERNEL_MODE_CODE_SIGNING | KEY_PACK_LICENSES | KEY_RECOVERY | KEY_RECOVERY_AGENT | LICENSE_SERVER_VERIFICATION | LIFETIME_SIGNING | MICROSOFT_PUBLISHER | MICROSOFT_TIME_STAMPING | MICROSOFT_TRUST_LIST_SIGNING | OCSP_SIGNING | OEM_WINDOWS_SYSTEM_COMPONENT_VERIFICATION | PLATFORM_CERTIFICATE | PREVIEW_BUILD_SIGNING | PRIVATE_KEY_ARCHIVAL | PROTECTED_PROCESS_LIGHT_VERIFICATION | PROTECTED_PROCESS_VERIFICATION | QUALIFIED_SUBORDINATION | REVOKED_LIST_SIGNER | ROOT_LIST_SIGNER | ROOT_PROGRAM_AUTO_UPDATE_CA_REVOCATION | ROOT_PROGRAM_AUTO_UPDATE_END_REVOCATION | ROOT_PROGRAM_NO_OSCP_FAILOVER_TO_CRL | SECURE_EMAIL | SERVER_AUTHENTICATION | SMART_CARD_LOGIN | SPC_ENCRYPTED_DIGEST_RETRY_COUNT | SPC_RELAXED_PE_MARKER_CHECK | TIME_STAMPING | WINDOWS_HARDWARE_DRIVER_ATTESTED_VERIFICATION | WINDOWS_HARDWARE_DRIVER_EXTENDED_VERIFICATION | WINDOWS_HARDWARE_DRIVER_VERIFICATION | WINDOWS_HELLO_RECOVERY_KEY_ENCRYPTION | WINDOWS_KITS_COMPONENT | WINDOWS_RT_VERIFICATION | WINDOWS_SOFTWARE_EXTENSION_VERIFICATION | WINDOWS_STORE | WINDOWS_SYSTEM_COMPONENT_VERIFICATION | WINDOWS_TCB_COMPONENT | WINDOWS_THIRD_PARTY_APPLICATION_COMPONENT | WINDOWS_UPDATE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)