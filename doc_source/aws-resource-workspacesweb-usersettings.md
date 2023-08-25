# AWS::WorkSpacesWeb::UserSettings<a name="aws-resource-workspacesweb-usersettings"></a>

This resource specifies user settings that can be associated with a web portal\. Once associated with a web portal, user settings control how users can transfer data between a streaming session and the their local devices\. 

## Syntax<a name="aws-resource-workspacesweb-usersettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-workspacesweb-usersettings-syntax.json"></a>

```
{
  "Type" : "AWS::WorkSpacesWeb::UserSettings",
  "Properties" : {
      "[CopyAllowed](#cfn-workspacesweb-usersettings-copyallowed)" : String,
      "[DisconnectTimeoutInMinutes](#cfn-workspacesweb-usersettings-disconnecttimeoutinminutes)" : Double,
      "[DownloadAllowed](#cfn-workspacesweb-usersettings-downloadallowed)" : String,
      "[IdleDisconnectTimeoutInMinutes](#cfn-workspacesweb-usersettings-idledisconnecttimeoutinminutes)" : Double,
      "[PasteAllowed](#cfn-workspacesweb-usersettings-pasteallowed)" : String,
      "[PrintAllowed](#cfn-workspacesweb-usersettings-printallowed)" : String,
      "[Tags](#cfn-workspacesweb-usersettings-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UploadAllowed](#cfn-workspacesweb-usersettings-uploadallowed)" : String
    }
}
```

### YAML<a name="aws-resource-workspacesweb-usersettings-syntax.yaml"></a>

```
Type: AWS::WorkSpacesWeb::UserSettings
Properties: 
  [CopyAllowed](#cfn-workspacesweb-usersettings-copyallowed): String
  [DisconnectTimeoutInMinutes](#cfn-workspacesweb-usersettings-disconnecttimeoutinminutes): Double
  [DownloadAllowed](#cfn-workspacesweb-usersettings-downloadallowed): String
  [IdleDisconnectTimeoutInMinutes](#cfn-workspacesweb-usersettings-idledisconnecttimeoutinminutes): Double
  [PasteAllowed](#cfn-workspacesweb-usersettings-pasteallowed): String
  [PrintAllowed](#cfn-workspacesweb-usersettings-printallowed): String
  [Tags](#cfn-workspacesweb-usersettings-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UploadAllowed](#cfn-workspacesweb-usersettings-uploadallowed): String
```

## Properties<a name="aws-resource-workspacesweb-usersettings-properties"></a>

`CopyAllowed`  <a name="cfn-workspacesweb-usersettings-copyallowed"></a>
Specifies whether the user can copy text from the streaming session to the local device\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisconnectTimeoutInMinutes`  <a name="cfn-workspacesweb-usersettings-disconnecttimeoutinminutes"></a>
The amount of time that a streaming session remains active after users disconnect\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DownloadAllowed`  <a name="cfn-workspacesweb-usersettings-downloadallowed"></a>
Specifies whether the user can download files from the streaming session to the local device\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdleDisconnectTimeoutInMinutes`  <a name="cfn-workspacesweb-usersettings-idledisconnecttimeoutinminutes"></a>
The amount of time that users can be idle \(inactive\) before they are disconnected from their streaming session and the disconnect timeout interval begins\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `60`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PasteAllowed`  <a name="cfn-workspacesweb-usersettings-pasteallowed"></a>
Specifies whether the user can paste text from the local device to the streaming session\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrintAllowed`  <a name="cfn-workspacesweb-usersettings-printallowed"></a>
Specifies whether the user can print to the local device\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-workspacesweb-usersettings-tags"></a>
The tags to add to the user settings resource\. A tag is a key\-value pair\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UploadAllowed`  <a name="cfn-workspacesweb-usersettings-uploadallowed"></a>
Specifies whether the user can upload files from the local device to the streaming session\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-workspacesweb-usersettings-return-values"></a>

### Ref<a name="aws-resource-workspacesweb-usersettings-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource's Amazon Resource Name \(ARN\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-workspacesweb-usersettings-return-values-fn--getatt"></a>

#### <a name="aws-resource-workspacesweb-usersettings-return-values-fn--getatt-fn--getatt"></a>

`AssociatedPortalArns`  <a name="AssociatedPortalArns-fn::getatt"></a>
A list of web portal ARNs that this user settings resource is associated with\.

`UserSettingsArn`  <a name="UserSettingsArn-fn::getatt"></a>
The ARN of the user settings\.