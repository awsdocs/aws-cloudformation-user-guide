# AWS::WorkSpacesWeb::IpAccessSettings IpRule<a name="aws-properties-workspacesweb-ipaccesssettings-iprule"></a>

The IP rules of the IP access settings\.

## Syntax<a name="aws-properties-workspacesweb-ipaccesssettings-iprule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-workspacesweb-ipaccesssettings-iprule-syntax.json"></a>

```
{
  "[Description](#cfn-workspacesweb-ipaccesssettings-iprule-description)" : String,
  "[IpRange](#cfn-workspacesweb-ipaccesssettings-iprule-iprange)" : String
}
```

### YAML<a name="aws-properties-workspacesweb-ipaccesssettings-iprule-syntax.yaml"></a>

```
  [Description](#cfn-workspacesweb-ipaccesssettings-iprule-description): String
  [IpRange](#cfn-workspacesweb-ipaccesssettings-iprule-iprange): String
```

## Properties<a name="aws-properties-workspacesweb-ipaccesssettings-iprule-properties"></a>

`Description`  <a name="cfn-workspacesweb-ipaccesssettings-iprule-description"></a>
The description of the IP rule\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpRange`  <a name="cfn-workspacesweb-ipaccesssettings-iprule-iprange"></a>
The IP range of the IP rule\. This can either be a single IP address or a range using CIDR notation\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}(?:/([0-9]|[12][0-9]|3[0-2])|)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)