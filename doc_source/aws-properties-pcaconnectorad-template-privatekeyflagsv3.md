# AWS::PCAConnectorAD::Template PrivateKeyFlagsV3<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv3"></a>

Private key flags for v3 templates specify the client compatibility, if the private key can be exported, if user input is required when using a private key, and if an alternate signature algorithm should be used\.

## Syntax<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv3-syntax.json"></a>

```
{
  "[ClientVersion](#cfn-pcaconnectorad-template-privatekeyflagsv3-clientversion)" : String,
  "[ExportableKey](#cfn-pcaconnectorad-template-privatekeyflagsv3-exportablekey)" : Boolean,
  "[RequireAlternateSignatureAlgorithm](#cfn-pcaconnectorad-template-privatekeyflagsv3-requirealternatesignaturealgorithm)" : Boolean,
  "[StrongKeyProtectionRequired](#cfn-pcaconnectorad-template-privatekeyflagsv3-strongkeyprotectionrequired)" : Boolean
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv3-syntax.yaml"></a>

```
  [ClientVersion](#cfn-pcaconnectorad-template-privatekeyflagsv3-clientversion): String
  [ExportableKey](#cfn-pcaconnectorad-template-privatekeyflagsv3-exportablekey): Boolean
  [RequireAlternateSignatureAlgorithm](#cfn-pcaconnectorad-template-privatekeyflagsv3-requirealternatesignaturealgorithm): Boolean
  [StrongKeyProtectionRequired](#cfn-pcaconnectorad-template-privatekeyflagsv3-strongkeyprotectionrequired): Boolean
```

## Properties<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv3-properties"></a>

`ClientVersion`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv3-clientversion"></a>
Defines the minimum client compatibility\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `WINDOWS_SERVER_2008 | WINDOWS_SERVER_2008_R2 | WINDOWS_SERVER_2012 | WINDOWS_SERVER_2012_R2 | WINDOWS_SERVER_2016`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExportableKey`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv3-exportablekey"></a>
Allows the private key to be exported\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireAlternateSignatureAlgorithm`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv3-requirealternatesignaturealgorithm"></a>
Reguires the PKCS \#1 v2\.1 signature format for certificates\. You should verify that your CA, objects, and applications can accept this signature format\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StrongKeyProtectionRequired`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv3-strongkeyprotectionrequired"></a>
Requirer user input when using the private key for enrollment\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)