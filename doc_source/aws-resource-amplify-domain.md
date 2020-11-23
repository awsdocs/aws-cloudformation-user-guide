# AWS::Amplify::Domain<a name="aws-resource-amplify-domain"></a>

 The AWS::Amplify::Domain resource allows you to connect a custom domain to your app\. 

## Syntax<a name="aws-resource-amplify-domain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-amplify-domain-syntax.json"></a>

```
{
  "Type" : "AWS::Amplify::Domain",
  "Properties" : {
      "[AppId](#cfn-amplify-domain-appid)" : String,
      "[AutoSubDomainCreationPatterns](#cfn-amplify-domain-autosubdomaincreationpatterns)" : [ String, ... ],
      "[AutoSubDomainIAMRole](#cfn-amplify-domain-autosubdomainiamrole)" : String,
      "[DomainName](#cfn-amplify-domain-domainname)" : String,
      "[EnableAutoSubDomain](#cfn-amplify-domain-enableautosubdomain)" : Boolean,
      "[SubDomainSettings](#cfn-amplify-domain-subdomainsettings)" : [ SubDomainSetting, ... ]
    }
}
```

### YAML<a name="aws-resource-amplify-domain-syntax.yaml"></a>

```
Type: AWS::Amplify::Domain
Properties: 
  [AppId](#cfn-amplify-domain-appid): String
  [AutoSubDomainCreationPatterns](#cfn-amplify-domain-autosubdomaincreationpatterns): 
    - String
  [AutoSubDomainIAMRole](#cfn-amplify-domain-autosubdomainiamrole): String
  [DomainName](#cfn-amplify-domain-domainname): String
  [EnableAutoSubDomain](#cfn-amplify-domain-enableautosubdomain): Boolean
  [SubDomainSettings](#cfn-amplify-domain-subdomainsettings): 
    - SubDomainSetting
```

## Properties<a name="aws-resource-amplify-domain-properties"></a>

`AppId`  <a name="cfn-amplify-domain-appid"></a>
 The unique ID for an Amplify app\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AutoSubDomainCreationPatterns`  <a name="cfn-amplify-domain-autosubdomaincreationpatterns"></a>
 Sets the branch patterns for automatic subdomain creation\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoSubDomainIAMRole`  <a name="cfn-amplify-domain-autosubdomainiamrole"></a>
The required AWS Identity and Access Management \(IAM\) service role for the Amazon Resource Name \(ARN\) for automatically creating subdomains\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-amplify-domain-domainname"></a>
 The domain name for the domain association\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnableAutoSubDomain`  <a name="cfn-amplify-domain-enableautosubdomain"></a>
 Enables the automated creation of subdomains for branches\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubDomainSettings`  <a name="cfn-amplify-domain-subdomainsettings"></a>
 The setting for the subdomain\.   
*Required*: Yes  
*Type*: List of [SubDomainSetting](aws-properties-amplify-domain-subdomainsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-amplify-domain-return-values"></a>

### Fn::GetAtt<a name="aws-resource-amplify-domain-return-values-fn--getatt"></a>

#### <a name="aws-resource-amplify-domain-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
ARN for the Domain Association\.

`AutoSubDomainCreationPatterns`  <a name="AutoSubDomainCreationPatterns-fn::getatt"></a>
Branch patterns for the automatically created subdomain\.

`AutoSubDomainIAMRole`  <a name="AutoSubDomainIAMRole-fn::getatt"></a>
The IAM service role for the subdomain\.

`CertificateRecord`  <a name="CertificateRecord-fn::getatt"></a>
DNS Record for certificate verification\.

`DomainName`  <a name="DomainName-fn::getatt"></a>
Name of the domain\.

`DomainStatus`  <a name="DomainStatus-fn::getatt"></a>
Status for the Domain Association\.

`EnableAutoSubDomain`  <a name="EnableAutoSubDomain-fn::getatt"></a>
Specifies whether the automated creation of subdomains for branches is enabled\.

`StatusReason`  <a name="StatusReason-fn::getatt"></a>
Reason for the current status of the domain\.