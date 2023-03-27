# AWS::IAM::OIDCProvider<a name="aws-resource-iam-oidcprovider"></a>

Creates or updates an IAM entity to describe an identity provider \(IdP\) that supports [OpenID Connect \(OIDC\)](http://openid.net/connect/)\.

The OIDC provider that you create with this operation can be used as a principal in a role's trust policy\. Such a policy establishes a trust relationship between AWS and the OIDC provider\.

When you create the IAM OIDC provider, you specify the following:
+ The URL of the OIDC identity provider \(IdP\) to trust
+ A list of client IDs \(also known as audiences\) that identify the application or applications that are allowed to authenticate using the OIDC provider
+ A list of tags that are attached to the specified IAM OIDC provider
+ A list of thumbprints of one or more server certificates that the IdP uses

You get all of this information from the OIDC IdP that you want to use to access AWS\.

When you update the IAM OIDC provider, you specify the following:
+ The URL of the OIDC identity provider \(IdP\) to trust
+ A list of client IDs \(also known as audiences\) that replaces the existing list of client IDs associated with the OIDC IdP
+ A list of tags that replaces the existing list of tags attached to the specified IAM OIDC provider
+ A list of thumbprints that replaces the existing list of server certificates thumbprints that the IdP uses

**Note**  
The trust for the OIDC provider is derived from the IAM provider that this operation creates\. Therefore, it is best to limit access to the [CreateOpenIDConnectProvider](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateOpenIDConnectProvider.html) operation to highly privileged users\.

## Syntax<a name="aws-resource-iam-oidcprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-oidcprovider-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::OIDCProvider",
  "Properties" : {
      "[ClientIdList](#cfn-iam-oidcprovider-clientidlist)" : [ String, ... ],
      "[Tags](#cfn-iam-oidcprovider-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[ThumbprintList](#cfn-iam-oidcprovider-thumbprintlist)" : [ String, ... ],
      "[Url](#cfn-iam-oidcprovider-url)" : String
    }
}
```

### YAML<a name="aws-resource-iam-oidcprovider-syntax.yaml"></a>

```
Type: AWS::IAM::OIDCProvider
Properties: 
  [ClientIdList](#cfn-iam-oidcprovider-clientidlist): 
    - String
  [Tags](#cfn-iam-oidcprovider-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [ThumbprintList](#cfn-iam-oidcprovider-thumbprintlist): 
    - String
  [Url](#cfn-iam-oidcprovider-url): String
```

## Properties<a name="aws-resource-iam-oidcprovider-properties"></a>

`ClientIdList`  <a name="cfn-iam-oidcprovider-clientidlist"></a>
A list of client IDs \(also known as audiences\) that are associated with the specified IAM OIDC provider resource object\. For more information, see [CreateOpenIDConnectProvider](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateOpenIDConnectProvider.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iam-oidcprovider-tags"></a>
A list of tags that are attached to the specified IAM OIDC provider\. The returned list of tags is sorted by tag key\. For more information about tagging, see [Tagging IAM resources](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_tags.html) in the *IAM User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThumbprintList`  <a name="cfn-iam-oidcprovider-thumbprintlist"></a>
A list of certificate thumbprints that are associated with the specified IAM OIDC provider resource object\. For more information, see [CreateOpenIDConnectProvider](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateOpenIDConnectProvider.html)\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-iam-oidcprovider-url"></a>
The URL that the IAM OIDC provider resource object is associated with\. For more information, see [CreateOpenIDConnectProvider](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateOpenIDConnectProvider.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iam-oidcprovider-return-values"></a>

### Ref<a name="aws-resource-iam-oidcprovider-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iam-oidcprovider-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iam-oidcprovider-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the specified `AWS::IAM::OIDCProvider` resource\.