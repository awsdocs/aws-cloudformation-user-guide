# AWS::ACMPCA::Permission<a name="aws-resource-acmpca-permission"></a>

Grants permissions to the AWS Certificate Manager \(ACM\) service principal \(`acm.amazonaws.com`\) to perform [IssueCertificate](https://docs.aws.amazon.com/privateca/latest/APIReference/API_IssueCertificate.html), [GetCertificate](https://docs.aws.amazon.com/privateca/latest/APIReference/API_GetCertificate.html), and [ListPermissions](https://docs.aws.amazon.com/privateca/latest/APIReference/API_ListPermissions.html) actions on a CA\. These actions are needed for the ACM principal to renew private PKI certificates requested through ACM and residing in the same AWS account as the CA\.

**About permissions**
+ If the private CA and the certificates it issues reside in the same account, you can use `AWS::ACMPCA::Permission` to grant permissions for ACM to carry out automatic certificate renewals\.
+ For automatic certificate renewal to succeed, the ACM service principal needs permissions to create, retrieve, and list permissions\.
+ If the private CA and the ACM certificates reside in different accounts, then permissions cannot be used to enable automatic renewals\. Instead, the ACM certificate owner must set up a resource\-based policy to enable cross\-account issuance and renewals\. For more information, see [Using a Resource Based Policy with AWS Private CA](https://docs.aws.amazon.com/privateca/latest/userguide/pca-rbp.html)\.

**Note**  
To update an `AWS::ACMPCA::Permission` resource, you must first delete the existing permission resource from the CloudFormation stack and then create a new permission resource with updated properties\.

## Syntax<a name="aws-resource-acmpca-permission-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-acmpca-permission-syntax.json"></a>

```
{
  "Type" : "AWS::ACMPCA::Permission",
  "Properties" : {
      "[Actions](#cfn-acmpca-permission-actions)" : [ String, ... ],
      "[CertificateAuthorityArn](#cfn-acmpca-permission-certificateauthorityarn)" : String,
      "[Principal](#cfn-acmpca-permission-principal)" : String,
      "[SourceAccount](#cfn-acmpca-permission-sourceaccount)" : String
    }
}
```

### YAML<a name="aws-resource-acmpca-permission-syntax.yaml"></a>

```
Type: AWS::ACMPCA::Permission
Properties: 
  [Actions](#cfn-acmpca-permission-actions): 
    - String
  [CertificateAuthorityArn](#cfn-acmpca-permission-certificateauthorityarn): String
  [Principal](#cfn-acmpca-permission-principal): String
  [SourceAccount](#cfn-acmpca-permission-sourceaccount): String
```

## Properties<a name="aws-resource-acmpca-permission-properties"></a>

`Actions`  <a name="cfn-acmpca-permission-actions"></a>
The private CA actions that can be performed by the designated AWS service\. Supported actions are `IssueCertificate`, `GetCertificate`, and `ListPermissions`\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `3`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateAuthorityArn`  <a name="cfn-acmpca-permission-certificateauthorityarn"></a>
The Amazon Resource Number \(ARN\) of the private CA from which the permission was issued\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `5`  
*Maximum*: `200`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:[\w+=/,.@-]*:[0-9]*:[\w+=,.@-]+(/[\w+=,.@-]+)*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Principal`  <a name="cfn-acmpca-permission-principal"></a>
The AWS service or entity that holds the permission\. At this time, the only valid principal is `acm.amazonaws.com`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Pattern*: `^[^*]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceAccount`  <a name="cfn-acmpca-permission-sourceaccount"></a>
The ID of the account that assigned the permission\.  
*Required*: No  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `[0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)