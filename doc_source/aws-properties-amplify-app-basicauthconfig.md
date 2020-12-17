# AWS::Amplify::App BasicAuthConfig<a name="aws-properties-amplify-app-basicauthconfig"></a>

Use the BasicAuthConfig property type to set password protection at an app level to all your branches\.

## Syntax<a name="aws-properties-amplify-app-basicauthconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplify-app-basicauthconfig-syntax.json"></a>

```
{
  "[EnableBasicAuth](#cfn-amplify-app-basicauthconfig-enablebasicauth)" : Boolean,
  "[Password](#cfn-amplify-app-basicauthconfig-password)" : String,
  "[Username](#cfn-amplify-app-basicauthconfig-username)" : String
}
```

### YAML<a name="aws-properties-amplify-app-basicauthconfig-syntax.yaml"></a>

```
  [EnableBasicAuth](#cfn-amplify-app-basicauthconfig-enablebasicauth): Boolean
  [Password](#cfn-amplify-app-basicauthconfig-password): String
  [Username](#cfn-amplify-app-basicauthconfig-username): String
```

## Properties<a name="aws-properties-amplify-app-basicauthconfig-properties"></a>

`EnableBasicAuth`  <a name="cfn-amplify-app-basicauthconfig-enablebasicauth"></a>
 Enables basic authorization for the Amplify app's branches\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-amplify-app-basicauthconfig-password"></a>
The password for basic authorization\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-amplify-app-basicauthconfig-username"></a>
The user name for basic authorization\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)