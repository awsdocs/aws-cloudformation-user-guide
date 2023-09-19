# AWS::WorkSpacesWeb::UserSettings CookieSpecification<a name="aws-properties-workspacesweb-usersettings-cookiespecification"></a>

Specifies a single cookie or set of cookies in an end user's browser\.

## Syntax<a name="aws-properties-workspacesweb-usersettings-cookiespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-workspacesweb-usersettings-cookiespecification-syntax.json"></a>

```
{
  "[Domain](#cfn-workspacesweb-usersettings-cookiespecification-domain)" : String,
  "[Name](#cfn-workspacesweb-usersettings-cookiespecification-name)" : String,
  "[Path](#cfn-workspacesweb-usersettings-cookiespecification-path)" : String
}
```

### YAML<a name="aws-properties-workspacesweb-usersettings-cookiespecification-syntax.yaml"></a>

```
  [Domain](#cfn-workspacesweb-usersettings-cookiespecification-domain): String
  [Name](#cfn-workspacesweb-usersettings-cookiespecification-name): String
  [Path](#cfn-workspacesweb-usersettings-cookiespecification-path): String
```

## Properties<a name="aws-properties-workspacesweb-usersettings-cookiespecification-properties"></a>

`Domain`  <a name="cfn-workspacesweb-usersettings-cookiespecification-domain"></a>
The domain of the cookie\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `253`  
*Pattern*: `(\.?)(?:[a-z0-9](?:[a-z0-9-]{0,61}[a-z0-9])?\.)*[a-z0-9][a-z0-9-]{0,61}[a-z0-9]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-workspacesweb-usersettings-cookiespecification-name"></a>
The name of the cookie\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-workspacesweb-usersettings-cookiespecification-path"></a>
The path of the cookie\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2000`  
*Pattern*: `/(\S)*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)