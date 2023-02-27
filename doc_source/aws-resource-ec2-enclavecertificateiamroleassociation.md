# AWS::EC2::EnclaveCertificateIamRoleAssociation<a name="aws-resource-ec2-enclavecertificateiamroleassociation"></a>

Associates an AWS Identity and Access Management \(IAM\) role with an AWS Certificate Manager \(ACM\) certificate\. This enables the certificate to be used by the ACM for Nitro Enclaves application inside an enclave\. For more information, see [AWS Certificate Manager for Nitro Enclaves](https://docs.aws.amazon.com/enclaves/latest/user/nitro-enclave-refapp.html) in the * AWS Nitro Enclaves User Guide*\.

When the IAM role is associated with the ACM certificate, the certificate, certificate chain, and encrypted private key are placed in an Amazon S3 location that only the associated IAM role can access\. The private key of the certificate is encrypted with an AWS managed key that has an attached attestation\-based key policy\.

To enable the IAM role to access the Amazon S3 object, you must grant it permission to call `s3:GetObject` on the Amazon S3 bucket returned by the command\. To enable the IAM role to access the KMS key, you must grant it permission to call `kms:Decrypt` on the KMS key returned by the command\. For more information, see [ Grant the role permission to access the certificate and encryption key](https://docs.aws.amazon.com/enclaves/latest/user/nitro-enclave-refapp.html#add-policy) in the * AWS Nitro Enclaves User Guide*\.

## Syntax<a name="aws-resource-ec2-enclavecertificateiamroleassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-enclavecertificateiamroleassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::EnclaveCertificateIamRoleAssociation",
  "Properties" : {
      "[CertificateArn](#cfn-ec2-enclavecertificateiamroleassociation-certificatearn)" : String,
      "[RoleArn](#cfn-ec2-enclavecertificateiamroleassociation-rolearn)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-enclavecertificateiamroleassociation-syntax.yaml"></a>

```
Type: AWS::EC2::EnclaveCertificateIamRoleAssociation
Properties: 
  [CertificateArn](#cfn-ec2-enclavecertificateiamroleassociation-certificatearn): String
  [RoleArn](#cfn-ec2-enclavecertificateiamroleassociation-rolearn): String
```

## Properties<a name="aws-resource-ec2-enclavecertificateiamroleassociation-properties"></a>

`CertificateArn`  <a name="cfn-ec2-enclavecertificateiamroleassociation-certificatearn"></a>
The ARN of the ACM certificate with which to associate the IAM role\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-ec2-enclavecertificateiamroleassociation-rolearn"></a>
The ARN of the IAM role to associate with the ACM certificate\. You can associate up to 16 IAM roles with an ACM certificate\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-enclavecertificateiamroleassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-enclavecertificateiamroleassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the IAM role and ACM certificate association\.

### Fn::GetAtt<a name="aws-resource-ec2-enclavecertificateiamroleassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-enclavecertificateiamroleassociation-return-values-fn--getatt-fn--getatt"></a>

`CertificateS3BucketName`  <a name="CertificateS3BucketName-fn::getatt"></a>
The name of the Amazon S3 bucket to which the certificate was uploaded\.

`CertificateS3ObjectKey`  <a name="CertificateS3ObjectKey-fn::getatt"></a>
The Amazon S3 object key where the certificate, certificate chain, and encrypted private key bundle are stored\. The object key is formatted as follows: `role_arn`/`certificate_arn`\.

`EncryptionKmsKeyId`  <a name="EncryptionKmsKeyId-fn::getatt"></a>
The ID of the AWS KMS key used to encrypt the private key of the certificate\.

## Examples<a name="aws-resource-ec2-enclavecertificateiamroleassociation--examples"></a>

### Associating an IAM role with an ACM certificate<a name="aws-resource-ec2-enclavecertificateiamroleassociation--examples--Associating_an_IAM_role_with_an_ACM_certificate"></a>

The following example associates IAM role `arn:aws:iam::123456789012:role/my-acm-role` with ACM certificate `arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE`\.

#### JSON<a name="aws-resource-ec2-enclavecertificateiamroleassociation--examples--Associating_an_IAM_role_with_an_ACM_certificate--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "myCertAssociation",
    "Resources": {
        "MyEnclaveCertificateIamRoleAssociation": {
            "Type": "AWS::EC2::EnclaveCertificateIamRoleAssociation",
            "Properties": {
        "CertificateArn": "arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE",
        "RoleArn": "arn:aws:iam::123456789012:role/my-acm-role"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ec2-enclavecertificateiamroleassociation--examples--Associating_an_IAM_role_with_an_ACM_certificate--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myCertAssociation:
    Type: AWS::EC2::EnclaveCertificateIamRoleAssociation
    Properties:
      CertificateArn:
        "arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE"
      RoleArn:
        "arn:aws:iam::123456789012:role/my-acm-role"
```