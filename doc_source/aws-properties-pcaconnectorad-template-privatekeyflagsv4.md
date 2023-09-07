# AWS::PCAConnectorAD::Template PrivateKeyFlagsV4<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv4"></a>

Private key flags for v4 templates specify the client compatibility, if the private key can be exported, if user input is required when using a private key, if an alternate signature algorithm should be used, and if certificates are renewed using the same private key\.

## Syntax<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv4-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv4-syntax.json"></a>

```
{
  "[ClientVersion](#cfn-pcaconnectorad-template-privatekeyflagsv4-clientversion)" : String,
  "[ExportableKey](#cfn-pcaconnectorad-template-privatekeyflagsv4-exportablekey)" : Boolean,
  "[RequireAlternateSignatureAlgorithm](#cfn-pcaconnectorad-template-privatekeyflagsv4-requirealternatesignaturealgorithm)" : Boolean,
  "[RequireSameKeyRenewal](#cfn-pcaconnectorad-template-privatekeyflagsv4-requiresamekeyrenewal)" : Boolean,
  "[StrongKeyProtectionRequired](#cfn-pcaconnectorad-template-privatekeyflagsv4-strongkeyprotectionrequired)" : Boolean,
  "[UseLegacyProvider](#cfn-pcaconnectorad-template-privatekeyflagsv4-uselegacyprovider)" : Boolean
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv4-syntax.yaml"></a>

```
  [ClientVersion](#cfn-pcaconnectorad-template-privatekeyflagsv4-clientversion): String
  [ExportableKey](#cfn-pcaconnectorad-template-privatekeyflagsv4-exportablekey): Boolean
  [RequireAlternateSignatureAlgorithm](#cfn-pcaconnectorad-template-privatekeyflagsv4-requirealternatesignaturealgorithm): Boolean
  [RequireSameKeyRenewal](#cfn-pcaconnectorad-template-privatekeyflagsv4-requiresamekeyrenewal): Boolean
  [StrongKeyProtectionRequired](#cfn-pcaconnectorad-template-privatekeyflagsv4-strongkeyprotectionrequired): Boolean
  [UseLegacyProvider](#cfn-pcaconnectorad-template-privatekeyflagsv4-uselegacyprovider): Boolean
```

## Properties<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv4-properties"></a>

`ClientVersion`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv4-clientversion"></a>
Defines the minimum client compatibility\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `WINDOWS_SERVER_2012 | WINDOWS_SERVER_2012_R2 | WINDOWS_SERVER_2016`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExportableKey`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv4-exportablekey"></a>
Allows the private key to be exported\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireAlternateSignatureAlgorithm`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv4-requirealternatesignaturealgorithm"></a>
Requires the PKCS \#1 v2\.1 signature format for certificates\. You should verify that your CA, objects, and applications can accept this signature format\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireSameKeyRenewal`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv4-requiresamekeyrenewal"></a>
Renew certificate using the same private key\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StrongKeyProtectionRequired`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv4-strongkeyprotectionrequired"></a>
Require user input when using the private key for enrollment\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseLegacyProvider`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv4-uselegacyprovider"></a>
Specifies the cryptographic service provider category used to generate private keys\. Set to TRUE to use Legacy Cryptographic Service Providers and FALSE to use Key Storage Providers\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)