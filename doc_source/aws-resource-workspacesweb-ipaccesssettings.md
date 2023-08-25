# AWS::WorkSpacesWeb::IpAccessSettings<a name="aws-resource-workspacesweb-ipaccesssettings"></a>

This resource specifies IP access settings that can be associated with a web portal\. For more information, see [Set up IP access controls \(optional\)](https://docs.aws.amazon.com/workspaces-web/latest/adminguide/ip-access-controls.html)\.

## Syntax<a name="aws-resource-workspacesweb-ipaccesssettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-workspacesweb-ipaccesssettings-syntax.json"></a>

```
{
  "Type" : "AWS::WorkSpacesWeb::IpAccessSettings",
  "Properties" : {
      "[AdditionalEncryptionContext](#cfn-workspacesweb-ipaccesssettings-additionalencryptioncontext)" : {Key: Value, ...},
      "[CustomerManagedKey](#cfn-workspacesweb-ipaccesssettings-customermanagedkey)" : String,
      "[Description](#cfn-workspacesweb-ipaccesssettings-description)" : String,
      "[DisplayName](#cfn-workspacesweb-ipaccesssettings-displayname)" : String,
      "[IpRules](#cfn-workspacesweb-ipaccesssettings-iprules)" : [ IpRule, ... ],
      "[Tags](#cfn-workspacesweb-ipaccesssettings-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-workspacesweb-ipaccesssettings-syntax.yaml"></a>

```
Type: AWS::WorkSpacesWeb::IpAccessSettings
Properties: 
  [AdditionalEncryptionContext](#cfn-workspacesweb-ipaccesssettings-additionalencryptioncontext): 
    Key: Value
  [CustomerManagedKey](#cfn-workspacesweb-ipaccesssettings-customermanagedkey): String
  [Description](#cfn-workspacesweb-ipaccesssettings-description): String
  [DisplayName](#cfn-workspacesweb-ipaccesssettings-displayname): String
  [IpRules](#cfn-workspacesweb-ipaccesssettings-iprules): 
    - IpRule
  [Tags](#cfn-workspacesweb-ipaccesssettings-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-workspacesweb-ipaccesssettings-properties"></a>

`AdditionalEncryptionContext`  <a name="cfn-workspacesweb-ipaccesssettings-additionalencryptioncontext"></a>
Additional encryption context of the IP access settings\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CustomerManagedKey`  <a name="cfn-workspacesweb-ipaccesssettings-customermanagedkey"></a>
The custom managed key of the IP access settings\.  
*Pattern*: `^arn:[\w+=\/,.@-]+:kms:[a-zA-Z0-9\-]*:[a-zA-Z0-9]{1,12}:key\/[a-zA-Z0-9-]+$`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-workspacesweb-ipaccesssettings-description"></a>
The description of the IP access settings\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-workspacesweb-ipaccesssettings-displayname"></a>
 The display name of the IP access settings\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpRules`  <a name="cfn-workspacesweb-ipaccesssettings-iprules"></a>
The IP rules of the IP access settings\.  
*Required*: Yes  
*Type*: List of [IpRule](aws-properties-workspacesweb-ipaccesssettings-iprule.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-workspacesweb-ipaccesssettings-tags"></a>
The tags to add to the browser settings resource\. A tag is a key\-value pair\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-workspacesweb-ipaccesssettings-return-values"></a>

### Ref<a name="aws-resource-workspacesweb-ipaccesssettings-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource's Amazon Resource Name \(ARN\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-workspacesweb-ipaccesssettings-return-values-fn--getatt"></a>

#### <a name="aws-resource-workspacesweb-ipaccesssettings-return-values-fn--getatt-fn--getatt"></a>

`AssociatedPortalArns`  <a name="AssociatedPortalArns-fn::getatt"></a>
A list of web portal ARNs that this IP access settings resource is associated with\.

`CreationDate`  <a name="CreationDate-fn::getatt"></a>
The creation date timestamp of the IP access settings\.

`IpAccessSettingsArn`  <a name="IpAccessSettingsArn-fn::getatt"></a>
The ARN of the IP access settings resource\.