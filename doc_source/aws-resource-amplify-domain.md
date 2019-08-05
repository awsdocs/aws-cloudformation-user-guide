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
      "[DomainName](#cfn-amplify-domain-domainname)" : String,
      "[SubDomainSettings](#cfn-amplify-domain-subdomainsettings)" : [ [SubDomainSetting](aws-properties-amplify-domain-subdomainsetting.md), ... ]
    }
}
```

### YAML<a name="aws-resource-amplify-domain-syntax.yaml"></a>

```
Type: AWS::Amplify::Domain
Properties:
  [AppId](#cfn-amplify-domain-appid): String
  [DomainName](#cfn-amplify-domain-domainname): String
  [SubDomainSettings](#cfn-amplify-domain-subdomainsettings):
    - [SubDomainSetting](aws-properties-amplify-domain-subdomainsetting.md)
```

## Properties<a name="aws-resource-amplify-domain-properties"></a>

`AppId`  <a name="cfn-amplify-domain-appid"></a>
 Unique Id for an Amplify App\.
*Required*: Yes
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DomainName`  <a name="cfn-amplify-domain-domainname"></a>
 Domain name for the Domain Association\.
*Required*: Yes
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubDomainSettings`  <a name="cfn-amplify-domain-subdomainsettings"></a>
 Setting structure for the Subdomain\.
*Required*: Yes
*Type*: List of [SubDomainSetting](aws-properties-amplify-domain-subdomainsetting.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-amplify-domain-return-values"></a>

### Fn::GetAtt<a name="aws-resource-amplify-domain-return-values-fn--getatt"></a>

#### <a name="aws-resource-amplify-domain-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
ARN for the Domain Association\.

`CertificateRecord`  <a name="CertificateRecord-fn::getatt"></a>
DNS Record for certificate verification\.

`DomainName`  <a name="DomainName-fn::getatt"></a>
Name of the domain\.

`DomainStatus`  <a name="DomainStatus-fn::getatt"></a>
Status fo the Domain Association\.

`StatusReason`  <a name="StatusReason-fn::getatt"></a>
Reason for the current status of the domain\.
