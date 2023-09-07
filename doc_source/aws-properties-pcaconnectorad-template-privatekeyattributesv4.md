# AWS::PCAConnectorAD::Template PrivateKeyAttributesV4<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv4"></a>

Defines the attributes of the private key\.

## Syntax<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv4-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv4-syntax.json"></a>

```
{
  "[Algorithm](#cfn-pcaconnectorad-template-privatekeyattributesv4-algorithm)" : String,
  "[CryptoProviders](#cfn-pcaconnectorad-template-privatekeyattributesv4-cryptoproviders)" : [ String, ... ],
  "[KeySpec](#cfn-pcaconnectorad-template-privatekeyattributesv4-keyspec)" : String,
  "[KeyUsageProperty](#cfn-pcaconnectorad-template-privatekeyattributesv4-keyusageproperty)" : KeyUsageProperty,
  "[MinimalKeyLength](#cfn-pcaconnectorad-template-privatekeyattributesv4-minimalkeylength)" : Double
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv4-syntax.yaml"></a>

```
  [Algorithm](#cfn-pcaconnectorad-template-privatekeyattributesv4-algorithm): String
  [CryptoProviders](#cfn-pcaconnectorad-template-privatekeyattributesv4-cryptoproviders): 
    - String
  [KeySpec](#cfn-pcaconnectorad-template-privatekeyattributesv4-keyspec): String
  [KeyUsageProperty](#cfn-pcaconnectorad-template-privatekeyattributesv4-keyusageproperty): 
    KeyUsageProperty
  [MinimalKeyLength](#cfn-pcaconnectorad-template-privatekeyattributesv4-minimalkeylength): Double
```

## Properties<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv4-properties"></a>

`Algorithm`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv4-algorithm"></a>
Defines the algorithm used to generate the private key\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ECDH_P256 | ECDH_P384 | ECDH_P521 | RSA`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CryptoProviders`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv4-cryptoproviders"></a>
Defines the cryptographic providers used to generate the private key\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeySpec`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv4-keyspec"></a>
Defines the purpose of the private key\. Set it to "KEY\_EXCHANGE" or "SIGNATURE" value\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `KEY_EXCHANGE | SIGNATURE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyUsageProperty`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv4-keyusageproperty"></a>
The key usage property defines the purpose of the private key contained in the certificate\. You can specify specific purposes using property flags or all by using property type ALL\.  
*Required*: No  
*Type*: [KeyUsageProperty](aws-properties-pcaconnectorad-template-keyusageproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimalKeyLength`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv4-minimalkeylength"></a>
Set the minimum key length of the private key\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)