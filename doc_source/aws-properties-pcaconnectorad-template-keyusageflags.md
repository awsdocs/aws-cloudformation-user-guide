# AWS::PCAConnectorAD::Template KeyUsageFlags<a name="aws-properties-pcaconnectorad-template-keyusageflags"></a>

The key usage flags represent the purpose \(e\.g\., encipherment, signature\) of the key contained in the certificate\.

## Syntax<a name="aws-properties-pcaconnectorad-template-keyusageflags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-keyusageflags-syntax.json"></a>

```
{
  "[DataEncipherment](#cfn-pcaconnectorad-template-keyusageflags-dataencipherment)" : Boolean,
  "[DigitalSignature](#cfn-pcaconnectorad-template-keyusageflags-digitalsignature)" : Boolean,
  "[KeyAgreement](#cfn-pcaconnectorad-template-keyusageflags-keyagreement)" : Boolean,
  "[KeyEncipherment](#cfn-pcaconnectorad-template-keyusageflags-keyencipherment)" : Boolean,
  "[NonRepudiation](#cfn-pcaconnectorad-template-keyusageflags-nonrepudiation)" : Boolean
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-keyusageflags-syntax.yaml"></a>

```
  [DataEncipherment](#cfn-pcaconnectorad-template-keyusageflags-dataencipherment): Boolean
  [DigitalSignature](#cfn-pcaconnectorad-template-keyusageflags-digitalsignature): Boolean
  [KeyAgreement](#cfn-pcaconnectorad-template-keyusageflags-keyagreement): Boolean
  [KeyEncipherment](#cfn-pcaconnectorad-template-keyusageflags-keyencipherment): Boolean
  [NonRepudiation](#cfn-pcaconnectorad-template-keyusageflags-nonrepudiation): Boolean
```

## Properties<a name="aws-properties-pcaconnectorad-template-keyusageflags-properties"></a>

`DataEncipherment`  <a name="cfn-pcaconnectorad-template-keyusageflags-dataencipherment"></a>
DataEncipherment is asserted when the subject public key is used for directly enciphering raw user data without the use of an intermediate symmetric cipher\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DigitalSignature`  <a name="cfn-pcaconnectorad-template-keyusageflags-digitalsignature"></a>
The digitalSignature is asserted when the subject public key is used for verifying digital signatures\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyAgreement`  <a name="cfn-pcaconnectorad-template-keyusageflags-keyagreement"></a>
KeyAgreement is asserted when the subject public key is used for key agreement\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyEncipherment`  <a name="cfn-pcaconnectorad-template-keyusageflags-keyencipherment"></a>
KeyEncipherment is asserted when the subject public key is used for enciphering private or secret keys, i\.e\., for key transport\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NonRepudiation`  <a name="cfn-pcaconnectorad-template-keyusageflags-nonrepudiation"></a>
NonRepudiation is asserted when the subject public key is used to verify digital signatures\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)