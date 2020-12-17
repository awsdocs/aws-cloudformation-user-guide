# AWS::AppStream::Stack UserSetting<a name="aws-properties-appstream-stack-usersetting"></a>

Specifies an action and whether the action is enabled or disabled for users during their streaming sessions\.

## Syntax<a name="aws-properties-appstream-stack-usersetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-stack-usersetting-syntax.json"></a>

```
{
  "[Action](#cfn-appstream-stack-usersetting-action)" : String,
  "[Permission](#cfn-appstream-stack-usersetting-permission)" : String
}
```

### YAML<a name="aws-properties-appstream-stack-usersetting-syntax.yaml"></a>

```
  [Action](#cfn-appstream-stack-usersetting-action): String
  [Permission](#cfn-appstream-stack-usersetting-permission): String
```

## Properties<a name="aws-properties-appstream-stack-usersetting-properties"></a>

`Action`  <a name="cfn-appstream-stack-usersetting-action"></a>
The action that is enabled or disabled\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CLIPBOARD_COPY_FROM_LOCAL_DEVICE | CLIPBOARD_COPY_TO_LOCAL_DEVICE | FILE_DOWNLOAD | FILE_UPLOAD | PRINTING_TO_LOCAL_DEVICE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permission`  <a name="cfn-appstream-stack-usersetting-permission"></a>
Indicates whether the action is enabled or disabled\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)