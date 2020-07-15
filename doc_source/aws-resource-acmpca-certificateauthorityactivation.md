# AWS::ACMPCA::CertificateAuthorityActivation<a name="aws-resource-acmpca-certificateauthorityactivation"></a>

The `AWS::ACMPCA::CertificateAuthorityActivation` resource creates and installs a CA certificate on a CA\. If no status is specified, the `AWS::ACMPCA::CertificateAuthorityActivation` resource status defaults to ACTIVE\. Once the CA has a CA certificate installed, you can use the resource to toggle the CA status field between ACTIVE and DISABLED\.

## Syntax<a name="aws-resource-acmpca-certificateauthorityactivation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-acmpca-certificateauthorityactivation-syntax.json"></a>

```
{
  "Type" : "AWS::ACMPCA::CertificateAuthorityActivation",
  "Properties" : {
      "[Certificate](#cfn-acmpca-certificateauthorityactivation-certificate)" : String,
      "[CertificateAuthorityArn](#cfn-acmpca-certificateauthorityactivation-certificateauthorityarn)" : String,
      "[CertificateChain](#cfn-acmpca-certificateauthorityactivation-certificatechain)" : String,
      "[Status](#cfn-acmpca-certificateauthorityactivation-status)" : String
    }
}
```

### YAML<a name="aws-resource-acmpca-certificateauthorityactivation-syntax.yaml"></a>

```
Type: AWS::ACMPCA::CertificateAuthorityActivation
Properties: 
  [Certificate](#cfn-acmpca-certificateauthorityactivation-certificate): String
  [CertificateAuthorityArn](#cfn-acmpca-certificateauthorityactivation-certificateauthorityarn): String
  [CertificateChain](#cfn-acmpca-certificateauthorityactivation-certificatechain): String
  [Status](#cfn-acmpca-certificateauthorityactivation-status): String
```

## Properties<a name="aws-resource-acmpca-certificateauthorityactivation-properties"></a>

`Certificate`  <a name="cfn-acmpca-certificateauthorityactivation-certificate"></a>
The Base64 PEM\-encoded certificate authority certificate\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CertificateAuthorityArn`  <a name="cfn-acmpca-certificateauthorityactivation-certificateauthorityarn"></a>
The Amazon Resource Name \(ARN\) of your private CA\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateChain`  <a name="cfn-acmpca-certificateauthorityactivation-certificatechain"></a>
The Base64 PEM\-encoded certificate chain that chains up to the root CA certificate that you used to sign your private CA certificate\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-acmpca-certificateauthorityactivation-status"></a>
Status of your private CA\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-acmpca-certificateauthorityactivation-return-values"></a>

### Ref<a name="aws-resource-acmpca-certificateauthorityactivation-return-values-ref"></a>

The Amazon Resource Name \(ARN\) of the certificate authority\.

### Fn::GetAtt<a name="aws-resource-acmpca-certificateauthorityactivation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-acmpca-certificateauthorityactivation-return-values-fn--getatt-fn--getatt"></a>

`CompleteCertificateChain`  <a name="CompleteCertificateChain-fn::getatt"></a>
The complete Base64 PEM\-encoded certificate chain, including the certificate authority certificate\.