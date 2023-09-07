# AWS::PCAConnectorAD::Template PrivateKeyAttributesV3<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv3"></a>

Defines the attributes of the private key\.

## Syntax<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv3-syntax.json"></a>

```
{
  "[Algorithm](#cfn-pcaconnectorad-template-privatekeyattributesv3-algorithm)" : String,
  "[CryptoProviders](#cfn-pcaconnectorad-template-privatekeyattributesv3-cryptoproviders)" : [ String, ... ],
  "[KeySpec](#cfn-pcaconnectorad-template-privatekeyattributesv3-keyspec)" : String,
  "[KeyUsageProperty](#cfn-pcaconnectorad-template-privatekeyattributesv3-keyusageproperty)" : KeyUsageProperty,
  "[MinimalKeyLength](#cfn-pcaconnectorad-template-privatekeyattributesv3-minimalkeylength)" : Double
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv3-syntax.yaml"></a>

```
  [Algorithm](#cfn-pcaconnectorad-template-privatekeyattributesv3-algorithm): String
  [CryptoProviders](#cfn-pcaconnectorad-template-privatekeyattributesv3-cryptoproviders): 
    - String
  [KeySpec](#cfn-pcaconnectorad-template-privatekeyattributesv3-keyspec): String
  [KeyUsageProperty](#cfn-pcaconnectorad-template-privatekeyattributesv3-keyusageproperty): 
    KeyUsageProperty
  [MinimalKeyLength](#cfn-pcaconnectorad-template-privatekeyattributesv3-minimalkeylength): Double
```

## Properties<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv3-properties"></a>

`Algorithm`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv3-algorithm"></a>
Defines the algorithm used to generate the private key\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ECDH_P256 | ECDH_P384 | ECDH_P521 | RSA`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CryptoProviders`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv3-cryptoproviders"></a>
Defines the cryptographic providers used to generate the private key\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeySpec`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv3-keyspec"></a>
Defines the purpose of the private key\. Set it to "KEY\_EXCHANGE" or "SIGNATURE" value\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `KEY_EXCHANGE | SIGNATURE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyUsageProperty`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv3-keyusageproperty"></a>
The key usage property defines the purpose of the private key contained in the certificate\. You can specify specific purposes using property flags or all by using property type ALL\.  
*Required*: Yes  
*Type*: [KeyUsageProperty](aws-properties-pcaconnectorad-template-keyusageproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimalKeyLength`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv3-minimalkeylength"></a>
Set the minimum key length of the private key\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)