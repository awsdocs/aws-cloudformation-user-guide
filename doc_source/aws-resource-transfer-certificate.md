# AWS::Transfer::Certificate<a name="aws-resource-transfer-certificate"></a>

Imports the signing and encryption certificates that you need to create local \(AS2\) profiles and partner profiles\.

## Syntax<a name="aws-resource-transfer-certificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-transfer-certificate-syntax.json"></a>

```
{
  "Type" : "AWS::Transfer::Certificate",
  "Properties" : {
      "[ActiveDate](#cfn-transfer-certificate-activedate)" : String,
      "[Certificate](#cfn-transfer-certificate-certificate)" : String,
      "[CertificateChain](#cfn-transfer-certificate-certificatechain)" : String,
      "[Description](#cfn-transfer-certificate-description)" : String,
      "[InactiveDate](#cfn-transfer-certificate-inactivedate)" : String,
      "[PrivateKey](#cfn-transfer-certificate-privatekey)" : String,
      "[Tags](#cfn-transfer-certificate-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Usage](#cfn-transfer-certificate-usage)" : String
    }
}
```

### YAML<a name="aws-resource-transfer-certificate-syntax.yaml"></a>

```
Type: AWS::Transfer::Certificate
Properties: 
  [ActiveDate](#cfn-transfer-certificate-activedate): String
  [Certificate](#cfn-transfer-certificate-certificate): String
  [CertificateChain](#cfn-transfer-certificate-certificatechain): String
  [Description](#cfn-transfer-certificate-description): String
  [InactiveDate](#cfn-transfer-certificate-inactivedate): String
  [PrivateKey](#cfn-transfer-certificate-privatekey): String
  [Tags](#cfn-transfer-certificate-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Usage](#cfn-transfer-certificate-usage): String
```

## Properties<a name="aws-resource-transfer-certificate-properties"></a>

`ActiveDate`  <a name="cfn-transfer-certificate-activedate"></a>
An optional date that specifies when the certificate becomes active\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Certificate`  <a name="cfn-transfer-certificate-certificate"></a>
The file name for the certificate\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `16384`  
*Pattern*: `^[\u0009\u000A\u000D\u0020-\u00FF]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateChain`  <a name="cfn-transfer-certificate-certificatechain"></a>
The list of certificates that make up the chain for the certificate\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2097152`  
*Pattern*: `^[\u0009\u000A\u000D\u0020-\u00FF]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-transfer-certificate-description"></a>
The name or description that's used to identity the certificate\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `^[\p{Graph}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InactiveDate`  <a name="cfn-transfer-certificate-inactivedate"></a>
An optional date that specifies when the certificate becomes inactive\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKey`  <a name="cfn-transfer-certificate-privatekey"></a>
The file that contains the private key for the certificate that's being imported\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-transfer-certificate-tags"></a>
Key\-value pairs that can be used to group and search for certificates\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Usage`  <a name="cfn-transfer-certificate-usage"></a>
Specifies whether this certificate is used for signing or encryption\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ENCRYPTION | SIGNING`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-transfer-certificate-return-values"></a>

### Ref<a name="aws-resource-transfer-certificate-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `certificateId`, such as `cert-1c698edce1654f869`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-transfer-certificate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-transfer-certificate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The unique Amazon Resource Name \(ARN\) for the certificate\.

`CertificateId`  <a name="CertificateId-fn::getatt"></a>
An array of identifiers for the imported certificates\. You use this identifier for working with profiles and partner profiles\.

`NotAfterDate`  <a name="NotAfterDate-fn::getatt"></a>
The final date that the certificate is valid\.

`NotBeforeDate`  <a name="NotBeforeDate-fn::getatt"></a>
The earliest date that the certificate is valid\.

`Serial`  <a name="Serial-fn::getatt"></a>
The serial number for the certificate\.

`Status`  <a name="Status-fn::getatt"></a>
The certificate can be either `ACTIVE`, `PENDING_ROTATION`, or `INACTIVE`\. `PENDING_ROTATION` means that this certificate will replace the current certificate when it expires\.

`Type`  <a name="Type-fn::getatt"></a>
If a private key has been specified for the certificate, its type is `CERTIFICATE_WITH_PRIVATE_KEY`\. If there is no private key, the type is `CERTIFICATE`\.