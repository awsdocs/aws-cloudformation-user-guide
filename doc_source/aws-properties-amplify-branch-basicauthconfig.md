# AWS::Amplify::Branch BasicAuthConfig<a name="aws-properties-amplify-branch-basicauthconfig"></a>

Use the BasicAuthConfig property type to set password protection for a specific branch\.

## Syntax<a name="aws-properties-amplify-branch-basicauthconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplify-branch-basicauthconfig-syntax.json"></a>

```
{
  "[EnableBasicAuth](#cfn-amplify-branch-basicauthconfig-enablebasicauth)" : Boolean,
  "[Password](#cfn-amplify-branch-basicauthconfig-password)" : String,
  "[Username](#cfn-amplify-branch-basicauthconfig-username)" : String
}
```

### YAML<a name="aws-properties-amplify-branch-basicauthconfig-syntax.yaml"></a>

```
  [EnableBasicAuth](#cfn-amplify-branch-basicauthconfig-enablebasicauth): Boolean
  [Password](#cfn-amplify-branch-basicauthconfig-password): String
  [Username](#cfn-amplify-branch-basicauthconfig-username): String
```

## Properties<a name="aws-properties-amplify-branch-basicauthconfig-properties"></a>

`EnableBasicAuth`  <a name="cfn-amplify-branch-basicauthconfig-enablebasicauth"></a>
 Enables basic authorization for the branch\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-amplify-branch-basicauthconfig-password"></a>
The password for basic authorization\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-amplify-branch-basicauthconfig-username"></a>
The user name for basic authorization\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)