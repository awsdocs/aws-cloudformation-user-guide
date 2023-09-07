# AWS::PCAConnectorAD::Template SubjectNameFlagsV3<a name="aws-properties-pcaconnectorad-template-subjectnameflagsv3"></a>

Information to include in the subject name and alternate subject name of the certificate\. The subject name can be common name, directory path, DNS as common name, or left blank\. You can optionally include email to the subject name for user templates\. If you leave the subject name blank then you must set a subject alternate name\. The subject alternate name \(SAN\) can include globally unique identifier \(GUID\), DNS, domain DNS, email, service principal name \(SPN\), and user principal name \(UPN\)\. You can leave the SAN blank\. If you leave the SAN blank, then you must set a subject name\.

## Syntax<a name="aws-properties-pcaconnectorad-template-subjectnameflagsv3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-subjectnameflagsv3-syntax.json"></a>

```
{
  "[RequireCommonName](#cfn-pcaconnectorad-template-subjectnameflagsv3-requirecommonname)" : Boolean,
  "[RequireDirectoryPath](#cfn-pcaconnectorad-template-subjectnameflagsv3-requiredirectorypath)" : Boolean,
  "[RequireDnsAsCn](#cfn-pcaconnectorad-template-subjectnameflagsv3-requirednsascn)" : Boolean,
  "[RequireEmail](#cfn-pcaconnectorad-template-subjectnameflagsv3-requireemail)" : Boolean,
  "[SanRequireDirectoryGuid](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequiredirectoryguid)" : Boolean,
  "[SanRequireDns](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequiredns)" : Boolean,
  "[SanRequireDomainDns](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequiredomaindns)" : Boolean,
  "[SanRequireEmail](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequireemail)" : Boolean,
  "[SanRequireSpn](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequirespn)" : Boolean,
  "[SanRequireUpn](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequireupn)" : Boolean
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-subjectnameflagsv3-syntax.yaml"></a>

```
  [RequireCommonName](#cfn-pcaconnectorad-template-subjectnameflagsv3-requirecommonname): Boolean
  [RequireDirectoryPath](#cfn-pcaconnectorad-template-subjectnameflagsv3-requiredirectorypath): Boolean
  [RequireDnsAsCn](#cfn-pcaconnectorad-template-subjectnameflagsv3-requirednsascn): Boolean
  [RequireEmail](#cfn-pcaconnectorad-template-subjectnameflagsv3-requireemail): Boolean
  [SanRequireDirectoryGuid](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequiredirectoryguid): Boolean
  [SanRequireDns](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequiredns): Boolean
  [SanRequireDomainDns](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequiredomaindns): Boolean
  [SanRequireEmail](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequireemail): Boolean
  [SanRequireSpn](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequirespn): Boolean
  [SanRequireUpn](#cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequireupn): Boolean
```

## Properties<a name="aws-properties-pcaconnectorad-template-subjectnameflagsv3-properties"></a>

`RequireCommonName`  <a name="cfn-pcaconnectorad-template-subjectnameflagsv3-requirecommonname"></a>
Include the common name in the subject name\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireDirectoryPath`  <a name="cfn-pcaconnectorad-template-subjectnameflagsv3-requiredirectorypath"></a>
Include the directory path in the subject name\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireDnsAsCn`  <a name="cfn-pcaconnectorad-template-subjectnameflagsv3-requirednsascn"></a>
Include the DNS as common name in the subject name\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireEmail`  <a name="cfn-pcaconnectorad-template-subjectnameflagsv3-requireemail"></a>
Include the subject's email in the subject name\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SanRequireDirectoryGuid`  <a name="cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequiredirectoryguid"></a>
Include the globally unique identifier \(GUID\) in the subject alternate name\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SanRequireDns`  <a name="cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequiredns"></a>
Include the DNS in the subject alternate name\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SanRequireDomainDns`  <a name="cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequiredomaindns"></a>
Include the domain DNS in the subject alternate name\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SanRequireEmail`  <a name="cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequireemail"></a>
Include the subject's email in the subject alternate name\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SanRequireSpn`  <a name="cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequirespn"></a>
Include the service principal name \(SPN\) in the subject alternate name\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SanRequireUpn`  <a name="cfn-pcaconnectorad-template-subjectnameflagsv3-sanrequireupn"></a>
Include the user principal name \(UPN\) in the subject alternate name\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)