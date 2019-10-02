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
 Enables Basic Auth for the branch\.   
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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`
