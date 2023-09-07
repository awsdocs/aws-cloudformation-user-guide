# AWS::PCAConnectorAD::Template PrivateKeyAttributesV2<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv2"></a>

Defines the attributes of the private key\.

## Syntax<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv2-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv2-syntax.json"></a>

```
{
  "[CryptoProviders](#cfn-pcaconnectorad-template-privatekeyattributesv2-cryptoproviders)" : [ String, ... ],
  "[KeySpec](#cfn-pcaconnectorad-template-privatekeyattributesv2-keyspec)" : String,
  "[MinimalKeyLength](#cfn-pcaconnectorad-template-privatekeyattributesv2-minimalkeylength)" : Double
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv2-syntax.yaml"></a>

```
  [CryptoProviders](#cfn-pcaconnectorad-template-privatekeyattributesv2-cryptoproviders): 
    - String
  [KeySpec](#cfn-pcaconnectorad-template-privatekeyattributesv2-keyspec): String
  [MinimalKeyLength](#cfn-pcaconnectorad-template-privatekeyattributesv2-minimalkeylength): Double
```

## Properties<a name="aws-properties-pcaconnectorad-template-privatekeyattributesv2-properties"></a>

`CryptoProviders`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv2-cryptoproviders"></a>
Defines the cryptographic providers used to generate the private key\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeySpec`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv2-keyspec"></a>
Defines the purpose of the private key\. Set it to "KEY\_EXCHANGE" or "SIGNATURE" value\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `KEY_EXCHANGE | SIGNATURE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimalKeyLength`  <a name="cfn-pcaconnectorad-template-privatekeyattributesv2-minimalkeylength"></a>
Set the minimum key length of the private key\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)