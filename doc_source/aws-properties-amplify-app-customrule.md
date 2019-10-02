# AWS::Amplify::App CustomRule<a name="aws-properties-amplify-app-customrule"></a>

 The CustomRule property type allows you to specify redirects, rewrites, and reverse proxies\. Redirects enable a web app to reroute navigation from one URL to another\. 

## Syntax<a name="aws-properties-amplify-app-customrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplify-app-customrule-syntax.json"></a>

```
{
  "[Condition](#cfn-amplify-app-customrule-condition)" : String,
  "[Source](#cfn-amplify-app-customrule-source)" : String,
  "[Status](#cfn-amplify-app-customrule-status)" : String,
  "[Target](#cfn-amplify-app-customrule-target)" : String
}
```

### YAML<a name="aws-properties-amplify-app-customrule-syntax.yaml"></a>

```
  [Condition](#cfn-amplify-app-customrule-condition): String
  [Source](#cfn-amplify-app-customrule-source): String
  [Status](#cfn-amplify-app-customrule-status): String
  [Target](#cfn-amplify-app-customrule-target): String
```

## Properties<a name="aws-properties-amplify-app-customrule-properties"></a>

`Condition`  <a name="cfn-amplify-app-customrule-condition"></a>
 The condition for a URL rewrite or redirect rule, e\.g\. country code\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-amplify-app-customrule-source"></a>
 The source pattern for a URL rewrite or redirect rule\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-amplify-app-customrule-status"></a>
 The status code for a URL rewrite or redirect rule\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-amplify-app-customrule-target"></a>
 The target pattern for a URL rewrite or redirect rule\.   
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
