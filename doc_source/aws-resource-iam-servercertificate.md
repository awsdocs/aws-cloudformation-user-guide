# AWS::IAM::ServerCertificate<a name="aws-resource-iam-servercertificate"></a>

Uploads a server certificate entity for the AWS account\. The server certificate entity includes a public key certificate, a private key, and an optional certificate chain, which should all be PEM\-encoded\.

We recommend that you use [AWS Certificate Manager](https://docs.aws.amazon.com/acm/) to provision, manage, and deploy your server certificates\. With ACM you can request a certificate, deploy it to AWS resources, and let ACM handle certificate renewals for you\. Certificates provided by ACM are free\. For more information about using ACM, see the [AWS Certificate Manager User Guide](https://docs.aws.amazon.com/acm/latest/userguide/)\.

For more information about working with server certificates, see [Working with server certificates](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_server-certs.html) in the *IAM User Guide*\. This topic includes a list of AWS services that can use the server certificates that you manage with IAM\.

For information about the number of server certificates you can upload, see [IAM and AWS STS quotas](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-quotas.html) in the *IAM User Guide*\.

**Note**  
Because the body of the public key certificate, private key, and the certificate chain can be large, you should use POST rather than GET when calling `UploadServerCertificate`\. For information about setting up signatures and authorization through the API, see [Signing AWS API requests](https://docs.aws.amazon.com/general/latest/gr/signing_aws_api_requests.html) in the * AWS General Reference*\. For general information about using the Query API with IAM, see [Calling the API by making HTTP query requests](https://docs.aws.amazon.com/IAM/latest/UserGuide/programming.html) in the *IAM User Guide*\.

## Syntax<a name="aws-resource-iam-servercertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-servercertificate-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::ServerCertificate",
  "Properties" : {
      "[CertificateBody](#cfn-iam-servercertificate-certificatebody)" : String,
      "[CertificateChain](#cfn-iam-servercertificate-certificatechain)" : String,
      "[Path](#cfn-iam-servercertificate-path)" : String,
      "[PrivateKey](#cfn-iam-servercertificate-privatekey)" : String,
      "[ServerCertificateName](#cfn-iam-servercertificate-servercertificatename)" : String,
      "[Tags](#cfn-iam-servercertificate-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iam-servercertificate-syntax.yaml"></a>

```
Type: AWS::IAM::ServerCertificate
Properties: 
  [CertificateBody](#cfn-iam-servercertificate-certificatebody): String
  [CertificateChain](#cfn-iam-servercertificate-certificatechain): String
  [Path](#cfn-iam-servercertificate-path): String
  [PrivateKey](#cfn-iam-servercertificate-privatekey): String
  [ServerCertificateName](#cfn-iam-servercertificate-servercertificatename): String
  [Tags](#cfn-iam-servercertificate-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iam-servercertificate-properties"></a>

`CertificateBody`  <a name="cfn-iam-servercertificate-certificatebody"></a>
The contents of the public key certificate\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `16384`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u00FF]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateChain`  <a name="cfn-iam-servercertificate-certificatechain"></a>
The contents of the public key certificate chain\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2097152`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u00FF]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Path`  <a name="cfn-iam-servercertificate-path"></a>
The path for the server certificate\. For more information about paths, see [IAM identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html) in the *IAM User Guide*\.  
This parameter is optional\. If it is not included, it defaults to a slash \(/\)\. This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of either a forward slash \(/\) by itself or a string that must begin and end with forward slashes\. In addition, it can contain any ASCII character from the \! \(`\u0021`\) through the DEL character \(`\u007F`\), including most punctuation characters, digits, and upper and lowercased letters\.  
 If you are uploading a server certificate specifically for use with Amazon CloudFront distributions, you must specify a path using the `path` parameter\. The path must begin with `/cloudfront` and must include a trailing slash \(for example, `/cloudfront/test/`\)\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `(\u002F)|(\u002F[\u0021-\u007F]+\u002F)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKey`  <a name="cfn-iam-servercertificate-privatekey"></a>
The contents of the private key in PEM\-encoded format\.  
The [regex pattern](http://wikipedia.org/wiki/regex) used to validate this parameter is a string of characters consisting of the following:  
+ Any printable ASCII character ranging from the space character \(`\u0020`\) through the end of the ASCII character range
+ The printable characters in the Basic Latin and Latin\-1 Supplement character set \(through `\u00FF`\)
+ The special characters tab \(`\u0009`\), line feed \(`\u000A`\), and carriage return \(`\u000D`\)
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `16384`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u00FF]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerCertificateName`  <a name="cfn-iam-servercertificate-servercertificatename"></a>
The name for the server certificate\. Do not include the path in this value\. The name of the certificate cannot contain any spaces\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iam-servercertificate-tags"></a>
A list of tags that are attached to the server certificate\. For more information about tagging, see [Tagging IAM resources](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_tags.html) in the *IAM User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iam-servercertificate-return-values"></a>

### Ref<a name="aws-resource-iam-servercertificate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `ServerCertificateName`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iam-servercertificate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iam-servercertificate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the specified `AWS::IAM::ServerCertificate` resource\.