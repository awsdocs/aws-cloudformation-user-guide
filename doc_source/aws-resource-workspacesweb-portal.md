# AWS::WorkSpacesWeb::Portal<a name="aws-resource-workspacesweb-portal"></a>

This resource specifies a web portal, which users use to start browsing sessions\. A `Standard` web portal can't start browsing sessions unless you have at defined and associated an `IdentityProvider` and `NetworkSettings` resource\. An `IAM Identity Center` web portal does not require an `IdentityProvider` resource\.

For more information about web portals, see [What is Amazon WorkSpaces Web?](https://docs.aws.amazon.com/workspaces-web/latest/adminguide/what-is-workspaces-web.html.html)\.

## Syntax<a name="aws-resource-workspacesweb-portal-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-workspacesweb-portal-syntax.json"></a>

```
{
  "Type" : "AWS::WorkSpacesWeb::Portal",
  "Properties" : {
      "[AdditionalEncryptionContext](#cfn-workspacesweb-portal-additionalencryptioncontext)" : {Key: Value, ...},
      "[AuthenticationType](#cfn-workspacesweb-portal-authenticationtype)" : String,
      "[BrowserSettingsArn](#cfn-workspacesweb-portal-browsersettingsarn)" : String,
      "[CustomerManagedKey](#cfn-workspacesweb-portal-customermanagedkey)" : String,
      "[DisplayName](#cfn-workspacesweb-portal-displayname)" : String,
      "[IpAccessSettingsArn](#cfn-workspacesweb-portal-ipaccesssettingsarn)" : String,
      "[NetworkSettingsArn](#cfn-workspacesweb-portal-networksettingsarn)" : String,
      "[Tags](#cfn-workspacesweb-portal-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TrustStoreArn](#cfn-workspacesweb-portal-truststorearn)" : String,
      "[UserAccessLoggingSettingsArn](#cfn-workspacesweb-portal-useraccessloggingsettingsarn)" : String,
      "[UserSettingsArn](#cfn-workspacesweb-portal-usersettingsarn)" : String
    }
}
```

### YAML<a name="aws-resource-workspacesweb-portal-syntax.yaml"></a>

```
Type: AWS::WorkSpacesWeb::Portal
Properties: 
  [AdditionalEncryptionContext](#cfn-workspacesweb-portal-additionalencryptioncontext): 
    Key: Value
  [AuthenticationType](#cfn-workspacesweb-portal-authenticationtype): String
  [BrowserSettingsArn](#cfn-workspacesweb-portal-browsersettingsarn): String
  [CustomerManagedKey](#cfn-workspacesweb-portal-customermanagedkey): String
  [DisplayName](#cfn-workspacesweb-portal-displayname): String
  [IpAccessSettingsArn](#cfn-workspacesweb-portal-ipaccesssettingsarn): String
  [NetworkSettingsArn](#cfn-workspacesweb-portal-networksettingsarn): String
  [Tags](#cfn-workspacesweb-portal-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TrustStoreArn](#cfn-workspacesweb-portal-truststorearn): String
  [UserAccessLoggingSettingsArn](#cfn-workspacesweb-portal-useraccessloggingsettingsarn): String
  [UserSettingsArn](#cfn-workspacesweb-portal-usersettingsarn): String
```

## Properties<a name="aws-resource-workspacesweb-portal-properties"></a>

`AdditionalEncryptionContext`  <a name="cfn-workspacesweb-portal-additionalencryptioncontext"></a>
The additional encryption context of the portal\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AuthenticationType`  <a name="cfn-workspacesweb-portal-authenticationtype"></a>
The type of authentication integration points used when signing into the web portal\. Defaults to `Standard`\.  
`Standard` web portals are authenticated directly through your identity provider \(IdP\)\. User and group access to your web portal is controlled through your IdP\. You need to include an IdP resource in your template to integrate your IdP with your web portal\. Completing the configuration for your IdP requires exchanging WorkSpaces Web’s SP metadata with your IdP’s IdP metadata\. If your IdP requires the SP metadata first before returning the IdP metadata, you should follow these steps:  
1\. Create and deploy a CloudFormation template with a `Standard` portal with no `IdentityProvider` resource\.  
2\. Retrieve the SP metadata using `Fn:GetAtt`, the WorkSpaces Web console, or by the calling the `GetPortalServiceProviderMetadata` API\.  
3\. Submit the data to your IdP\.  
4\. Add an `IdentityProvider` resource to your CloudFormation template\.  
`IAM Identity Center` web portals are authenticated through AWS IAM Identity Center \(successor to AWS Single Sign\-On\)\. They provide additional features, such as IdP\-initiated authentication\. Identity sources \(including external identity provider integration\) and other identity provider information must be configured in IAM Identity Center\. User and group assignment must be done through the WorkSpaces Web console\. These cannot be configured in CloudFormation\.  
*Required*: No  
*Type*: String  
*Allowed values*: `IAM_Identity_Center | Standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BrowserSettingsArn`  <a name="cfn-workspacesweb-portal-browsersettingsarn"></a>
The ARN of the browser settings that is associated with this web portal\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=\/,.@-]+:[a-zA-Z0-9\-]+:[a-zA-Z0-9\-]*:[a-zA-Z0-9]{1,12}:[a-zA-Z]+(\/[a-fA-F0-9\-]{36})+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomerManagedKey`  <a name="cfn-workspacesweb-portal-customermanagedkey"></a>
The customer managed key of the web portal\.  
*Pattern*: `^arn:[\w+=\/,.@-]+:kms:[a-zA-Z0-9\-]*:[a-zA-Z0-9]{1,12}:key\/[a-zA-Z0-9-]+$`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DisplayName`  <a name="cfn-workspacesweb-portal-displayname"></a>
The name of the web portal\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpAccessSettingsArn`  <a name="cfn-workspacesweb-portal-ipaccesssettingsarn"></a>
The ARN of the IP access settings that is associated with the web portal\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=\/,.@-]+:[a-zA-Z0-9\-]+:[a-zA-Z0-9\-]*:[a-zA-Z0-9]{1,12}:[a-zA-Z]+(\/[a-fA-F0-9\-]{36})+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkSettingsArn`  <a name="cfn-workspacesweb-portal-networksettingsarn"></a>
The ARN of the network settings that is associated with the web portal\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=\/,.@-]+:[a-zA-Z0-9\-]+:[a-zA-Z0-9\-]*:[a-zA-Z0-9]{1,12}:[a-zA-Z]+(\/[a-fA-F0-9\-]{36})+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-workspacesweb-portal-tags"></a>
The tags to add to the web portal\. A tag is a key\-value pair\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustStoreArn`  <a name="cfn-workspacesweb-portal-truststorearn"></a>
The ARN of the trust store that is associated with the web portal\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=\/,.@-]+:[a-zA-Z0-9\-]+:[a-zA-Z0-9\-]*:[a-zA-Z0-9]{1,12}:[a-zA-Z]+(\/[a-fA-F0-9\-]{36})+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserAccessLoggingSettingsArn`  <a name="cfn-workspacesweb-portal-useraccessloggingsettingsarn"></a>
The ARN of the user access logging settings that is associated with the web portal\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=\/,.@-]+:[a-zA-Z0-9\-]+:[a-zA-Z0-9\-]*:[a-zA-Z0-9]{1,12}:[a-zA-Z]+(\/[a-fA-F0-9\-]{36})+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserSettingsArn`  <a name="cfn-workspacesweb-portal-usersettingsarn"></a>
The ARN of the user settings that is associated with the web portal\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=\/,.@-]+:[a-zA-Z0-9\-]+:[a-zA-Z0-9\-]*:[a-zA-Z0-9]{1,12}:[a-zA-Z]+(\/[a-fA-F0-9\-]{36})+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-workspacesweb-portal-return-values"></a>

### Ref<a name="aws-resource-workspacesweb-portal-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource's Amazon Resource Name \(ARN\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-workspacesweb-portal-return-values-fn--getatt"></a>

#### <a name="aws-resource-workspacesweb-portal-return-values-fn--getatt-fn--getatt"></a>

`BrowserType`  <a name="BrowserType-fn::getatt"></a>
The browser that users see when using a streaming session\.

`CreationDate`  <a name="CreationDate-fn::getatt"></a>
The creation date of the web portal\.

`PortalArn`  <a name="PortalArn-fn::getatt"></a>
The ARN of the web portal\.

`PortalEndpoint`  <a name="PortalEndpoint-fn::getatt"></a>
The endpoint URL of the web portal that users access in order to start streaming sessions\.

`PortalStatus`  <a name="PortalStatus-fn::getatt"></a>
The status of the web portal\.

`RendererType`  <a name="RendererType-fn::getatt"></a>
The renderer that is used in streaming sessions\.

`ServiceProviderSamlMetadata`  <a name="ServiceProviderSamlMetadata-fn::getatt"></a>
The SAML metadata of the service provider\.

`StatusReason`  <a name="StatusReason-fn::getatt"></a>
A message that explains why the web portal is in its current status\.