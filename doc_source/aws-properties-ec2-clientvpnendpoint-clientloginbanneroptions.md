# AWS::EC2::ClientVpnEndpoint ClientLoginBannerOptions<a name="aws-properties-ec2-clientvpnendpoint-clientloginbanneroptions"></a>

Options for enabling a customizable text banner that will be displayed on AWS provided clients when a VPN session is established\.

## Syntax<a name="aws-properties-ec2-clientvpnendpoint-clientloginbanneroptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-clientvpnendpoint-clientloginbanneroptions-syntax.json"></a>

```
{
  "[BannerText](#cfn-ec2-clientvpnendpoint-clientloginbanneroptions-bannertext)" : String,
  "[Enabled](#cfn-ec2-clientvpnendpoint-clientloginbanneroptions-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-clientvpnendpoint-clientloginbanneroptions-syntax.yaml"></a>

```
  [BannerText](#cfn-ec2-clientvpnendpoint-clientloginbanneroptions-bannertext): String
  [Enabled](#cfn-ec2-clientvpnendpoint-clientloginbanneroptions-enabled): Boolean
```

## Properties<a name="aws-properties-ec2-clientvpnendpoint-clientloginbanneroptions-properties"></a>

`BannerText`  <a name="cfn-ec2-clientvpnendpoint-clientloginbanneroptions-bannertext"></a>
Customizable text that will be displayed in a banner on AWS provided clients when a VPN session is established\. UTF\-8 encoded characters only\. Maximum of 1400 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-ec2-clientvpnendpoint-clientloginbanneroptions-enabled"></a>
Enable or disable a customizable text banner that will be displayed on AWS provided clients when a VPN session is established\.  
Valid values: `true | false`   
Default value: `false`   
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)