# AWS::Amplify::Domain SubDomainSetting<a name="aws-properties-amplify-domain-subdomainsetting"></a>

 The SubDomainSetting property type allows you to connect a subdomain \(e\.g\. foo\.yourdomain\.com\) to a specific branch\. 

## Syntax<a name="aws-properties-amplify-domain-subdomainsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplify-domain-subdomainsetting-syntax.json"></a>

```
{
  "[BranchName](#cfn-amplify-domain-subdomainsetting-branchname)" : String,
  "[Prefix](#cfn-amplify-domain-subdomainsetting-prefix)" : String
}
```

### YAML<a name="aws-properties-amplify-domain-subdomainsetting-syntax.yaml"></a>

```
  [BranchName](#cfn-amplify-domain-subdomainsetting-branchname): String
  [Prefix](#cfn-amplify-domain-subdomainsetting-prefix): String
```

## Properties<a name="aws-properties-amplify-domain-subdomainsetting-properties"></a>

`BranchName`  <a name="cfn-amplify-domain-subdomainsetting-branchname"></a>
 Branch name setting for the Subdomain\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-amplify-domain-subdomainsetting-prefix"></a>
 Prefix setting for the Subdomain\.   
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
