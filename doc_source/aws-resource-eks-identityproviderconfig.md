# AWS::EKS::IdentityProviderConfig<a name="aws-resource-eks-identityproviderconfig"></a>

Associate an identity provider configuration to a cluster\.

If you want to authenticate identities using an identity provider, you can create an identity provider configuration and associate it to your cluster\. After configuring authentication to your cluster you can create Kubernetes `roles` and `clusterroles` to assign permissions to the roles, and then bind the roles to the identities using Kubernetes `rolebindings` and `clusterrolebindings`\. For more information see [Using RBAC Authorization](https://kubernetes.io/docs/reference/access-authn-authz/rbac/) in the Kubernetes documentation\.

## Syntax<a name="aws-resource-eks-identityproviderconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-eks-identityproviderconfig-syntax.json"></a>

```
{
  "Type" : "AWS::EKS::IdentityProviderConfig",
  "Properties" : {
      "[ClusterName](#cfn-eks-identityproviderconfig-clustername)" : String,
      "[IdentityProviderConfigName](#cfn-eks-identityproviderconfig-identityproviderconfigname)" : String,
      "[Oidc](#cfn-eks-identityproviderconfig-oidc)" : OidcIdentityProviderConfig,
      "[Tags](#cfn-eks-identityproviderconfig-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-eks-identityproviderconfig-type)" : String
    }
}
```

### YAML<a name="aws-resource-eks-identityproviderconfig-syntax.yaml"></a>

```
Type: AWS::EKS::IdentityProviderConfig
Properties: 
  [ClusterName](#cfn-eks-identityproviderconfig-clustername): String
  [IdentityProviderConfigName](#cfn-eks-identityproviderconfig-identityproviderconfigname): String
  [Oidc](#cfn-eks-identityproviderconfig-oidc): 
    OidcIdentityProviderConfig
  [Tags](#cfn-eks-identityproviderconfig-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-eks-identityproviderconfig-type): String
```

## Properties<a name="aws-resource-eks-identityproviderconfig-properties"></a>

`ClusterName`  <a name="cfn-eks-identityproviderconfig-clustername"></a>
The cluster that the configuration is associated to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IdentityProviderConfigName`  <a name="cfn-eks-identityproviderconfig-identityproviderconfigname"></a>
The name of the configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Oidc`  <a name="cfn-eks-identityproviderconfig-oidc"></a>
An object representing an OpenID Connect \(OIDC\) identity provider configuration\.  
*Required*: No  
*Type*: [OidcIdentityProviderConfig](aws-properties-eks-identityproviderconfig-oidcidentityproviderconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-eks-identityproviderconfig-tags"></a>
The metadata to apply to the provider configuration to assist with categorization and organization\. Each tag consists of a key and an optional value\. You define both\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-eks-identityproviderconfig-type"></a>
The type of the identity provider configuration\. The only type available is `oidc`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-eks-identityproviderconfig-return-values"></a>

### Ref<a name="aws-resource-eks-identityproviderconfig-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myIdentityProviderConfig" }` 

For the IdentityProviderConfig, Ref returns the physical resource ID of the config\. For example, `cluster-name/oidc/identity-provider-config-name`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-eks-identityproviderconfig-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-eks-identityproviderconfig-return-values-fn--getatt-fn--getatt"></a>

`IdentityProviderConfigArn`  <a name="IdentityProviderConfigArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) associated with the identity provider config\.

## Remarks<a name="aws-resource-eks-identityproviderconfig--remarks"></a>

 *Creating an identity provider config and Fargate profile resources in the same template\.* 

If AWS CloudFormation attempts to create both resources at the same time, resource creation fails\. If you want to create both resources in the same template, then add the `DependsOn` property in your template, as shown in the examples\.

## Examples<a name="aws-resource-eks-identityproviderconfig--examples"></a>

### Create an identity provider config<a name="aws-resource-eks-identityproviderconfig--examples--Create_an_identity_provider_config"></a>

The following example creates a an identity provider config\. If you're not creating an `EKSFargateProfile` in the same template, remove the `"DependsOn"` line in the following example\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-fargateprofile.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-fargateprofile.html)\.

#### JSON<a name="aws-resource-eks-identityproviderconfig--examples--Create_an_identity_provider_config--json"></a>

```
{
  "EKSIdpConfig": {
    "DependsOn": "EKSFargateProfile",
    "Type": "AWS::EKS::IdentityProviderConfig",
    "Properties": {
      "ClusterName": "my-cluster",
      "Type": "oidc",
      "Oidc": {
        "ClientId": "kubernetes",
        "IssuerUrl": "https://example.com"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-eks-identityproviderconfig--examples--Create_an_identity_provider_config--yaml"></a>

```
Resources:
  EKSIdpConfig:
    DependsOn: EKSFargateProfile
    Type: AWS::EKS::IdentityProviderConfig
    Properties:
      ClusterName: my-cluster
      Type: oidc
      Oidc:
        ClientId: "kubernetes"
        IssuerUrl: "https://example.com"
```

## See also<a name="aws-resource-eks-identityproviderconfig--seealso"></a>
+  [Authenticating users for your cluster from an OpenID Connect identity provider](https://docs.aws.amazon.com/eks/latest/userguide/authenticate-oidc-identity-provider.html) in the *Amazon EKS User Guide *\.
+  [AssociateIdentityProviderConfig](https://docs.aws.amazon.com/eks/latest/APIReference/API_AssociateIdentityProviderConfig.html) in the *Amazon EKS API Reference *\.