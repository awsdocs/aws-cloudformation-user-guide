# AWS::EC2::VerifiedAccessTrustProvider<a name="aws-resource-ec2-verifiedaccesstrustprovider"></a>

Describes a Verified Access trust provider\.

## Syntax<a name="aws-resource-ec2-verifiedaccesstrustprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-verifiedaccesstrustprovider-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VerifiedAccessTrustProvider",
  "Properties" : {
      "[Description](#cfn-ec2-verifiedaccesstrustprovider-description)" : String,
      "[DeviceOptions](#cfn-ec2-verifiedaccesstrustprovider-deviceoptions)" : DeviceOptions,
      "[DeviceTrustProviderType](#cfn-ec2-verifiedaccesstrustprovider-devicetrustprovidertype)" : String,
      "[OidcOptions](#cfn-ec2-verifiedaccesstrustprovider-oidcoptions)" : OidcOptions,
      "[PolicyReferenceName](#cfn-ec2-verifiedaccesstrustprovider-policyreferencename)" : String,
      "[Tags](#cfn-ec2-verifiedaccesstrustprovider-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TrustProviderType](#cfn-ec2-verifiedaccesstrustprovider-trustprovidertype)" : String,
      "[UserTrustProviderType](#cfn-ec2-verifiedaccesstrustprovider-usertrustprovidertype)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-verifiedaccesstrustprovider-syntax.yaml"></a>

```
Type: AWS::EC2::VerifiedAccessTrustProvider
Properties: 
  [Description](#cfn-ec2-verifiedaccesstrustprovider-description): String
  [DeviceOptions](#cfn-ec2-verifiedaccesstrustprovider-deviceoptions): 
    DeviceOptions
  [DeviceTrustProviderType](#cfn-ec2-verifiedaccesstrustprovider-devicetrustprovidertype): String
  [OidcOptions](#cfn-ec2-verifiedaccesstrustprovider-oidcoptions): 
    OidcOptions
  [PolicyReferenceName](#cfn-ec2-verifiedaccesstrustprovider-policyreferencename): String
  [Tags](#cfn-ec2-verifiedaccesstrustprovider-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TrustProviderType](#cfn-ec2-verifiedaccesstrustprovider-trustprovidertype): String
  [UserTrustProviderType](#cfn-ec2-verifiedaccesstrustprovider-usertrustprovidertype): String
```

## Properties<a name="aws-resource-ec2-verifiedaccesstrustprovider-properties"></a>

`Description`  <a name="cfn-ec2-verifiedaccesstrustprovider-description"></a>
A description for the AWS Verified Access trust provider\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceOptions`  <a name="cfn-ec2-verifiedaccesstrustprovider-deviceoptions"></a>
The options for device\-identity trust provider\.  
*Required*: No  
*Type*: [DeviceOptions](aws-properties-ec2-verifiedaccesstrustprovider-deviceoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceTrustProviderType`  <a name="cfn-ec2-verifiedaccesstrustprovider-devicetrustprovidertype"></a>
The type of device\-based trust provider\.  
*Required*: No  
*Type*: String  
*Allowed values*: `crowdstrike | jamf`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OidcOptions`  <a name="cfn-ec2-verifiedaccesstrustprovider-oidcoptions"></a>
The options for an OpenID Connect\-compatible user\-identity trust provider\.  
*Required*: No  
*Type*: [OidcOptions](aws-properties-ec2-verifiedaccesstrustprovider-oidcoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyReferenceName`  <a name="cfn-ec2-verifiedaccesstrustprovider-policyreferencename"></a>
The identifier to be used when working with policy rules\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-verifiedaccesstrustprovider-tags"></a>
The tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustProviderType`  <a name="cfn-ec2-verifiedaccesstrustprovider-trustprovidertype"></a>
The type of Verified Access trust provider\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `device | user`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserTrustProviderType`  <a name="cfn-ec2-verifiedaccesstrustprovider-usertrustprovidertype"></a>
The type of user\-based trust provider\.  
*Required*: No  
*Type*: String  
*Allowed values*: `iam-identity-center | oidc`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-verifiedaccesstrustprovider-return-values"></a>

### Ref<a name="aws-resource-ec2-verifiedaccesstrustprovider-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Verified Access trust provider\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-verifiedaccesstrustprovider-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-verifiedaccesstrustprovider-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The creation time\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
The last updated time\.

`VerifiedAccessTrustProviderId`  <a name="VerifiedAccessTrustProviderId-fn::getatt"></a>
The ID of the Verified Access trust provider\.