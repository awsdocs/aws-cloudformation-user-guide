# AWS::PCAConnectorAD::Template PrivateKeyFlagsV2<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv2"></a>

Private key flags for v2 templates specify the client compatibility, if the private key can be exported, and if user input is required when using a private key\.

## Syntax<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv2-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv2-syntax.json"></a>

```
{
  "[ClientVersion](#cfn-pcaconnectorad-template-privatekeyflagsv2-clientversion)" : String,
  "[ExportableKey](#cfn-pcaconnectorad-template-privatekeyflagsv2-exportablekey)" : Boolean,
  "[StrongKeyProtectionRequired](#cfn-pcaconnectorad-template-privatekeyflagsv2-strongkeyprotectionrequired)" : Boolean
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv2-syntax.yaml"></a>

```
  [ClientVersion](#cfn-pcaconnectorad-template-privatekeyflagsv2-clientversion): String
  [ExportableKey](#cfn-pcaconnectorad-template-privatekeyflagsv2-exportablekey): Boolean
  [StrongKeyProtectionRequired](#cfn-pcaconnectorad-template-privatekeyflagsv2-strongkeyprotectionrequired): Boolean
```

## Properties<a name="aws-properties-pcaconnectorad-template-privatekeyflagsv2-properties"></a>

`ClientVersion`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv2-clientversion"></a>
Defines the minimum client compatibility\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `WINDOWS_SERVER_2003 | WINDOWS_SERVER_2008 | WINDOWS_SERVER_2008_R2 | WINDOWS_SERVER_2012 | WINDOWS_SERVER_2012_R2 | WINDOWS_SERVER_2016`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExportableKey`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv2-exportablekey"></a>
Allows the private key to be exported\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StrongKeyProtectionRequired`  <a name="cfn-pcaconnectorad-template-privatekeyflagsv2-strongkeyprotectionrequired"></a>
Require user input when using the private key for enrollment\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)