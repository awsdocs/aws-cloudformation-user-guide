# AWS::MediaPackage::PackagingConfiguration EncryptionContractConfiguration<a name="aws-properties-mediapackage-packagingconfiguration-encryptioncontractconfiguration"></a>

Use `encryptionContractConfiguration` to configure one or more content encryption keys for your endpoints that use SPEKE Version 2\.0\. The encryption contract defines the content keys used to encrypt the audio and video tracks in your stream\. To configure the encryption contract, specify which audio and video encryption presets to use\. For more information about these presets, see [SPEKE Version 2\.0 Presets](https://docs.aws.amazon.com/mediapackage/latest/ug/drm-content-speke-v2-presets.html)\.

Note the following considerations when using `encryptionContractConfiguration`:
+ You can use `encryptionContractConfiguration` for DASH endpoints that use SPEKE Version 2\.0\. SPEKE Version 2\.0 relies on the CPIX Version 2\.3 specification\.
+ You cannot combine an `UNENCRYPTED` preset with `UNENCRYPTED` or `SHARED` presets across `presetSpeke20Audio` and `presetSpeke20Video`\.
+ When you use a `SHARED` preset, you must use it for both `presetSpeke20Audio` and `presetSpeke20Video`\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-encryptioncontractconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-encryptioncontractconfiguration-syntax.json"></a>

```
{
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-encryptioncontractconfiguration-syntax.yaml"></a>

```
```