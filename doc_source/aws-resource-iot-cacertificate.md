# AWS::IoT::CACertificate<a name="aws-resource-iot-cacertificate"></a>

Specifies a CA certificate\.

## Syntax<a name="aws-resource-iot-cacertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-cacertificate-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::CACertificate",
  "Properties" : {
      "[AutoRegistrationStatus](#cfn-iot-cacertificate-autoregistrationstatus)" : String,
      "[CACertificatePem](#cfn-iot-cacertificate-cacertificatepem)" : String,
      "[CertificateMode](#cfn-iot-cacertificate-certificatemode)" : String,
      "[RegistrationConfig](#cfn-iot-cacertificate-registrationconfig)" : RegistrationConfig,
      "[RemoveAutoRegistration](#cfn-iot-cacertificate-removeautoregistration)" : Boolean,
      "[Status](#cfn-iot-cacertificate-status)" : String,
      "[Tags](#cfn-iot-cacertificate-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VerificationCertificatePem](#cfn-iot-cacertificate-verificationcertificatepem)" : String
    }
}
```

### YAML<a name="aws-resource-iot-cacertificate-syntax.yaml"></a>

```
Type: AWS::IoT::CACertificate
Properties: 
  [AutoRegistrationStatus](#cfn-iot-cacertificate-autoregistrationstatus): String
  [CACertificatePem](#cfn-iot-cacertificate-cacertificatepem): String
  [CertificateMode](#cfn-iot-cacertificate-certificatemode): String
  [RegistrationConfig](#cfn-iot-cacertificate-registrationconfig): 
    RegistrationConfig
  [RemoveAutoRegistration](#cfn-iot-cacertificate-removeautoregistration): Boolean
  [Status](#cfn-iot-cacertificate-status): String
  [Tags](#cfn-iot-cacertificate-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VerificationCertificatePem](#cfn-iot-cacertificate-verificationcertificatepem): String
```

## Properties<a name="aws-resource-iot-cacertificate-properties"></a>

`AutoRegistrationStatus`  <a name="cfn-iot-cacertificate-autoregistrationstatus"></a>
Whether the CA certificate is configured for auto registration of device certificates\. Valid values are "ENABLE" and "DISABLE"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CACertificatePem`  <a name="cfn-iot-cacertificate-cacertificatepem"></a>
The certificate data in PEM format\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateMode`  <a name="cfn-iot-cacertificate-certificatemode"></a>
The mode of the CA\.   
All the device certificates that are registered using this CA will be registered in the same mode as the CA\. For more information about certificate mode for device certificates, see [certificate mode](https://docs.aws.amazon.com/iot/latest/apireference/API_CertificateDescription.html#iot-Type-CertificateDescription-certificateMode)\.  
Valid values are "DEFAULT" and "SNI\_ONLY"\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RegistrationConfig`  <a name="cfn-iot-cacertificate-registrationconfig"></a>
Information about the registration configuration\.  
*Required*: No  
*Type*: [RegistrationConfig](aws-properties-iot-cacertificate-registrationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveAutoRegistration`  <a name="cfn-iot-cacertificate-removeautoregistration"></a>
If true, removes auto registration\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-iot-cacertificate-status"></a>
The status of the CA certificate\.  
Valid values are "ACTIVE" and "INACTIVE"\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iot-cacertificate-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerificationCertificatePem`  <a name="cfn-iot-cacertificate-verificationcertificatepem"></a>
The private key verification certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot-cacertificate-return-values"></a>

### Ref<a name="aws-resource-iot-cacertificate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the CA certificate ID\.

### Fn::GetAtt<a name="aws-resource-iot-cacertificate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-cacertificate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the CA certificate\. For example:  
 `{ "Fn::GetAtt": ["MyCACertificate", "Arn"] }`   
A value similar to the following is returned:  
 `arn:aws:iot:us-east-1:123456789012:cacert/a6be6b84559801927e35a8f901fae08b5971d78d1562e29504ff9663b276a5f5` 

`Id`  <a name="Id-fn::getatt"></a>
The CA certificate ID\.