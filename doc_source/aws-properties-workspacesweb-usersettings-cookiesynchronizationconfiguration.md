# AWS::WorkSpacesWeb::UserSettings CookieSynchronizationConfiguration<a name="aws-properties-workspacesweb-usersettings-cookiesynchronizationconfiguration"></a>

The configuration that specifies which cookies should be synchronized from the end user's local browser to the remote browser\.

## Syntax<a name="aws-properties-workspacesweb-usersettings-cookiesynchronizationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-workspacesweb-usersettings-cookiesynchronizationconfiguration-syntax.json"></a>

```
{
  "[Allowlist](#cfn-workspacesweb-usersettings-cookiesynchronizationconfiguration-allowlist)" : [ CookieSpecification, ... ],
  "[Blocklist](#cfn-workspacesweb-usersettings-cookiesynchronizationconfiguration-blocklist)" : [ CookieSpecification, ... ]
}
```

### YAML<a name="aws-properties-workspacesweb-usersettings-cookiesynchronizationconfiguration-syntax.yaml"></a>

```
  [Allowlist](#cfn-workspacesweb-usersettings-cookiesynchronizationconfiguration-allowlist): 
    - CookieSpecification
  [Blocklist](#cfn-workspacesweb-usersettings-cookiesynchronizationconfiguration-blocklist): 
    - CookieSpecification
```

## Properties<a name="aws-properties-workspacesweb-usersettings-cookiesynchronizationconfiguration-properties"></a>

`Allowlist`  <a name="cfn-workspacesweb-usersettings-cookiesynchronizationconfiguration-allowlist"></a>
The list of cookie specifications that are allowed to be synchronized to the remote browser\.  
*Required*: Yes  
*Type*: List of [CookieSpecification](aws-properties-workspacesweb-usersettings-cookiespecification.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Blocklist`  <a name="cfn-workspacesweb-usersettings-cookiesynchronizationconfiguration-blocklist"></a>
The list of cookie specifications that are blocked from being synchronized to the remote browser\.  
*Required*: No  
*Type*: List of [CookieSpecification](aws-properties-workspacesweb-usersettings-cookiespecification.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)