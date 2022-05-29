# AWS::Cognito::UserPoolDomain<a name="aws-resource-cognito-userpooldomain"></a>

The AWS::Cognito::UserPoolDomain resource creates a new domain for a user pool\.

## Syntax<a name="aws-resource-cognito-userpooldomain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpooldomain-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolDomain",
  "Properties" : {
      "[CustomDomainConfig](#cfn-cognito-userpooldomain-customdomainconfig)" : CustomDomainConfigType,
      "[Domain](#cfn-cognito-userpooldomain-domain)" : String,
      "[UserPoolId](#cfn-cognito-userpooldomain-userpoolid)" : String
    }
}
```

### YAML<a name="aws-resource-cognito-userpooldomain-syntax.yaml"></a>

```
Type: AWS::Cognito::UserPoolDomain
Properties: 
  [CustomDomainConfig](#cfn-cognito-userpooldomain-customdomainconfig): 
    CustomDomainConfigType
  [Domain](#cfn-cognito-userpooldomain-domain): String
  [UserPoolId](#cfn-cognito-userpooldomain-userpoolid): String
```

## Properties<a name="aws-resource-cognito-userpooldomain-properties"></a>

`CustomDomainConfig`  <a name="cfn-cognito-userpooldomain-customdomainconfig"></a>
The configuration for a custom domain that hosts the sign\-up and sign\-in pages for your application\. Use this object to specify an SSL certificate that is managed by ACM\.  
*Required*: No  
*Type*: [CustomDomainConfigType](aws-properties-cognito-userpooldomain-customdomainconfigtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Domain`  <a name="cfn-cognito-userpooldomain-domain"></a>
The domain name for the domain that hosts the sign\-up and sign\-in pages for your application\. For example: `auth.example.com`\. If you're using a prefix domain, this field denotes the first part of the domain before `.auth.[region].amazoncognito.com`\.  
This string can include only lowercase letters, numbers, and hyphens\. Don't use a hyphen for the first or last character\. Use periods to separate subdomain names\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-z0-9](?:[a-z0-9\-]{0,61}[a-z0-9])?$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserPoolId`  <a name="cfn-cognito-userpooldomain-userpoolid"></a>
The user pool ID for the user pool where you want to associate a user pool domain\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cognito-userpooldomain-return-values"></a>

### Ref<a name="aws-resource-cognito-userpooldomain-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns physicalResourceId, which is “Domain"\. For example:

 `{ "Ref": "your-test-domain" }` 

For the Amazon Cognito user pool domain `your-test-domain`, Ref returns the name of the user pool domain\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cognito-userpooldomain--examples"></a>



### Creating a new custom domain for a user pool<a name="aws-resource-cognito-userpooldomain--examples--Creating_a_new_custom_domain_for_a_user_pool"></a>

The following example creates a custom domain, "my\-test\-user\-pool\-domain", in the referenced user pool\.

#### JSON<a name="aws-resource-cognito-userpooldomain--examples--Creating_a_new_custom_domain_for_a_user_pool--json"></a>

```
{
   "UserPoolDomain":{
      "Type":"AWS::Cognito::UserPoolDomain",
      "Properties":{
         "UserPoolId":{
            "Ref":"UserPool"
         },
         "Domain":"my-test-user-pool-domain.myapplication.com",
         "CustomDomainConfig":{
            "CertificateArn":{
               "Ref":"CertificateArn"
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-cognito-userpooldomain--examples--Creating_a_new_custom_domain_for_a_user_pool--yaml"></a>

```
UserPoolDomain: 
  Type: AWS::Cognito::UserPoolDomain 
  Properties:
    UserPoolId: !Ref UserPool 
    Domain: "my-test-user-pool-domain.myapplication.com"
    CustomDomainConfig: 
      CertificateArn: !Ref CertificateArn
```

### Creating a new default domain for a user pool<a name="aws-resource-cognito-userpooldomain--examples--Creating_a_new_default_domain_for_a_user_pool"></a>

The following example creates a new default domain, "my\-test\-user\-pool\-domain", in the referenced user pool\.

#### JSON<a name="aws-resource-cognito-userpooldomain--examples--Creating_a_new_default_domain_for_a_user_pool--json"></a>

```
{
   "UserPoolDomain":{
      "Type":"AWS::Cognito::UserPoolDomain",
      "Properties":{
         "UserPoolId":{
            "Ref":"UserPool"
         },
         "Domain":"my-test-user-pool-domain"
      }
   }
}
```

#### YAML<a name="aws-resource-cognito-userpooldomain--examples--Creating_a_new_default_domain_for_a_user_pool--yaml"></a>

```
UserPoolDomain: 
  Type: AWS::Cognito::UserPoolDomain 
  Properties:
    UserPoolId: !Ref UserPool 
    Domain: "my-test-user-pool-domain"
```