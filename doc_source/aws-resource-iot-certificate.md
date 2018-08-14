# AWS::IoT::Certificate<a name="aws-resource-iot-certificate"></a>

Use the `AWS::IoT::Certificate` resource to declare an X\.509 certificate\.

For information about working with X\.509 certificates, see [Authentication in AWS IoT](http://docs.aws.amazon.com/iot/latest/developerguide/identity-in-iot.html) in the *AWS IoT Developer Guide*\.

## Syntax<a name="w3ab2c21c10d790b7"></a>

### JSON<a name="aws-resource-iot-certificate-syntax.json"></a>

```
{
   "Type": "AWS::IoT::Certificate",
   "Properties": {
      "[CertificateSigningRequest](#cfn-iot-certificate-certificatesigningrequest)": String,
      "[Status](#cfn-iot-certificate-status)": String
    }
}
```

### YAML<a name="aws-resource-iot-certificate-syntax.yaml"></a>

```
Type: "AWS::IoT::Certificate"
  Properties:
    [CertificateSigningRequest](#cfn-iot-certificate-certificatesigningrequest): String
    [Status](#cfn-iot-certificate-status): String
```

## Properties<a name="w3ab2c21c10d790b9"></a>

`CertificateSigningRequest`  <a name="cfn-iot-certificate-certificatesigningrequest"></a>
The certificate signing request \(CSR\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Status`  <a name="cfn-iot-certificate-status"></a>
The status of the certificate\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d790c11"></a>

### Ref<a name="w3ab2c21c10d790c11b2"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the certificate ID\. For example:

```
{ "Ref": "MyCertificate" }
```

A value similar to the following is returned:

```
a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d790c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
Returns the Amazon Resource Name \(ARN\) for the instance profile\. For example:  

```
{ "Fn::GetAtt": ["MyCertificate", "Arn"] }
```
A value similar to the following is returned:  

```
arn:aws:iot:ap-southeast-2:123456789012:cert/a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2
```

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="w3ab2c21c10d790c13"></a>

The following example declares an X\.509 certificate and its status\.

### JSON<a name="aws-resource-iot-certificate-example.json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "MyCertificate": {
         "Type": "AWS::IoT::Certificate",
         "Properties": {
            "CertificateSigningRequest": {
               "Ref": "CSRParameter"
            },
            "Status": {
               "Ref": "StatusParameter"
            }
         }
      }
   },
   "Parameters": {
      "CSRParameter": {
         "Type": "String"
      },
      "StatusParameter": {
         "Type": "String"
      }
   }
}
```

### YAML<a name="aws-resource-iot-certificate-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  MyCertificate: 
    Type: "AWS::IoT::Certificate"
    Properties: 
      CertificateSigningRequest: 
        Ref: "CSRParameter"
      Status: 
        Ref: "StatusParameter"
Parameters: 
  CSRParameter: 
    Type: "String"
  StatusParameter: 
    Type: "String"
```