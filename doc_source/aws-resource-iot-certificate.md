# AWS::IoT::Certificate<a name="aws-resource-iot-certificate"></a>

Use the `AWS::IoT::Certificate` resource to declare an AWS IoT X\.509 certificate\. For information about working with X\.509 certificates, see [X\.509 Client Certificates](https://docs.aws.amazon.com/iot/latest/developerguide/x509-client-certs.html) in the *AWS IoT Developer Guide*\.

## Syntax<a name="aws-resource-iot-certificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-certificate-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::Certificate",
  "Properties" : {
      "[CACertificatePem](#cfn-iot-certificate-cacertificatepem)" : String,
      "[CertificateMode](#cfn-iot-certificate-certificatemode)" : String,
      "[CertificatePem](#cfn-iot-certificate-certificatepem)" : String,
      "[CertificateSigningRequest](#cfn-iot-certificate-certificatesigningrequest)" : String,
      "[Status](#cfn-iot-certificate-status)" : String
    }
}
```

### YAML<a name="aws-resource-iot-certificate-syntax.yaml"></a>

```
Type: AWS::IoT::Certificate
Properties: 
  [CACertificatePem](#cfn-iot-certificate-cacertificatepem): String
  [CertificateMode](#cfn-iot-certificate-certificatemode): String
  [CertificatePem](#cfn-iot-certificate-certificatepem): String
  [CertificateSigningRequest](#cfn-iot-certificate-certificatesigningrequest): String
  [Status](#cfn-iot-certificate-status): String
```

## Properties<a name="aws-resource-iot-certificate-properties"></a>

`CACertificatePem`  <a name="cfn-iot-certificate-cacertificatepem"></a>
The CA certificate used to sign the device certificate being registered, not available when CertificateMode is SNI\_ONLY\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateMode`  <a name="cfn-iot-certificate-certificatemode"></a>
Specifies which mode of certificate registration to use with this resource\. Valid options are DEFAULT with CaCertificatePem and CertificatePem, SNI\_ONLY with CertificatePem, and Default with CertificateSigningRequest\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificatePem`  <a name="cfn-iot-certificate-certificatepem"></a>
The certificate data in PEM format\. Requires SNI\_ONLY for the certificate mode or the accompanying CACertificatePem for registration\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateSigningRequest`  <a name="cfn-iot-certificate-certificatesigningrequest"></a>
The certificate signing request \(CSR\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Status`  <a name="cfn-iot-certificate-status"></a>
The status of the certificate\.  
Valid values are ACTIVE, INACTIVE, REVOKED, PENDING\_TRANSFER, and PENDING\_ACTIVATION\.  
The status value REGISTER\_INACTIVE is deprecated and should not be used\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-certificate-return-values"></a>

### Ref<a name="aws-resource-iot-certificate-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the certificate ID\. For example:

 `{ "Ref": "MyCertificate" }` 

A value similar to the following is returned:

 `a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot-certificate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-certificate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the instance profile\. For example:  
 `{ "Fn::GetAtt": ["MyCertificate", "Arn"] }`   
A value similar to the following is returned:  
 `arn:aws:iot:ap-southeast-2:123456789012:cert/a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2` 

`Id`  <a name="Id-fn::getatt"></a>
The certificate ID\.